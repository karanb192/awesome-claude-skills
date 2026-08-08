---
name: changelog-automation
description: Generate changelogs and release notes from git history. Parses conventional commits when available, intelligently classifies freeform commits when not. Adapts to any repo — tags or no tags.
when_to_use: When the user asks to generate a changelog, prepare release notes, summarize changes between versions or tags, or update CHANGELOG.md
disable-model-invocation: true
argument-hint: "[version] [--from ref] [--to ref] [--unreleased]"
allowed-tools: Bash(git log *) Bash(git tag *) Bash(git describe *) Bash(git diff *) Bash(git rev-list *) Bash(git rev-parse *)
---

# Changelog Automation

Generate structured changelogs from git history. Adapts to the repo's actual state — works with conventional commits, freeform messages, tagged releases, or none of the above. Output follows [Keep a Changelog](https://keepachangelog.com/) format.

## When to Use

- User says "generate changelog", "release notes", or "what changed since [version]"
- Preparing a release and need a summary of all changes
- Updating an existing CHANGELOG.md with new entries

## Complementary Skills

This skill produces better output when the project also uses:

- **test-driven-development** (obra/superpowers) — TDD commits naturally produce well-scoped, descriptive messages tied to specific behaviors
- **writing-plans** (obra/superpowers) — planned implementations lead to structured commit sequences rather than ad-hoc fixes
- **executing-plans** (obra/superpowers) — checkpoint-based execution produces commits that map cleanly to plan steps
- **requesting-code-review** (obra/superpowers) — PR preparation encourages well-described, atomic commits
- **finishing-a-development-branch** (obra/superpowers) — clean branch history with squashed or rebased commits reduces noise

Without these, the skill still works — it just has to work harder to classify freeform commits.

## Inputs

- `$ARGUMENTS` — version string and/or flags
  - `/changelog-automation 2.1.0` — generate changelog for version 2.1.0 (from last tag to HEAD)
  - `/changelog-automation 2.1.0 --from v2.0.0` — changelog between two specific points
  - `/changelog-automation --unreleased` — list changes since the last tag without assigning a version
  - `/changelog-automation 1.0.0 --from main --to release/1.0` — compare branches

If no arguments are provided, prompt the user for the version number. Detect the last tag automatically.

## Core Process

1. **Assess repo** — detect what the repo actually has to work with
2. **Discover range** — determine the commit range
3. **Parse and classify commits** — structured or intelligent classification
4. **Generate output** — format as Keep a Changelog markdown
5. **Present to user** — show the changelog and ask whether to write/update CHANGELOG.md

---

## Step 1: Assess Repo

Before doing anything, understand what you have to work with. Run these checks:

```bash
# Check for tags
TAG_COUNT=$(git tag | wc -l | tr -d ' ')

# Check for conventional commits (sample last 30)
CONVENTIONAL_COUNT=$(git log -30 --pretty=format:"%s" | grep -cE '^(feat|fix|docs|style|refactor|perf|test|build|ci|chore|revert)(\(.+\))?(!)?: ' || true)
TOTAL_SAMPLE=$(git log -30 --oneline | wc -l | tr -d ' ')

# Check for existing CHANGELOG.md
CHANGELOG_EXISTS=$(test -f CHANGELOG.md && echo "yes" || echo "no")
```

Classify the repo into one of four modes:

| Mode | Tags? | Conventional Commits? | Strategy |
|------|-------|-----------------------|----------|
| **Structured** | Yes | >70% of sample | Parse conventionally, use tags for ranges |
| **Tagged-freeform** | Yes | <70% of sample | Intelligent classification, use tags for ranges |
| **Untagged-conventional** | No | >70% of sample | Parse conventionally, require user-specified range |
| **Freeform** | No | <70% of sample | Intelligent classification, require user-specified range |

Report the detected mode to the user:

> **Repo assessment:** Found {N} tags, {X}/{Y} recent commits follow conventional format.
> Using **{mode}** mode.

If mode is **Freeform** or **Tagged-freeform**, add:

> Freeform commits detected. I will read each commit and classify it by intent (feature, fix, refactor, etc.). Results may need light editing.

---

## Step 2: Discover Range

### When tags exist

```bash
# Get the latest tag
LATEST_TAG=$(git describe --tags --abbrev=0 2>/dev/null)

# If --from flag provided, use that instead
# Verify the reference exists before using it
git rev-parse --verify "$FROM_REF" >/dev/null 2>&1
```

Use the range `$LATEST_TAG..HEAD` unless the user specifies otherwise.

### When no tags exist

Offer these options to the user:

1. **All history** — from initial commit to HEAD (good for first-ever changelog)
   ```bash
   INITIAL_COMMIT=$(git rev-list --max-parents=0 HEAD)
   ```
2. **Date-based** — "changes since 2026-01-01"
   ```bash
   git log --after="2026-01-01" --pretty=format:"%H|%s|%an|%ad" --date=short
   ```
3. **Commit-count** — "last 50 commits"
   ```bash
   git log -50 --pretty=format:"%H|%s|%an|%ad" --date=short
   ```
4. **Branch comparison** — "changes on this branch vs main"
   ```bash
   git log main..HEAD --pretty=format:"%H|%s|%an|%ad" --date=short
   ```

Do not silently default to "all history" — that can be thousands of commits. Always confirm with the user.

---

## Step 3: Parse and Classify Commits

Fetch commits in the range:

```bash
git log $FROM..$TO --pretty=format:"%H|%s|%an|%ad" --date=short --no-merges
```

Always exclude merge commits (`--no-merges`).

### For conventional commits

Parse each subject line against this pattern:

```
^(feat|fix|docs|style|refactor|perf|test|build|ci|chore|revert)(\(.+\))?(!)?:\s*(.+)$
```

Components:
- **type** — the commit type (feat, fix, etc.)
- **scope** — optional, in parentheses (e.g., `auth`, `api`)
- **breaking indicator** — `!` before the colon
- **description** — the rest of the subject line

Also check commit bodies for `BREAKING CHANGE:` or `BREAKING-CHANGE:` footers:

```bash
git log $FROM..$TO --pretty=format:"%H%n%B%n---END---" --no-merges
```

### For freeform commits — intelligent classification

This is where Claude adds value no CLI tool can. For each freeform commit:

1. Read the subject line and body
2. If the diff is small (<50 lines), read it: `git diff $HASH~1..$HASH --stat`
3. Classify by **intent**, not keywords:

| Intent | Signals | Maps to |
|--------|---------|---------|
| New capability | "add", "introduce", "implement", "support", new files created | `### Added` |
| Bug fix | "fix", "resolve", "correct", "patch", "handle", "prevent", changes in error paths | `### Fixed` |
| Breaking change | "remove", "drop", "rename public API", "change default", deleted public interfaces | `### Breaking Changes` |
| Performance | "optimize", "speed", "cache", "reduce memory", "batch" | `### Performance` |
| Documentation | "readme", "docs", "comment", "jsdoc", changes only in .md or doc files | `### Documentation` |
| Refactor | "refactor", "extract", "reorganize", "clean up", "rename" (internal), structural changes with no behavior change | `### Changed` |
| Build/CI | "ci", "pipeline", "docker", "workflow", "deploy", changes in CI config files | `### Build` |
| Chore | "bump", "update deps", "lint", "format", lock file changes | `### Other` |

**When uncertain**, classify as `### Other` rather than guessing wrong. Flag uncertain classifications to the user:

> Note: I classified "{commit message}" as a fix based on the diff, but the message is ambiguous. Please verify.

### Squashed / vague commits

Some commits are useless for changelogs:
- `"WIP"`, `"temp"`, `"asdf"`, `"."` — skip these, note them as skipped
- `"update"`, `"changes"`, `"stuff"` — read the diff to classify, or skip and flag
- Single mega-commits (500+ lines changed) — warn the user that granularity is lost

---

## Step 4: Generate Output

Group commits into these categories, in this order:

| Category | Heading | Conventional Types |
|----------|---------|-------------------|
| Breaking Changes | `### Breaking Changes` | Any type with `!` or `BREAKING CHANGE` footer |
| Features | `### Added` | `feat` |
| Bug Fixes | `### Fixed` | `fix` |
| Performance | `### Performance` | `perf` |
| Documentation | `### Documentation` | `docs` |
| Refactoring | `### Changed` | `refactor`, `style` |
| Build & CI | `### Build` | `build`, `ci` |
| Other | `### Other` | `chore`, `test`, `revert`, unclassified |

Only include categories that have commits. Skip empty sections.

If a commit appears in Breaking Changes, do NOT also list it under its type category.

### Scope grouping

If scopes are present, group entries by scope within each category:

```markdown
### Added

- **auth:** Add OAuth2 provider support (a1b2c3d)
- **auth:** Add session refresh endpoint (b2c3d4e)
- **api:** Add pagination to list endpoints (c3d4e5f)
```

If no scopes are present, list entries flat.

### Output template

```markdown
## [VERSION] - YYYY-MM-DD

### Breaking Changes

- **scope:** Description (short-hash)

### Added

- Description (short-hash)

### Fixed

- Description (short-hash)
```

Rules:
- Use today's date unless the user specifies otherwise
- Include the 7-char short commit hash in parentheses
- Capitalize the first letter of each description
- If commits were skipped or flagged uncertain, add a note at the bottom:
  ```markdown
  > **Note:** {N} commits were skipped (vague messages). {M} classifications are uncertain — review entries marked with (?).
  ```

---

## Step 5: Present and Write

1. Show the generated changelog to the user
2. If any uncertain classifications exist, list them and ask for corrections
3. Ask: "Write this to CHANGELOG.md?"
4. If CHANGELOG.md exists, insert the new version entry below the `# Changelog` header and above existing entries
5. If CHANGELOG.md does not exist, create it:

```markdown
# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/),
and this project adheres to [Semantic Versioning](https://semver.org/).

## [VERSION] - YYYY-MM-DD

(entries here)
```

---

## Common Mistakes

- **Duplicating breaking changes** — a `feat!:` commit goes in Breaking Changes only, not also in Added
- **Wrong commit range** — always verify the ref exists before using it as a range boundary
- **Overwriting existing entries** — prepend new versions, never replace the file
- **Missing body breaking changes** — check commit bodies, not just subjects, for `BREAKING CHANGE:` footers
- **Over-classifying freeform commits** — when in doubt, put it in Other and flag it, rather than guessing wrong
- **Including noise commits** — skip WIP, temp, fixup commits; they are not changelog-worthy
- **Silently defaulting to all history** — on untagged repos, always confirm the range with the user first

## Edge Cases

- **No tags exist** — offer range options (date, count, branch), do not silently use all history
- **No conventional commits** — use intelligent classification, flag uncertain items
- **Monorepo** — if the user specifies a path filter, use `git log -- path/` to scope commits
- **Empty range** — tell the user "No changes found between X and Y"
- **All commits are squash-merged** — warn about lost granularity, read diffs to classify
- **Mixed conventions** — some commits conventional, some not. Parse what you can, classify the rest intelligently
- **Extremely large ranges (500+ commits)** — warn the user, offer to summarize by category count first before generating full output
