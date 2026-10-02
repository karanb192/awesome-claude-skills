# awesome-claude-skills

A directory of Agent Skills for Claude. Find a skill for your task, read its
instructions, and follow its source repository's install guide.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

| I want to... | Start with |
|---|---|
| Work with PDFs, documents, or spreadsheets | [Document & File Processing](#-document--file-processing) |
| Write tests or debug code | [Tests][tests] · [Debugging][debugging] |
| Build a development workflow | [Development & Architecture](#️-development--architecture) |
| Browse complete collections | [Skill Collections](#skill-collections) |

[tests]: #-testing--quality
[debugging]: #-debugging--troubleshooting

## Quick Start

For document work in Claude Code, install Anthropic's document skills from
your terminal:

```bash
claude plugin marketplace add anthropics/skills
claude plugin install document-skills@anthropic-agent-skills
```

Then ask Claude to extract the form fields from a PDF you provide.
[Anthropic's installation guide](https://github.com/anthropics/skills#claude-code)
covers the plugin and other supported environments.

Read the skill's instructions and bundled scripts before enabling it. A listing
is not a security audit or a guarantee that the skill fits your project.

## Contents

- [Quick Start](#quick-start)
- [What are Skills?](#what-are-skills)
- [Featured Skills](#featured-skills)
- [How to Install Skills](#how-to-install-skills)
- [Skills vs MCP vs System Prompts](#skills-vs-mcp-vs-system-prompts)
- [Skill Categories](#skill-categories)
  - [📄 Document & File Processing](#-document--file-processing)
  - [🧪 Testing & Quality](#-testing--quality)
  - [🐛 Debugging & Troubleshooting](#-debugging--troubleshooting)
  - [🤝 Collaboration & Workflow](#-collaboration--workflow)
  - [⚙️ Development & Architecture](#️-development--architecture)
  - [🔒 Security & Performance](#-security--performance)
  - [📚 Documentation & Automation](#-documentation--automation)
  - [🎬 Media & Content Creation](#-media--content-creation)
  - [📊 Data & Analysis](#-data--analysis)
  - [💰 Finance & Tax](#-finance--tax)
  - [✍️ Writing & Research](#️-writing--research)
  - [🎯 Meta Skills](#-meta-skills)
- [Skill Collections](#skill-collections)
- [FAQ](#faq)
- [Resources](#resources)
- [Contributors](#contributors)
- [Contributing](#contributing)
- [License](#license)

## What are Skills?

**Agent Skills** are modular capabilities that extend Claude's functionality
through organized folders containing instructions, scripts, and resources. Each
skill teaches Claude how to perform specialized tasks in a repeatable,
standardized way.

**Key benefits:**

- **Efficient:** Skills use only 30-50 tokens until loaded
- **Portable:** Works across Claude Code CLI, Claude.ai, and API
- **Composable:** Stack multiple skills together
- **Context-aware:** Claude automatically identifies relevant skills

Skills are available on Claude Pro, Max, Team, and Enterprise plans with code
execution enabled.

## Featured Skills

**Start with these top 10 essential skills:**

| Skill | Why You Need It | Category | Verified |
|-------|----------------|----------|----------|
| [test-driven-development](https://github.com/obra/superpowers) | Write bulletproof code with RED-GREEN-REFACTOR workflow | 🧪 Testing | ✅ |
| [systematic-debugging](https://github.com/obra/superpowers) | Find bugs 10x faster with 4-phase root cause analysis | 🐛 Debugging | ✅ |
| [using-git-worktrees](https://github.com/obra/superpowers) | Work on multiple features simultaneously without context switching | 🤝 Workflow | ✅ |
| [mcp-builder](https://github.com/anthropics/skills) | Build custom MCP servers to extend Claude's capabilities | ⚙️ Development | ✅ |
| [pdf](https://github.com/anthropics/skills) | Extract text, tables, metadata from PDFs with merge & annotation support | 📄 Documents | ✅ |
| [docx](https://github.com/anthropics/skills) | Create, edit, and analyze Word documents with tracked changes | 📄 Documents | ✅ |
| [artifacts-builder](https://github.com/anthropics/skills) | Build complex React artifacts with Tailwind CSS and shadcn/ui | ⚙️ Development | ✅ |
| [skill-creator](https://github.com/anthropics/skills) | Create your own skills and contribute to the ecosystem | 🎯 Meta | ✅ |
| [requesting-code-review](https://github.com/obra/superpowers) | Pre-review preparation with formatted diffs and clear PR descriptions | 🤝 Workflow | ✅ |
| [subagent-driven-development](https://github.com/obra/superpowers) | Quality-gated iteration with multi-agent workflows for complex tasks | 🎯 Meta | ✅ |

## How to Install Skills

Use the install guide in the source repository. Collections can ship as plugins,
individual skill folders, or both; choose one route for each collection.

- [Anthropic skills](https://github.com/anthropics/skills#claude-code) provides
  document and example plugins.
- [Superpowers](https://github.com/obra/superpowers#installation) provides
  installation instructions for each supported coding agent.
- For a standalone Claude Code skill, place its folder at
  `~/.claude/skills/<skill-name>/` for personal use or
  `.claude/skills/<skill-name>/` inside one project. The folder must contain
  `SKILL.md`; keep its supporting files with it. See the
  [Claude Code skill guide][skill-guide].

[skill-guide]: https://code.claude.com/docs/en/skills#choose-where-skills-load

Use the source project's own verification steps after installation. This
directory does not install or update the listed skills.

## Skills vs MCP vs System Prompts

Confused about when to use Skills vs other Claude customization methods? Here's
the breakdown:

| Feature | Skills | MCP Servers | System Prompts |
|---------|--------|-------------|----------------|
| **Purpose** | Task-specific workflows | External tool integration | General behavior modification |
| **Setup** | Source install guide | Server config | Project instructions |
| **Activation** | Automatic (context-aware) | Explicit tool calls | Always active |
| **Best For** | TDD, debugging, git workflows | APIs, databases, file systems | Project conventions, style guides |
| **Portability** | Host-dependent | Host-dependent | Project-specific |
| **Token Cost** | 30-50 until loaded | Per-call | Always consuming tokens |
| **Examples** | `test-driven-development` | Weather API, GitHub integration | "Use TypeScript strict mode" |

**When to use what:**

- ✅ **Skills** → Repeatable workflows (TDD, debugging, code review)
- ✅ **MCP** → External data/tools (APIs, search, databases)
- ✅ **System Prompts** → Project-specific rules and conventions

## Skill Categories

### 📄 Document & File Processing

#### pdf

**Source:** [anthropics/skills](https://github.com/anthropics/skills) |
**Verified:** ✅
**Description:** Extract text, tables, metadata from PDFs. Merge documents and
add annotations.
**Use Case:** Processing contracts, extracting data from reports, combining PDF files
**Stars:** ⭐⭐⭐⭐⭐

#### docx

**Source:** [anthropics/skills](https://github.com/anthropics/skills) |
**Verified:** ✅
**Description:** Create, edit, and analyze Word documents with support for
tracked changes and comments.
**Use Case:** Automating document generation, processing feedback, extracting
structured data
**Stars:** ⭐⭐⭐⭐⭐

#### xlsx

**Source:** [anthropics/skills](https://github.com/anthropics/skills) |
**Verified:** ✅
**Description:** Excel spreadsheet operations including formulas, charts, pivot
tables, and data validation.
**Use Case:** Financial reports, data analysis, automated spreadsheet generation
**Stars:** ⭐⭐⭐⭐⭐

#### pptx

**Source:** [anthropics/skills](https://github.com/anthropics/skills) |
**Verified:** ✅
**Description:** PowerPoint presentation creation with templates, charts, and
multimedia integration.
**Use Case:** Automated slide generation, presentation analysis, template customization
**Stars:** ⭐⭐⭐⭐

---

### 🧪 Testing & Quality

#### test-driven-development

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** RED-GREEN-REFACTOR cycle: write failing tests, implement code,
refactor for quality
**Use Case:** Building new features with strong test coverage guarantees
**Stars:** ⭐⭐⭐⭐⭐

#### webapp-testing

**Source:** [anthropics/skills](https://github.com/anthropics/skills) |
**Verified:** ✅
**Description:** Playwright-based web app testing for UI verification and debugging
**Use Case:** Testing web UIs, validating user flows, catching visual regressions
**Stars:** ⭐⭐⭐⭐

#### condition-based-waiting

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Async testing patterns with proper wait conditions to prevent
flaky tests
**Use Case:** Testing asynchronous operations, API calls, animations
**Stars:** ⭐⭐⭐⭐

#### testing-anti-patterns

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Identifies common testing mistakes: brittle assertions, test
interdependence, poor isolation
**Use Case:** Code reviews, refactoring existing test suites
**Stars:** ⭐⭐⭐

#### e2e-testing-skill

**Status:** Community-needed
**Description:** End-to-end test automation across multiple services and browser
environments.
**Use Case:** Integration testing, cross-browser compatibility validation

#### snapshot-testing

**Status:** Community-needed
**Description:** Visual regression testing with component snapshot management.
**Use Case:** Component libraries, design system maintenance

---

### 🐛 Debugging & Troubleshooting

#### agenttrace-session-audit

**Source:** [luoyuctl/agenttrace](https://github.com/luoyuctl/agenttrace)
**Description:** Audits agent sessions for cost, tokens, failures, and latency.
**Use Case:** Debugging Claude Code, Codex, Gemini, Aider, and Cursor runs.
**Stars:** ⭐⭐⭐

#### systematic-debugging

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Four-phase root cause process: reproduce, isolate, identify,
verify fix.
**Use Case:** Complex bugs, production issues, multi-component failures
**Stars:** ⭐⭐⭐⭐⭐

#### root-cause-tracing

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Deep problem investigation with dependency chain analysis.
**Use Case:** Tracing cascading failures, understanding system interactions
**Stars:** ⭐⭐⭐⭐

#### verification-before-completion

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Ensures fixes are validated before marking work complete.
**Use Case:** Bug fixes, refactoring work, feature additions
**Stars:** ⭐⭐⭐⭐

#### defense-in-depth

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Multiple validation layers for comprehensive error handling.
**Use Case:** Critical systems, production code, API endpoints
**Stars:** ⭐⭐⭐

#### performance-profiling

**Status:** Community-needed
**Description:** Identify performance bottlenecks, memory leaks, and
CPU-intensive operations.
**Use Case:** Optimization work, scaling applications, investigating slowness

---

### 🤝 Collaboration & Workflow

#### ax-extract-workflow

**Source:** [Necmttn/ax](https://github.com/Necmttn/ax) | **Verified:** ⏳
**Description:** Reconstructs shipped-feature workflows from local ax session history.
**Use Case:** Replaying the decisions and handoffs behind a finished feature
**Stars:** ⭐⭐⭐

#### requesting-code-review

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Pre-review preparation and PR best practices with formatted diffs.
**Use Case:** Before submitting PRs, preparing for team review
**Stars:** ⭐⭐⭐⭐⭐

#### receiving-code-review

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Constructive feedback integration and iteration on review comments.
**Use Case:** Responding to PR feedback, implementing requested changes
**Stars:** ⭐⭐⭐⭐

#### using-git-worktrees

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Parallel development branches for context switching optimization.
**Use Case:** Juggling multiple features, emergency hotfixes, experimental branches
**Stars:** ⭐⭐⭐⭐⭐

#### finishing-a-development-branch

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Guides merge/PR decisions and maintaining clean git history.
**Use Case:** Preparing features for merge, cleaning up commit history
**Stars:** ⭐⭐⭐⭐

#### brainstorming

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Socratic design refinement and feature exploration through
guided questioning.
**Use Case:** Architecture decisions, API design, feature planning
**Stars:** ⭐⭐⭐⭐

#### writing-plans

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Creates detailed implementation strategies and architecture documentation.
**Use Case:** Complex features, system design, technical specs
**Stars:** ⭐⭐⭐⭐⭐

#### executing-plans

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Batch execution with checkpoints for progress tracking and recovery.
**Use Case:** Large refactors, multi-step implementations
**Stars:** ⭐⭐⭐⭐

#### pr-review

**Source:**
[priyank766/OpenSource-SKILL](https://github.com/priyank766/OpenSource-SKILL) |
**Verified:** ⏳
**Description:** Detection-first pull request review; a weighted 10-point filter
keeps only the 2-3 findings worth a comment.
**Use Case:** Reviewing open-source PRs as a maintainer without burying the
author in nits
**Stars:** ⭐⭐⭐

---

### ⚙️ Development & Architecture

#### mcp-builder

**Source:** [anthropics/skills](https://github.com/anthropics/skills) |
**Verified:** ✅
**Description:** Create high-quality Model Context Protocol servers for external
integrations.
**Use Case:** Building custom MCP servers, extending Claude's capabilities
**Stars:** ⭐⭐⭐⭐⭐

#### artifacts-builder

**Source:** [anthropics/skills](https://github.com/anthropics/skills) |
**Verified:** ✅
**Description:** Build complex claude.ai HTML artifacts using React, Tailwind
CSS, and shadcn/ui.
**Use Case:** Interactive demos, prototypes, data visualizations
**Stars:** ⭐⭐⭐⭐

#### api-development

**Status:** Community-needed
**Description:** RESTful API design patterns with OpenAPI/Swagger generation.
**Use Case:** Building backend services, documenting APIs

#### database-migration

**Status:** Community-needed
**Description:** Schema version management and safe migration patterns for production.
**Use Case:** Database evolution, schema changes, data migrations

#### refactoring-patterns

**Status:** Community-needed
**Description:** Code smell detection and systematic refactoring techniques.
**Use Case:** Legacy code modernization, improving code quality

---

### 🔒 Security & Performance

#### security-review

**Status:** Community-needed
**Description:** Automated vulnerability scanning and OWASP compliance checks.
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
**Description:** Stress testing patterns and performance benchmarking.
**Use Case:** Capacity planning, finding breaking points

---

### 📚 Documentation & Automation

#### process-builder

**Source:**
[Castaldo-Solutions/process-builder](https://github.com/Castaldo-Solutions/process-builder)
| **Verified:** ⏳
**Description:** Interviews you about a business process and generates a BPMN
swimlane diagram as a .drawio file.
**Use Case:** Process mapping, AS-IS analysis with pain points, TO-BE automation
roadmaps
**Stars:** ⭐⭐⭐

#### documentation-generator

**Status:** Community-needed
**Description:** Auto-generate API documentation and keep docs synchronized with
code.
**Use Case:** Maintaining up-to-date documentation, API references

#### changelog-automation

**Status:** Community-needed
**Description:** Conventional commits integration with automated release note generation.
**Use Case:** Release management, version tracking

#### ci-cd-integration

**Status:** Community-needed
**Description:** GitHub Actions workflow creation and automated deployment pipelines.
**Use Case:** DevOps automation, continuous delivery

---

### 🎬 Media & Content Creation

#### bria-ai

**Source:**
[Bria-AI/bria-skill](https://github.com/Bria-AI/bria-skill/tree/dev/skills/bria-ai)
| **Verified:** ⏳
**Description:** Generate, edit, and remove image backgrounds via the Bria.ai
API — text-to-image, natural-language edits, transparent PNGs.
**Use Case:** Hero images, product photos, icons, and cutouts for web,
e-commerce, and marketing pipelines
**Stars:** ⭐⭐⭐⭐

#### canvas-design

**Source:** Community | **Verified:** ⏳
**Description:** Create visual designs and graphics using Claude's canvas capabilities.
**Use Case:** Quick mockups, diagrams, visual brainstorming
**Stars:** ⭐⭐⭐

#### slack-gif-creator

**Source:** Community | **Verified:** ⏳
**Description:** Generate custom GIFs for Slack communication and team engagement.
**Use Case:** Team communication, visual humor, notifications
**Stars:** ⭐⭐

#### algorithmic-art

**Source:** Community | **Verified:** ⏳
**Description:** Generate procedural art and visualizations using code-based techniques.
**Use Case:** Creative coding, data visualization, generative design
**Stars:** ⭐⭐⭐

#### video-editing-helper

**Status:** Community-needed
**Description:** Assist with video editing workflows, ffmpeg commands, and transitions.
**Use Case:** Video production, content creation, media processing

---

### 📊 Data & Analysis

#### claude-ecom

**Source:**
[takechanman1228/claude-ecom](https://github.com/takechanman1228/claude-ecom) |
**Verified:** ⏳
**Description:** Ecommerce business review: turn order CSVs into KPI trees, ~30
health checks, RFM cohorts, and action plans across 30d/90d/365d
**Use Case:** Monthly D2C business reviews, revenue/retention/margin
diagnostics, automated consultant-quality analysis
**Stars:** ⭐⭐⭐

#### data-visualization

**Status:** Community-needed
**Description:** Create charts, graphs, and interactive visualizations from datasets.
**Use Case:** Data exploration, reporting, presentation of insights

#### sql-query-builder

**Status:** Community-needed
**Description:** Generate optimized SQL queries with proper indexing and
performance tuning.
**Use Case:** Database queries, data extraction, performance optimization

#### csv-processing

**Status:** Community-needed
**Description:** Parse, transform, and analyze CSV files with data cleaning and validation.
**Use Case:** Data migration, ETL processes, data quality checks

---

### 💰 Finance & Tax

#### itr-wala

**Source:** [karanb192/itr-wala](https://github.com/karanb192/itr-wala) |
**Verified:** ✅
**Description:** Prepares Indian income-tax returns (AY 2026-27): AI reads Form
16/AIS, deterministic Python computes every rupee.
**Use Case:** Filing ITR-1/2/3/4 yourself: both regimes compared, deductions
interviewed, portal walkthrough
**Stars:** ⭐⭐⭐

#### file-itr

**Source:** [shivprime94/file-itr](https://github.com/shivprime94/file-itr) |
**Verified:** ✅
**Description:** The first Indian ITR skill: prompt-driven portal walkthrough
with hard-won field notes and AIS research.
**Use Case:** Prompt-based guidance through the income-tax portal for Indian returns
**Stars:** ⭐⭐⭐

---

### ✍️ Writing & Research

#### brand-guidelines

**Source:** Community | **Verified:** ⏳
**Description:** Maintain and enforce brand voice, style, and messaging consistency.
**Use Case:** Content creation, marketing materials, company communications
**Stars:** ⭐⭐⭐⭐

#### business-name-fit

**Source:**
[Elham-Farajnejad/business-name-fit](https://github.com/Elham-Farajnejad/business-name-fit)
| **Verified:** ⏳
**Description:** Picks or vets a business name that stays authentic to your
culture while working in your target market, via 8 cross-cultural checks.
**Use Case:** Naming a company or product across languages; catching a name that
reads well at home but fails abroad
**Stars:** ⭐⭐⭐

#### internal-comms

**Source:** Community | **Verified:** ⏳
**Description:** Draft internal communications, memos, and team announcements.
**Use Case:** HR communications, team updates, policy announcements
**Stars:** ⭐⭐⭐

#### research-assistant

**Status:** Community-needed
**Description:** Gather, synthesize, and cite sources for research projects.
**Use Case:** Academic research, market analysis, competitive intelligence

#### technical-writing

**Status:** Community-needed
**Description:** Create clear technical documentation following industry best practices.
**Use Case:** API docs, user manuals, technical specifications

---

### 🎯 Meta Skills

#### skill-creator

**Source:** [anthropics/skills](https://github.com/anthropics/skills) |
**Verified:** ✅
**Description:** Teaches methods for developing effective skills following best practices.
**Use Case:** Building custom skills, contributing to the ecosystem
**Stars:** ⭐⭐⭐⭐⭐

#### template-skill

**Source:** [anthropics/skills](https://github.com/anthropics/skills) |
**Verified:** ✅
**Description:** Minimal skeleton for new skill projects with proper structure.
**Use Case:** Starting new skills from scratch
**Stars:** ⭐⭐⭐⭐

#### writing-skills

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Creating skills following best practices with proper YAML frontmatter.
**Use Case:** Contributing new skills, maintaining skill quality
**Stars:** ⭐⭐⭐⭐

#### sharing-skills

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Contributing skills via branches and pull requests to community
repositories.
**Use Case:** Open-source contributions, sharing expertise
**Stars:** ⭐⭐⭐

#### testing-skills-with-subagents

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Validating skill quality and effectiveness using
subagent-driven testing.
**Use Case:** Quality assurance for skills, debugging skill behavior
**Stars:** ⭐⭐⭐⭐

#### subagent-driven-development

**Source:** [obra/superpowers](https://github.com/obra/superpowers) |
**Verified:** ✅
**Description:** Quality-gated iteration with multi-agent workflows for complex tasks.
**Use Case:** Large-scale refactoring, parallel development streams
**Stars:** ⭐⭐⭐⭐⭐

---

## Skill Collections

Looking for curated skill bundles? Start with these collections:

| Collection | Skills | Maintainer | Focus Area |
|------------|--------|------------|------------|
| [obra/superpowers](https://github.com/obra/superpowers) | 20+ | @obra | Development workflows & best practices |
| [anthropics/skills](https://github.com/anthropics/skills) | 10+ | @anthropics | Official skills & document processing |
| [Marketing Skills](https://github.com/coreyhaines31/marketingskills) | 49 | @coreyhaines31 | Marketing: SEO, copywriting, cold email, pricing, CRO, ads, analytics |
| [JasonColapietro/suede-creator-skills](https://github.com/JasonColapietro/suede-creator-skills) | 67 | @JasonColapietro | Code quality, design, marketing & shipping |
| [inhouseseo/superseo-skills](https://github.com/inhouseseo/superseo-skills) | 11 | @inhouseseo | SEO audits, content writing, link building, E-E-A-T |
| [kpab/claude-fable-5-skills](https://github.com/kpab/claude-fable-5-skills) | 10 | @kpab | Fable 5-native skills: effort calibration, scope guarding & subagent orchestration |
| [ChatCrystal](https://github.com/ZengLiangYi/ChatCrystal/tree/main/skills) | 3 | @ZengLiangYi | Local-first memory recall and writeback for AI coding sessions |
| [Affitor/affiliate-skills](https://github.com/Affitor/affiliate-skills) | 45 | @Affitor | Affiliate marketing full funnel: research, content, SEO, landing pages, distribution, analytics, automation |
| [noizai/skills](https://github.com/noizai/skills) | 2+ | @noizai | TTS dubbing and companion voice presets |

---

## FAQ

### How do I know if a skill is working?

Follow the source project's verification steps, then try a task it covers.
For the document plugin in [Quick Start](#quick-start), provide a PDF and
ask Claude to extract its form fields. Check the result against the file.
Listing `~/.claude/skills/` only checks standalone folders in that
directory; it does not list skills installed through plugins.

### Can I use multiple skills at once?

Yes! Skills are composable. Claude automatically loads and coordinates multiple
skills as needed. For example, you might use `test-driven-development` +
`systematic-debugging` + `using-git-worktrees` simultaneously.

### Do skills work on all platforms?

The skill format is shared, but installation and available tools depend
on the host. Check the source project's supported environments and install
instructions. Installing a Claude Code plugin does not install it in
Claude.ai or the API. [Anthropic's guide][anthropic-install] describes
the separate routes for its skills.

[anthropic-install]: https://github.com/anthropics/skills#try-in-claude-code-claudeai-and-the-api

### How do I update skills?

Use the update route for your installation. For a Claude Code plugin,
follow the [plugin update guide][plugin-updates]. For a standalone skill
folder, follow its source repository's update instructions; use Git only
if that folder is a Git checkout. Copied folders and plugin-managed
installs do not share a universal `git pull` command.

[plugin-updates]: https://code.claude.com/docs/en/discover-plugins#keep-plugins-updated

### Can I create my own skills?

Absolutely! Check out the [skill-creator](https://github.com/anthropics/skills)
skill and our [Contributing Guide](CONTRIBUTING.md) for best practices.

### Do skills consume tokens?

Minimal! Each skill uses only 30-50 tokens until Claude loads it. Once loaded,
only relevant portions are used.

### What's the difference between skills and MCP servers?

See the [comparison table](#skills-vs-mcp-vs-system-prompts) above. TL;DR:
Skills for workflows, MCP for external tools.

### Where can I find more skills?

- [obra/superpowers](https://github.com/obra/superpowers) - 20+ battle-tested skills
- [anthropics/skills](https://github.com/anthropics/skills) - Official Anthropic
  skills
- [claudeskills.info](https://claudeskills.info/) - Searchable directory
- This list! Browse the categories above

### Can I share my skills?

Yes! Submit a PR to this repo or publish your own repository. Use the
[sharing-skills](https://github.com/obra/superpowers) skill for guidance.

### Are there any security concerns?

Skills can execute code, so only install from trusted sources. Review the
skill's `SKILL.md` and any scripts before installing. Look for the ✅ Verified
badge on skills that have been community-reviewed.

---

## Resources

### Official Documentation

- [Agent Skills
  Documentation](https://docs.claude.com/en/docs/claude-code/skills) - Official
  Anthropic skills docs
- [Skills Announcement](https://www.anthropic.com/news/skills) - Claude Skills
  launch announcement
- [Engineering Deep Dive][skills-deep-dive] - Technical details

[skills-deep-dive]: https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills

### Official Repositories

- [anthropics/skills](https://github.com/anthropics/skills) - Official Anthropic
  skills repository
- [obra/superpowers](https://github.com/obra/superpowers) - Battle-tested core
  skills library (20+ skills)

### Related Awesome Lists

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) -
  Commands, workflows, and tools for Claude Code
- [awesome-claude](https://github.com/alvinunreal/awesome-claude) - General
  Claude resources

### Community Resources

- [Claude Skills Hub](https://claudeskills.info/) - Searchable skills directory
- [Simon Willison's Blog][simon-skills] - "Claude Skills are awesome, maybe a
  bigger deal than MCP"
- [Claudebin](https://claudebin.com)
  ([GitHub](https://github.com/wunderlabs-dev/claudebin.com/)) - A minimalistic
  tool for publishing and sharing Claude coding sessions

### Tools & Utilities

[simon-skills]: https://simonwillison.net/2025/Oct/16/claude-skills/

- [create-claude-skill](https://github.com/anthropics/skills) - Interactive
  skill creator
- [template-skill](https://github.com/anthropics/skills) - Minimal skill template

---

## Contributors

Thanks to these amazing people who have contributed to this list:

<!-- ALL-CONTRIBUTORS-LIST:START -->
This awesome list is maintained by the community. Want to see your name here? [Contribute!](#contributing)
<!-- ALL-CONTRIBUTORS-LIST:END -->

---

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for
detailed guidelines.

**Quick contribution checklist:**

- ✅ Skill has working `SKILL.md` with YAML frontmatter
- ✅ Clear documentation and use cases
- ✅ Actively maintained (commits within 6 months)
- ✅ Relevant to Claude workflows
- ✅ No security vulnerabilities or malicious code

**Ways to contribute:**

1. Add new skills to existing categories
2. Create entirely new categories
3. Improve skill descriptions
4. Add usage examples and tutorials
5. Report broken or outdated skills
6. Help verify community skills (earn the ✅ badge!)

---

## License

MIT License - see [LICENSE](LICENSE) file for details.

This awesome list is licensed under MIT. Individual skills maintain their own licenses.

---

## Acknowledgments

Special thanks to:

- **Anthropic** for creating Agent Skills and Claude Code
- **[@obra](https://github.com/obra)** for the incredible superpowers skills library
- **The Claude community** for continuous innovation and contributions

---

Found an outdated entry? [Report it](https://github.com/karanb192/awesome-claude-skills/issues/new/choose)
or read the [contribution guide](CONTRIBUTING.md) to propose a correction.

Maintained by [Karan Bansal](https://karanbansal.in) · [Blog][blog].

[blog]: https://karanbansal.in/blog/
