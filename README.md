# awesome-claude-code-skills

> A curated list of Agent Skills for Claude Code to supercharge your development workflow

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
![Skills Count](https://img.shields.io/badge/skills-36-brightgreen)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)

**Claude Code just got Skills!** This is the definitive collection of **36 Agent Skills** designed specifically for Claude Code CLI to boost developer productivity, enforce best practices, and automate complex workflows.

> 💡 **New to Skills?** Start with the [Quick Start Guide](#quick-start) • **Looking for something specific?** Use `Ctrl+F` to search

## Contents

- [Quick Start](#quick-start)
- [What are Skills?](#what-are-skills)
- [Featured Skills](#featured-skills)
- [How to Install Skills](#how-to-install-skills)
- [Skills vs MCP vs System Prompts](#skills-vs-mcp-vs-system-prompts)
- [Skill Categories](#skill-categories)
  - [🧪 Testing & Quality](#-testing--quality)
  - [🐛 Debugging & Troubleshooting](#-debugging--troubleshooting)
  - [🤝 Collaboration & Workflow](#-collaboration--workflow)
  - [⚙️ Development & Architecture](#️-development--architecture)
  - [🔒 Security & Performance](#-security--performance)
  - [📚 Documentation & Automation](#-documentation--automation)
  - [🎯 Meta Skills](#-meta-skills)
- [FAQ](#faq)
- [Resources](#resources)
- [Contributing](#contributing)
- [License](#license)

## Quick Start

**Get your first skill running in 30 seconds:**

```bash
# 1. Install obra's superpowers collection (20+ battle-tested skills)
git clone https://github.com/obra/superpowers ~/.claude/skills/superpowers

# 2. Try test-driven-development skill
# In Claude Code, just say: "Let's use TDD to build a user authentication system"
# Claude will automatically load the TDD skill and guide you through RED-GREEN-REFACTOR!
```

**That's it!** Skills load automatically when relevant. No configuration needed.

## What are Skills?

**Agent Skills** are modular capabilities that extend Claude Code's functionality through organized folders containing instructions, scripts, and resources. Each skill teaches Claude how to perform specialized tasks in a repeatable, standardized way.

**Key benefits:**
- **Efficient:** Skills use only 30-50 tokens until loaded
- **Portable:** Works across Claude Code CLI, Claude.ai, and API
- **Composable:** Stack multiple skills together
- **Context-aware:** Claude automatically identifies relevant skills

Skills are available on Claude Pro, Max, Team, and Enterprise plans with code execution enabled.

## Featured Skills

**Start with these 5 essential skills:**

| Skill | Why You Need It | Category |
|-------|----------------|----------|
| [test-driven-development](https://github.com/obra/superpowers) | Write bulletproof code with RED-GREEN-REFACTOR workflow | 🧪 Testing |
| [systematic-debugging](https://github.com/obra/superpowers) | Find bugs 10x faster with 4-phase root cause analysis | 🐛 Debugging |
| [using-git-worktrees](https://github.com/obra/superpowers) | Work on multiple features simultaneously without context switching chaos | 🤝 Workflow |
| [mcp-builder](https://github.com/anthropics/skills) | Build custom MCP servers to extend Claude's capabilities | ⚙️ Development |
| [skill-creator](https://github.com/anthropics/skills) | Create your own skills and contribute to the ecosystem | 🎯 Meta |

## How to Install Skills

### Method 1: Git Clone (Recommended)

```bash
# Linux/macOS
mkdir -p ~/.claude/skills
git clone https://github.com/owner/skill-name ~/.claude/skills/skill-name

# Windows (PowerShell)
mkdir $env:USERPROFILE\.claude\skills
git clone https://github.com/owner/skill-name $env:USERPROFILE\.claude\skills\skill-name
```

**Pro tip:** Clone entire skill collections like [obra/superpowers](https://github.com/obra/superpowers) to get 20+ skills at once!

### Method 2: Manual Installation

1. Create a folder in `~/.claude/skills/`
2. Add a `SKILL.md` file with YAML frontmatter and instructions
3. (Optional) Include supporting scripts and resources

**Verify installation:**
```bash
# Check if skill is loaded
ls ~/.claude/skills/

# Skills load automatically - just start using Claude Code!
```

## Skills vs MCP vs System Prompts

Confused about when to use Skills vs other Claude customization methods? Here's the breakdown:

| Feature | Skills | MCP Servers | System Prompts |
|---------|--------|-------------|----------------|
| **Purpose** | Task-specific workflows | External tool integration | General behavior modification |
| **Setup** | Git clone to `~/.claude/skills/` | Install & configure MCP server | Edit `CLAUDE.md` in project |
| **Activation** | Automatic (context-aware) | Explicit tool calls | Always active |
| **Best For** | TDD, debugging, git workflows | APIs, databases, file systems | Project conventions, style guides |
| **Portability** | Cross-platform (CLI, web, API) | Platform-dependent | Project-specific |
| **Token Cost** | 30-50 until loaded | Per-call | Always consuming tokens |
| **Examples** | `test-driven-development` | Weather API, GitHub integration | "Use TypeScript strict mode" |

**When to use what:**
- ✅ **Skills** → Repeatable workflows (TDD, debugging, code review)
- ✅ **MCP** → External data/tools (APIs, search, databases)
- ✅ **System Prompts** → Project-specific rules and conventions

## Skill Categories

### 🧪 Testing & Quality

#### test-driven-development
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** RED-GREEN-REFACTOR cycle: write failing tests, implement code, refactor for quality
**Use Case:** Building new features with strong test coverage guarantees
**Stars:** ⭐⭐⭐⭐⭐

#### webapp-testing
**Source:** [anthropics/skills](https://github.com/anthropics/skills)
**Description:** Playwright-based web app testing for UI verification and debugging
**Use Case:** Testing web UIs, validating user flows, catching visual regressions
**Stars:** ⭐⭐⭐⭐

#### condition-based-waiting
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Async testing patterns with proper wait conditions to prevent flaky tests
**Use Case:** Testing asynchronous operations, API calls, animations
**Stars:** ⭐⭐⭐⭐

#### testing-anti-patterns
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Identifies common testing mistakes: brittle assertions, test interdependence, poor isolation
**Use Case:** Code reviews, refactoring existing test suites
**Stars:** ⭐⭐⭐

#### e2e-testing-skill
**Status:** Community-needed
**Description:** End-to-end test automation across multiple services and browser environments.
**Use Case:** Integration testing, cross-browser compatibility validation

#### snapshot-testing
**Status:** Community-needed
**Description:** Visual regression testing with component snapshot management for catching unintended UI changes.
**Use Case:** Component libraries, design system maintenance

---

### 🐛 Debugging & Troubleshooting

#### systematic-debugging
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Four-phase root cause process for methodical bug hunting: reproduce, isolate, identify, verify fix.
**Use Case:** Complex bugs, production issues, multi-component failures
**Stars:** ⭐⭐⭐⭐⭐

#### root-cause-tracing
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Deep problem investigation techniques with dependency chain analysis to find underlying issues.
**Use Case:** Tracing cascading failures, understanding system interactions
**Stars:** ⭐⭐⭐⭐

#### verification-before-completion
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Ensures fixes are properly validated before marking work complete. Prevents regression and incomplete solutions.
**Use Case:** Bug fixes, refactoring work, feature additions
**Stars:** ⭐⭐⭐⭐

#### defense-in-depth
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Multiple validation layers for comprehensive error handling and resilience.
**Use Case:** Critical systems, production code, API endpoints
**Stars:** ⭐⭐⭐

#### performance-profiling
**Status:** Community-needed
**Description:** Identify performance bottlenecks, memory leaks, and CPU-intensive operations.
**Use Case:** Optimization work, scaling applications, investigating slowness

---

### 🤝 Collaboration & Workflow

#### requesting-code-review
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Pre-review preparation and PR best practices. Formats diffs, writes clear descriptions, highlights changes.
**Use Case:** Before submitting PRs, preparing for team review
**Stars:** ⭐⭐⭐⭐⭐

#### receiving-code-review
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Constructive feedback integration and iteration on review comments.
**Use Case:** Responding to PR feedback, implementing requested changes
**Stars:** ⭐⭐⭐⭐

#### using-git-worktrees
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Parallel development branches for context switching optimization. Work on multiple features simultaneously.
**Use Case:** Juggling multiple features, emergency hotfixes, experimental branches
**Stars:** ⭐⭐⭐⭐⭐

#### finishing-a-development-branch
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Guides merge/PR decisions and maintaining clean git history with proper squashing and rebasing.
**Use Case:** Preparing features for merge, cleaning up commit history
**Stars:** ⭐⭐⭐⭐

#### brainstorming
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Socratic design refinement and feature exploration through guided questioning.
**Use Case:** Architecture decisions, API design, feature planning
**Stars:** ⭐⭐⭐⭐

#### writing-plans
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Creates detailed implementation strategies and architecture documentation.
**Use Case:** Complex features, system design, technical specs
**Stars:** ⭐⭐⭐⭐⭐

#### executing-plans
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Batch execution with checkpoints for progress tracking and recovery.
**Use Case:** Large refactors, multi-step implementations
**Stars:** ⭐⭐⭐⭐

---

### ⚙️ Development & Architecture

#### mcp-builder
**Source:** [anthropics/skills](https://github.com/anthropics/skills)
**Description:** Create high-quality Model Context Protocol servers for integrating external APIs and services.
**Use Case:** Building custom MCP servers, extending Claude's capabilities
**Stars:** ⭐⭐⭐⭐⭐

#### artifacts-builder
**Source:** [anthropics/skills](https://github.com/anthropics/skills)
**Description:** Build complex claude.ai HTML artifacts using React, Tailwind CSS, and shadcn/ui components.
**Use Case:** Interactive demos, prototypes, data visualizations
**Stars:** ⭐⭐⭐⭐

#### api-development
**Status:** Community-needed
**Description:** RESTful API design patterns with OpenAPI/Swagger generation and best practices.
**Use Case:** Building backend services, documenting APIs

#### database-migration
**Status:** Community-needed
**Description:** Schema version management and safe migration patterns for production databases.
**Use Case:** Database evolution, schema changes, data migrations

#### refactoring-patterns
**Status:** Community-needed
**Description:** Code smell detection and systematic refactoring techniques following established patterns.
**Use Case:** Legacy code modernization, improving code quality

---

### 🔒 Security & Performance

#### security-review
**Status:** Community-needed
**Description:** Automated vulnerability scanning and OWASP compliance checks for codebases.
**Use Case:** Security audits, pre-deployment checks, compliance validation

#### dependency-audit
**Status:** Community-needed
**Description:** Supply chain security analysis with CVE detection in dependencies.
**Use Case:** Regular security checks, updating vulnerable packages

#### performance-optimization
**Status:** Community-needed
**Description:** Algorithmic improvements and resource usage optimization strategies.
**Use Case:** Improving application speed, reducing memory footprint

#### load-testing
**Status:** Community-needed
**Description:** Stress testing patterns and performance benchmarking for production readiness.
**Use Case:** Capacity planning, finding breaking points

---

### 📚 Documentation & Automation

#### documentation-generator
**Status:** Community-needed
**Description:** Auto-generate API documentation and keep docs synchronized with code changes.
**Use Case:** Maintaining up-to-date documentation, API references

#### changelog-automation
**Status:** Community-needed
**Description:** Conventional commits integration with automated release note generation.
**Use Case:** Release management, version tracking

#### ci-cd-integration
**Status:** Community-needed
**Description:** GitHub Actions workflow creation and automated deployment pipeline setup.
**Use Case:** DevOps automation, continuous delivery

---

### 🎯 Meta Skills

#### skill-creator
**Source:** [anthropics/skills](https://github.com/anthropics/skills)
**Description:** Teaches methods for developing effective skills that extend Claude's capabilities following best practices.
**Use Case:** Building custom skills, contributing to the ecosystem
**Stars:** ⭐⭐⭐⭐⭐

#### template-skill
**Source:** [anthropics/skills](https://github.com/anthropics/skills)
**Description:** Minimal skeleton for new skill projects with proper structure and documentation.
**Use Case:** Starting new skills from scratch
**Stars:** ⭐⭐⭐⭐

#### writing-skills
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Creating skills following best practices with proper YAML frontmatter and instruction design.
**Use Case:** Contributing new skills, maintaining skill quality
**Stars:** ⭐⭐⭐⭐

#### sharing-skills
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Contributing skills via branches and pull requests to community repositories.
**Use Case:** Open-source contributions, sharing expertise
**Stars:** ⭐⭐⭐

#### testing-skills-with-subagents
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Validating skill quality and effectiveness using subagent-driven testing.
**Use Case:** Quality assurance for skills, debugging skill behavior
**Stars:** ⭐⭐⭐⭐

#### subagent-driven-development
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Quality-gated iteration with multi-agent workflows for complex tasks.
**Use Case:** Large-scale refactoring, parallel development streams
**Stars:** ⭐⭐⭐⭐⭐

---

## FAQ

### How do I know if a skill is working?

Skills load automatically when Claude detects they're relevant. You'll see Claude using skill-specific patterns (like RED-GREEN-REFACTOR for TDD). To check installed skills:
```bash
ls ~/.claude/skills/
```

### Can I use multiple skills at once?

Yes! Skills are composable. Claude automatically loads and coordinates multiple skills as needed. For example, you might use `test-driven-development` + `systematic-debugging` + `using-git-worktrees` simultaneously.

### Do skills work on all platforms?

Yes! Skills use the same format across Claude Code CLI, Claude.ai, and the Claude API. Install once, use everywhere.

### How do I update skills?

```bash
cd ~/.claude/skills/skill-name
git pull origin main
```

### Can I create my own skills?

Absolutely! Check out the [skill-creator](https://github.com/anthropics/skills) skill and our [Contributing Guide](CONTRIBUTING.md) for best practices.

### Do skills consume tokens?

Minimal! Each skill uses only 30-50 tokens until Claude loads it. Once loaded, only relevant portions are used.

### What's the difference between skills and MCP servers?

See the [comparison table](#skills-vs-mcp-vs-system-prompts) above. TL;DR: Skills for workflows, MCP for external tools.

### Where can I find more skills?

- [obra/superpowers](https://github.com/obra/superpowers) - 20+ battle-tested skills
- [anthropics/skills](https://github.com/anthropics/skills) - Official Anthropic skills
- [claudeskills.info](https://claudeskills.info/) - Searchable directory
- This list! Browse the categories above

### Can I share my skills?

Yes! Submit a PR to this repo or publish your own repository. Use the [sharing-skills](https://github.com/obra/superpowers) skill for guidance.

### Are there any security concerns?

Skills can execute code, so only install from trusted sources. Review the skill's `SKILL.md` and any scripts before installing. See [Security Best Practices](#security-best-practices) in Contributing.

---

## Resources

### Official Documentation
- [Agent Skills Documentation](https://docs.claude.com/en/docs/claude-code/skills) - Official Anthropic skills docs
- [Skills Announcement](https://www.anthropic.com/news/skills) - Claude Skills launch announcement
- [Engineering Deep Dive](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) - Technical details

### Official Repositories
- [anthropics/skills](https://github.com/anthropics/skills) - Official Anthropic skills repository
- [obra/superpowers](https://github.com/obra/superpowers) - Battle-tested core skills library (20+ skills)

### Related Awesome Lists
- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) - Commands, workflows, and tools for Claude Code
- [awesome-claude-skills](https://github.com/BehiSecc/awesome-claude-skills) - General Claude skills (all platforms)
- [awesome-claude](https://github.com/alvinunreal/awesome-claude) - General Claude resources

### Community Resources
- [Claude Skills Hub](https://claudeskills.info/) - Searchable skills directory
- [Simon Willison's Blog](https://simonwillison.net/2025/Oct/16/claude-skills/) - "Claude Skills are awesome, maybe a bigger deal than MCP"

### Tools & Utilities
- [create-claude-skill](https://github.com/anthropics/skills) - Interactive skill creator (basic)
- [template-skill](https://github.com/anthropics/skills) - Minimal skill template

---

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Quick contribution checklist:**
- ✅ Skill has working `SKILL.md` with YAML frontmatter
- ✅ Clear documentation and use cases
- ✅ Actively maintained (commits within 6 months)
- ✅ Relevant to Claude Code CLI workflows
- ✅ No security vulnerabilities or malicious code

**Ways to contribute:**
1. Add new skills to existing categories
2. Create entirely new categories
3. Improve skill descriptions
4. Add usage examples and tutorials
5. Report broken or outdated skills

---

## License

MIT License - see [LICENSE](LICENSE) file for details.

This awesome list is licensed under MIT. Individual skills maintain their own licenses.

---

## Acknowledgments

Special thanks to:
- **Anthropic** for creating Agent Skills and Claude Code
- **[@obra](https://github.com/obra)** for the incredible superpowers skills library
- **The Claude Code community** for continuous innovation

---

**Star this repo** if you find it helpful! ⭐

**Have a skill to share?** Open a PR or create an issue!

**Questions?** Check the [discussions](../../discussions) or open an issue.
