# changelog-automation

A Claude Code skill that generates structured changelogs from git history. Works with conventional commits, freeform messages, tagged releases, or any combination — adapts to what your repo actually has.

## Installation

```bash
# Clone into your skills directory
git clone https://github.com/wyktor33/changelog-automation ~/.claude/skills/changelog-automation

# That's it — the skill is available immediately in Claude Code
```

## Usage

The skill is invoked manually (it writes files, so Claude won't auto-trigger it):

```
/changelog-automation 2.1.0                     # From last tag to HEAD
/changelog-automation 2.1.0 --from v2.0.0       # Between two tags
/changelog-automation --unreleased               # Changes since last tag, no version assigned
/changelog-automation 1.0.0 --from main --to release/1.0   # Compare branches
```

If you run it without arguments, the skill will detect your latest tag and ask you for the version number.

### What happens when you invoke it

1. **Assesses your repo** — checks for tags, conventional commits, existing CHANGELOG.md
2. **Detects the commit range** — uses tags if available, asks you to confirm if not
3. **Classifies every commit** — parses conventional commits structurally, reads and classifies freeform commits by intent
4. **Generates a changelog** — Keep a Changelog format with grouped categories
5. **Asks before writing** — shows you the output first, flags uncertain classifications, lets you correct before saving

### Output format

The skill generates [Keep a Changelog](https://keepachangelog.com/) format:

```markdown
## [2.1.0] - 2026-04-16

### Breaking Changes

- Change default response format to JSON:API (h8i9j0k)

### Added

- **auth:** Add OAuth2 provider support (a1b2c3d)

### Fixed

- Resolve memory leak in connection pool (c3d4e5f)
```

See [examples/sample-output.md](examples/sample-output.md) for a full example.

## How Your Repo Affects Output Quality

The skill adapts to any repo, but the quality of its output directly depends on how your team writes commits. Here's what to expect:

| Your repo has... | Skill output quality | What happens |
|-----------------|---------------------|-------------|
| Conventional commits + tags | Excellent | Fully structured, no guesswork |
| Tags but freeform commits | Good | Claude reads and classifies by intent, flags uncertain ones |
| Conventional commits but no tags | Good | Clean parsing, but you must specify the range manually |
| Freeform commits, no tags | Usable | Intelligent classification with manual range, expect some flagged items |
| Squash-merged everything | Limited | Single large commits lose granularity — Claude reads diffs to compensate |
| WIP/temp/garbage messages | Poor | Most commits skipped — very little to work with |

## Guide: Maintaining a Dev Cycle That Produces Good Changelogs

You don't need to adopt every practice below. Each one independently improves changelog quality. Pick what fits your team.

### Level 1: The Minimum — Write Descriptive Commits

The single highest-impact change. Even without conventions, a descriptive commit message gives the skill enough to classify correctly.

**Bad — the skill can't help you:**
```
fix stuff
update
WIP
.
```

**Good — the skill classifies these accurately:**
```
fix race condition in token refresh when multiple tabs are open
add CSV export to the reports page
remove deprecated v1 authentication endpoints
```

**Rules of thumb:**
- Start with a verb: add, fix, remove, update, refactor, optimize
- Say what changed AND what it affects
- If you squash-merge, edit the squash message to be meaningful

### Level 2: Adopt Conventional Commits

[Conventional Commits](https://www.conventionalcommits.org/) give the skill structured data to work with — no guesswork, no flags, exact categorization.

```
feat(auth): add OAuth2 provider support
fix: resolve memory leak in connection pool
feat!: change default response format to JSON:API
docs: update API reference for v2 endpoints
```

**Format:** `type(scope): description`

| Type | When to use |
|------|------------|
| `feat` | New feature or capability |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `style` | Formatting, no logic change |
| `refactor` | Code restructuring, no behavior change |
| `perf` | Performance improvement |
| `test` | Adding or fixing tests |
| `build` | Build system or dependencies |
| `ci` | CI/CD configuration |
| `chore` | Maintenance, tooling, config |
| `revert` | Reverting a previous commit |

**Breaking changes:** Add `!` before the colon (`feat!:`) or include a `BREAKING CHANGE:` footer in the commit body.

**Scopes** are optional but useful for larger projects — they let the skill group related changes together (e.g., all `auth` changes, all `api` changes).

### Level 3: Tag Your Releases

Tags give the skill automatic range detection. Without them, you have to specify ranges manually every time.

```bash
# After merging to main for a release
git tag -a v2.1.0 -m "Release 2.1.0"
git push origin v2.1.0
```

**Conventions that work:**
- `v1.2.3` (most common)
- `1.2.3` (also works)
- Follow [Semantic Versioning](https://semver.org/): MAJOR.MINOR.PATCH

### Level 4: Atomic Commits

One logical change per commit. This gives the skill the best possible input.

**Instead of:**
```
implement user dashboard with charts, fix auth bug, update deps
```

**Do:**
```
feat(dashboard): add user activity chart
feat(dashboard): add revenue summary widget
fix(auth): prevent session expiry during active use
chore: update chart.js to v4.2
```

Each commit maps to exactly one changelog entry. No ambiguity, no lost information.

### Level 5: Clean Branch History Before Merge

If your branch has messy WIP commits, clean them up before merging:

```bash
# Interactive rebase to squash/reword before merge
git rebase -i main
```

Or use squash-merge with a well-written merge commit:

```bash
# GitHub squash-merge with a proper message
feat(dashboard): add user activity tracking

- Activity chart with daily/weekly/monthly views
- Revenue summary widget
- Export to CSV
```

The `finishing-a-development-branch` skill from obra/superpowers can guide this process.

## Complementary Skills

This skill produces the best results when your workflow includes these other skills. None are required — each one independently improves output quality.

### Commit Quality (direct impact on changelog)

| Skill | Source | How it helps |
|-------|--------|-------------|
| **finishing-a-development-branch** | [obra/superpowers](https://github.com/obra/superpowers) | Guides clean branch history and merge preparation — reduces noise commits |
| **requesting-code-review** | [obra/superpowers](https://github.com/obra/superpowers) | Encourages well-described, atomic commits during PR preparation |

### Workflow Quality (indirect impact — better process = better commits)

| Skill | Source | How it helps |
|-------|--------|-------------|
| **test-driven-development** | [obra/superpowers](https://github.com/obra/superpowers) | TDD produces commits scoped to specific behaviors — maps cleanly to "Added" and "Fixed" entries |
| **writing-plans** | [obra/superpowers](https://github.com/obra/superpowers) | Planned implementations produce structured commit sequences |
| **executing-plans** | [obra/superpowers](https://github.com/obra/superpowers) | Checkpoint-based execution produces commits that map to plan steps |
| **using-git-worktrees** | [obra/superpowers](https://github.com/obra/superpowers) | Isolated workstreams keep feature commits separate from unrelated changes |

### Build & Release (adjacent workflow)

| Skill | Source | How it helps |
|-------|--------|-------------|
| **verification-before-completion** | [obra/superpowers](https://github.com/obra/superpowers) | Ensures changes are validated before release — pairs with changelog as a release checklist |

## FAQ

### Does my project need conventional commits for this to work?

No. The skill works with any commit messages. Conventional commits give the best results (exact classification, no guesswork), but Claude can intelligently classify freeform commits by reading them and their diffs.

### Does my project need tags?

No. Tags let the skill automatically detect version ranges. Without tags, you specify the range manually (by date, commit count, or branch comparison).

### What about monorepos?

You can scope the changelog to a subdirectory:

```
/changelog-automation 2.1.0 --from v2.0.0
```

Then tell Claude to filter by path: "Only include changes in `packages/api/`". The skill uses `git log -- path/` to scope commits.

### What if most of my commits are WIP or meaningless?

The skill skips noise commits (WIP, temp, fixup, single-character messages) and tells you how many were skipped. If the majority are noise, consider adopting Level 1 practices from the dev cycle guide above.

### Can I edit the output before it's written?

Yes. The skill always shows you the generated changelog first and asks before writing. It also flags uncertain classifications so you can correct them.

## License

MIT
