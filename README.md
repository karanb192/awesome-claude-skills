# ![Awesome Claude Skills](assets/header.svg)

Find a skill for the task at hand. A community directory for
[Claude Code](https://code.claude.com/docs/en/skills),
[Claude.ai and the API][anthropic-install].

**[Browse skills](#browse-skills)** · [Install your first skill](#quick-start) ·
[Collections](#skill-collections) · [Contribute](CONTRIBUTING.md)

<a id="featured-skills"></a>

## Pick a starting point

| Your next task | Try this |
| --- | --- |
| Extract tables from a PDF | [pdf][pdf] |
| Find why a test keeps failing | [systematic-debugging][debugging] |
| Build a feature with tests first | [test-driven-development][tdd] |
| Create a Word document | [docx][docx] |
| Turn a repeated task into a skill | [skill-creator][creator] |

## Browse skills

| Code | Create | Work |
| --- | --- | --- |
| [Testing](#testing--quality) | [Files](#document--file-processing) | [Workflow](#collaboration--workflow) |
| [Debugging](#debugging--troubleshooting) | [Media](#media--content-creation) | [Data](#data--analysis) |
| [Build apps](#development--architecture) | [Writing](#writing--research) | [Finance & tax](#finance--tax) |
| [Security](#security--performance) | [Skills](#meta-skills) | [Automation](#documentation--automation) |

Skill names link to their source. Read the install guide there before enabling
a skill. Inclusion is not a security audit. Use **Cmd+F** or **Ctrl+F** to search.

<a id="skill-categories"></a>
<a id="-document--file-processing"></a>

### Document & File Processing

| Skill | Use it to |
| --- | --- |
| [cue-omni-reader](https://github.com/sensedeal/cue-skills/tree/main/cue-omni-reader) | Parse documents and web sources into text through the Cue Omni Reader MCP service. |
| [docx][docx] | Create and edit Word documents with tracked changes and comments. |
| [equalang](https://github.com/equalang/equalang-skill) | Translate files or transcribe recordings through Equalang using an API key and credits. |
| [humanpen](https://github.com/humanpen/humanpen-skill) | Rewrite, translate, shorten, and restyle citations in files through paid HumanPen APIs. |
| [pdf][pdf] | Extract text and tables, combine PDFs, and fill forms. |
| [pptx][pptx] | Create, edit, and inspect PowerPoint presentations. |
| [translate-book](https://github.com/kcy4334-lgtm/translate-book-arxiv) | Translate papers and books with a LaTeX-source route for preserving arXiv equations and tables. |
| [xlsx][xlsx] | Build and edit spreadsheets with formulas and formatting. |

<a id="-testing--quality"></a>

### Testing & Quality

| Skill | Use it to |
| --- | --- |
| [agent-qa-authoring](https://github.com/vostride/agent-qa/tree/main/skills/agent-qa-authoring) | Author and validate agent-qa tests and IDs; source license restricts competing use. |
| [checkup](https://github.com/agentvitals/checkup/tree/main/checkup) | Run hosted probes and retrieve server-scored results; full mode uploads approved conversation logs. |
| [crosscheck](https://github.com/moveju112/skill_verify/tree/main/skills/crosscheck) | Compare independent Claude and Codex analysis, reconcile findings, and verify completed work. |
| [design-fidelity-verify](https://github.com/jeltehomminga/figma-design-skills/tree/main/skills/design-fidelity-verify) | Compare measured values in a running app with a Figma design specification. |
| [ironloop](https://github.com/edouard-claude/ironloop/tree/main/skills/engineering/ironloop) | Plan Rust work through specifications, tests, simulation, and authorized security checks. |
| [never-again](https://github.com/malaysherasia-ai/claude-never-again/tree/main/skills/never-again) | Capture repaired bugs as enforceable hooks or brief lessons for future sessions. |
| [sim (interview-sim)](https://github.com/chrisjacksonn/interview-sim/tree/main/skills/sim) | Practice timed coding interviews with script-managed clocks and hidden-test grading. |
| [test-checklist](https://github.com/Ifeanyiejindu/qarunbook/tree/main/plugins/qarunbook/skills/test-checklist) | Derive a QA plan from app code with steps and expected results for each platform. |
| [test-driven-development][tdd] | Write a failing test, implement the change, then refactor. |
| [webapp-testing][webapp-testing] | Exercise a local web app with Playwright and inspect its behavior. |
| [what-could-break](https://github.com/stas4000/what-could-break/tree/main/what-could-break) | Trace a change through consumers, stored data and duplicated rules, then design a concrete check for the critical assumption. |

<a id="-debugging--troubleshooting"></a>

### Debugging & Troubleshooting

| Skill | Use it to |
| --- | --- |
| [agenttrace-session-audit](https://github.com/luoyuctl/agenttrace) | Inspect agent sessions for cost, tokens, failures, and latency. |
| [systematic-debugging][debugging] | Investigate a bug's cause before attempting a fix. |
| [verification-before-completion][verification] | Run checks and inspect their output before calling work done. |

<a id="-collaboration--workflow"></a>

### Collaboration & Workflow

| Skill | Use it to |
| --- | --- |
| [a2ui-ask](https://github.com/YuniqueUnic/a2ui-ask) | Collect structured user input through a browser form and JSON answer files. |
| [ai-meeting](https://github.com/bin1874/ai-meeting-skill/tree/main/ai-meeting) | Run structured proposal reviews with CLI agents and preserve each agent session between rounds. |
| [ax-extract-workflow](https://github.com/Necmttn/ax) | Reconstruct a shipped feature's workflow from local ax session history. |
| [brainstorming][brainstorming] | Work through requirements and design choices before implementation. |
| [breather](https://github.com/ilandahan/breather/tree/main/skills/breather) | Offer session stopping points with attended-time context and a written handoff. |
| [clueless](https://github.com/ADanMan/clueless/tree/main/skills/clueless) | Name assumptions, irreversible steps, and review gaps when a user needs extra guidance. |
| [communication-protocol-setup](https://github.com/cez0060405/communication-protocol-setup) | Agree on assistant communication preferences and export a reusable protocol. |
| [delegate](https://github.com/aayushpokhrel1/delegation-pipeline/tree/master/skills/delegate) | Delegate a precisely specified coding task to a worker, then review its diff and tests. |
| [dialog-tree](https://github.com/ikotelkin/claude-skills/tree/main/skills/dialog-tree) | Track conversation branches in an interactive dialogue tree. |
| [executing-plans][executing-plans] | Carry out an implementation plan with review checkpoints. |
| [fabling](https://github.com/gncdev/fabling/tree/main/fabling) | Apply a work profile for proportionate investigation, visual checks, and task completion. |
| [finishing-a-development-branch][finishing] | Decide how to integrate finished work and clean up the branch. |
| [guashuai / junshi](https://github.com/DENGYUFAN0/guashuai-junshi/tree/main/adapters/claude-code/skills) | Coordinate model tiers with either an orchestrator or an occasional expert advisor. |
| [kgai knowledge-graph](https://github.com/kgaidev/kgai) | Capture project decisions and domain knowledge in a linked graph through the kgai CLI. |
| [mindpalace](https://github.com/aashutosh396/mindpalace-skill) | Organize a local knowledge vault around resources, project pointers, logs, and runbooks. |
| [OrcaReplay](https://github.com/Continuum-AI-Corp/OrcaReplay) | Inspect recorded agent runs and replay or fork them through Orca MCP. |
| [orchestrating-subagents](https://github.com/PapiScholz/symphony/tree/main/skills/orchestrating-subagents) | Choose model tiers for delegated work and review dispatch cost and duration. |
| [planning-with-files](https://github.com/OthmanAdi/planning-with-files/tree/master/skills/planning-with-files) | Persist plans, findings, and progress across long tasks and context resets. |
| [pr-review](https://github.com/priyank766/OpenSource-SKILL) | Filter a pull request review down to actionable findings. |
| [punchcard](https://github.com/Maksim-Burtsev/punchcard/tree/master/skills/punchcard) | Review a code change for module boundaries, dependencies, data models, and error paths. |
| [receiving-code-review][receiving-review] | Evaluate review feedback and work through requested changes. |
| [requesting-code-review][requesting-review] | Request a review before work proceeds or merges. |
| [shipreel](https://github.com/theBstar/shipreel/tree/main/plugins/shipreel/skills/shipreel) | Render a narrated PR walkthrough with diagrams, code panels, and optional app recordings. |
| [simple-man](https://github.com/Maksim-Burtsev/simple-man/tree/master/skills/simple-man) | Shorten agent replies while preserving findings, fixes, checks, and required facts. |
| [slop-post](https://github.com/useslop/claude-plugins/tree/main/plugins/slop/skills/slop-post) | Create a private Slop draft from a session with a receipt of model, tools, and commits. |
| [tlgr](https://github.com/tlgrcli/tlgr/tree/main/plugin/skills/tlgr) | Read, search, and manage a personal Telegram account through a JSON CLI. |
| [using-git-worktrees][worktrees] | Work in isolated checkouts for separate development tasks. |
| [using-lwc](https://github.com/JanYork/llm-wiki-cli/tree/main/skills/using-lwc) | Recall and preserve source-grounded project knowledge with LWC wiki and graph tools. |
| [workflow-design](https://github.com/ghorbanies/workflow-design) | Model workflow states, test guards, analyze transition logs, and plan safe flow changes. |
| [working-memory](https://github.com/ikotelkin/claude-skills/tree/main/skills/working-memory) | Preserve a bounded work checkpoint across context compaction. |
| [writing-plans][writing-plans] | Break a specification into implementation steps. |

<a id="️-development--architecture"></a>

### Development & Architecture

| Skill | Use it to |
| --- | --- |
| [anti-slop-design](https://github.com/wwewtech/anti-slop-design/tree/main/skills/anti-slop-design) | Review and refine UI typography, color tokens, interactions, and accessibility. |
| [birdview](https://github.com/Qiuner/birdview) | Map architecture, constraints, and planned changes back to source evidence. |
| [build-with-better-design](https://github.com/better-designs/better-design-plugin/tree/main/skills/build-with-better-design) | Select and install a design system through the Better Design MCP service. |
| [cohesivity](https://github.com/cohesivity-org/cohesivity-plugin/tree/main/packages/claude/skills/cohesivity) | Provision and manage application backend services through Cohesivity APIs and MCP. |
| [dropthehassle-publish](https://github.com/bosmdavid-gif/dropthehassle-skill/tree/main/skills/dropthehassle-publish) | Publish built static sites through DropTheHassle and connect an existing backend. |
| [easy-auto-research](https://github.com/wjc2830/Easy-AutoResearch-for-DeepLearning/tree/main/easy-auto-research) | Run a supervised deep-learning experiment loop with versioned code and persistent progress. |
| [enterprise-architect](https://github.com/rafalr100/enterprise-architect-skill/tree/main/skills/enterprise-architect) | Plan target architectures, capability maps, decision records, and technology roadmaps. |
| [erupt-admin](https://github.com/plinian/erupt-skill) | Scaffold a Java admin app with the erupt framework, H2, CRUD, and permission models. |
| [figma-design-extract](https://github.com/jeltehomminga/figma-design-skills/tree/main/skills/figma-design-extract) | Extract Figma values into a design specification mapped to the project tokens. |
| [keyboard-shortcuts](https://github.com/nparashar150/claude-keyboard-shortcuts/tree/main/skills/keyboard-shortcuts) | Audit and implement web-app shortcuts, command palettes, and keyboard help. |
| [mcp-builder][mcp-builder] | Build Model Context Protocol servers that connect tools and APIs to Claude. |
| [pit-stop](https://github.com/Finn763/pit-stop) | Find a small repository maintenance fix, support it with evidence, and review the patch. |
| [regulex-plus](https://github.com/PipeDream941/regulex-plus) | Render JavaScript regular expressions as SVG, PNG, or Mermaid diagrams through a CLI. |
| [tastegate](https://github.com/stas4000/tastegate/tree/main/tastegate) | Build a frontend from a design brief, then check layout, contrast and other visible defects with a bundled Playwright browser gate. |
| [tree-ring-memory](https://github.com/TerminallyLazy/tree-ring-memory-skill) | Recall, capture, audit, and forget durable project memory through Tree Ring Memory. |
| [unflat](https://github.com/merturl4576/unflat) | Add visual depth to web marketing pages through a bounded CSS treatment. |
| [web-artifacts-builder][artifacts] | Build web artifacts with React, Tailwind CSS, and shadcn/ui. |

<a id="-security--performance"></a>

### Security & Performance

| Skill | Use it to |
| --- | --- |
| [awesome-bug-bounty](https://github.com/YangTech-gh/Awesome-Bug-Bounty/tree/main/skills/awesome-bug-bounty) | Plan authorized bug-bounty research with scope checks, vulnerability guides, and report templates. |
| [claude-security-skills](https://github.com/NovaCode37/claude-security-skills) | Check secrets, Python code, dependencies, containers, JWTs, CORS, and HTTP headers. |
| [deep-security-audit](https://github.com/ravindrakele/claude-skills/tree/main/plugins/deep-security-audit/skills/deep-security-audit) | Map code attack surfaces and review candidate vulnerabilities with independent verification. |
| [gedik](https://github.com/onur-kesim/gedik/tree/main/skills/gedik) | Audit authorized project surfaces and attach reproducible evidence to security findings. |
| [SecHelix](https://github.com/omarmohelal/SecHelix/tree/main/skills/sechelix) | Review authorized local code for security issues with evidence and a refutation pass. |
| [wp-security-audit](https://github.com/mwstech/wp-security-audit-skill) | Audit WordPress configuration, plugin vulnerabilities, and indicators of compromise. |

<a id="-documentation--automation"></a>

### Documentation & Automation

| Skill | Use it to |
| --- | --- |
| [famulor-assistants-history](https://github.com/bekservice/Famulor-Skill/tree/main/claude-store/skills/famulor-assistants-history) | Read Famulor assistant settings and interaction history through its restricted MCP profile. |
| [linkedin-outreach](https://github.com/vanshyadav1408/Omentir/tree/main/plugins/omentir/skills/linkedin-outreach) | Research prospects, draft outreach, and inspect campaigns through Omentir MCP. |
| [okf](https://github.com/mattjoyce/okf-skill/tree/master/skills/okf) | Author and validate Open Knowledge Format bundles of linked Markdown concept files. |
| [process-builder](https://github.com/Castaldo-Solutions/process-builder) | Turn a process interview into a BPMN swimlane diagram in a .drawio file. |
| [project-planning-journaling](https://github.com/mh-mansouri/Project-Planning-Journaling/tree/main/project-planning-journaling) | Scope a project and maintain a resumable journal of decisions, progress, and open work. |

<a id="-media--content-creation"></a>

### Media & Content Creation

| Skill | Use it to |
| --- | --- |
| [3d-logo](https://github.com/hasuwini77/3d-logo-skill/tree/main/skills/3d-logo) | Build a rotating 3D logo component with React Three Fiber. |
| [algorithmic-art][algorithmic-art] | Create generative art with p5.js. |
| [bria-ai](https://github.com/Bria-AI/bria-skill/tree/dev/skills/bria-ai) | Generate and edit images or remove backgrounds through the Bria API. |
| [canvas-design][canvas-design] | Create visual designs as PNG and PDF files. |
| [film-crew](https://github.com/HEOJUNFO/ai-film-crew/tree/master/skills/film-crew) | Plan AI-video shots and write prompts with camera, lighting, and continuity guidance. |
| [harmonic-mixing](https://github.com/songfinder-dev/songfinder-skills/tree/main/skills/harmonic-mixing) | Look up tempo and musical key to plan playlists and DJ transitions. |
| [identify-song](https://github.com/songfinder-dev/songfinder-skills/tree/main/skills/identify-song) | Identify a track from a link or audio file through Song Finder. |
| [kavel-image](https://github.com/hanshs474/kavel-image-skill) | Generate images through Kavel's anonymous submit-and-poll API within its free allowance; photo edits require a Kavel API key. |
| [meshy-pose-rigging](https://github.com/rickyworld/rigmeshy-by-ricky/tree/master/meshy-pose-rigging) | Prepare character references and work through Meshy auto-rigging and export troubleshooting. |
| [publishport](https://github.com/karuha-m/publishport-skill/tree/main/skills/publishport) | Publish and cross-post through connected accounts in the user's PublishPort browser app. |
| [ruxi-skill](https://github.com/swaylq/ruxi-skill) | Build a single-file visual novel from selected book scenes with source-linked choices. |
| [screenbrowser](https://github.com/screenbrowser/skill/tree/main/skills/screenbrowser) | Produce narrated web-app tutorials through the Screen Browser MCP service. |
| [seedance-25-prompting](https://github.com/gbeyrouti/seedance-prompting-claude-skill/tree/main/seedance-25-prompting) | Write and troubleshoot Seedance video prompts, reference roles, audio, and shot timing. |
| [slack-gif-creator][slack-gif-creator] | Make animated GIFs sized for Slack. |
| [table-sheet](https://github.com/netmobster/unstuck-games/tree/main/plugins/table-sheet) | Turn a D&D Beyond character sheet into a play guide and pre-session checklist. |

<a id="-data--analysis"></a>

### Data & Analysis

| Skill | Use it to |
| --- | --- |
| [apify-remote-startup-jobs](https://github.com/johnisanerd/claude-skill-remote-startup-jobs/tree/main/apify-remote-startup-jobs) | Fetch structured remote startup job listings through a paid Apify actor. |
| [apify-yc-startup-jobs](https://github.com/johnisanerd/claude-skill-yc-startup-jobs/tree/main/apify-yc-startup-jobs) | Compare published startup salary and equity ranges through a paid Apify actor. |
| [apitube-news-api](https://github.com/apitube/news-api-skills/tree/main/skills/apitube-news-api) | Search and filter news through APITube, with API authentication, pagination, and error handling. |
| [claude-ecom](https://github.com/takechanman1228/claude-ecom) | Review ecommerce order CSVs for revenue, retention, and margin patterns. |
| [converly](https://github.com/converlyio/converly-agent) | Configure Converly conversion flows and inspect test events and delivered conversions. |
| [invoice-winning-numbers](https://github.com/tahodev/baodao-skill/tree/main/invoice-winning-numbers) | Look up Taiwan invoice winning numbers by period from official sources. |
| [polymarket-tennis](https://github.com/livetennisapi/polymarket-tennis/tree/main/skills/polymarket-tennis) | Build an observe-only tennis market watcher joining market prices to live match scores. |
| [pvr-inox-radar](https://github.com/karanb192/pvr-inox-radar/tree/main/skills/pvr-inox-radar) | Map PVR INOX showtimes in India with seats-together counts and travel-time estimates. |

<a id="-finance--tax"></a>

### Finance & Tax

| Skill | Use it to |
| --- | --- |
| [file-itr](https://github.com/shivprime94/file-itr) | Follow a guided walkthrough of India's income-tax filing portal. |
| [furusato-nozei](https://github.com/tahodev/kurashi-skill/tree/main/furusato-nozei) | Estimate Japan's hometown-tax donation cap with stated assumptions and official sources. |
| [itr-wala](https://github.com/karanb192/itr-wala) | Prepare Indian income-tax returns using document extraction and Python calculations. |
| [simmer-tennis-live-gate](https://github.com/livetennisapi/simmer-tennis-live-gate) | Gate simulated tennis market entries on live match state without placing orders. |
| [stipend](https://github.com/stipend-sh/stipend) | Manage a self-custodied USDC wallet and x402 payments with configurable spending policies. |
| [verify-polish-company](https://github.com/bartosz-kuc/skanfirmy-mcp/tree/main/skill) | Look up Polish company registrations, VAT status, bank accounts, and EU VAT numbers. |

<a id="️-writing--research"></a>

### Writing & Research

| Skill | Use it to |
| --- | --- |
| [ai-tell-detector](https://github.com/aragossa/ai-tell-detector/tree/main/en/ai-tell-detector) | Audit English or Russian drafts for generic writing patterns and suggest precise edits. |
| [brand-guidelines][brand-guidelines] | Apply Anthropic's brand colors and typography to artifacts. |
| [business-name-fit](https://github.com/Elham-Farajnejad/business-name-fit) | Assess a business name across cultures, languages, and target markets. |
| [goethecoach](https://github.com/janosszaboaipm-design/goethecoach-claude-skill/tree/main/goethecoach) | Practise Goethe exam writing, reading, and speaking with rubric-based feedback. |
| [grill](https://github.com/mtangoz/grill/tree/main/skills/grill) | Challenge a decision with an outside model and name tests that could settle the doubts. |
| [grounded](https://github.com/jostelzer/grounded/tree/main/skills/grounded) | Draft scientific literature reviews with live source discovery and citation checks. |
| [humanize-chinese](https://github.com/swaylq/humanize-chinese) | Edit Chinese prose with rewriting, phrase cleanup, and local checks; non-commercial license. |
| [humanize-pro](https://github.com/msdanyg/humanize-pro) | Rewrite or audit prose against a saved voice profile and publishing-channel rules. |
| [humanizer-ru](https://github.com/ilyautov/humanizer-ru) | Edit Russian prose for its audience while preserving facts, voice, and protected text. |
| [humanizing-writing](https://github.com/AshwinSathian/humanize-writing-skill) | Edit prose for generic structure, filler, weak claims, and repeated writing patterns. |
| [internal-comms][internal-comms] | Draft updates, newsletters, and other internal communications. |
| [publora-post-ideas](https://github.com/publora-team/publora-post-ideas/tree/main/skills/publora-post-ideas) | Choose among three social-post angles, then draft the one the user selects. |
| [reading-analysis](https://github.com/shenquan520/reading-analysis) | Analyse English exam passages, answer choices, and recurring errors. Noncommercial license. |
| [sales-framework](https://github.com/KudoMetrics-Techologies-Private-Limited/sales-framework/tree/main/skills/sales-framework) | Review sales copy, pitches, and objections against a published persuasion framework. |
| [Say it plainly](https://github.com/adjustleads/provenskills-free-packs/tree/main/plain-writing/say-it-plainly) | Rewrite prose for a reader without changing its claims. Noncommercial license. |
| [structured-gist](https://github.com/domattioli/structured-gist/tree/main/skills/structured-gist) | Format explanations and process recaps as nested outlines for skimming. |
| [tldr](https://github.com/SurefireStudios/tldr/tree/main/skills/tldr) | Lead with a short summary while preserving full details and critical caveats. |
| [zh-tw-humanizer](https://github.com/acchuang/zh-tw-humanizer) | Edit Traditional Chinese prose with Taiwan terminology and protected-fact rules. |

<a id="-meta-skills"></a>

### Meta Skills

| Skill | Use it to |
| --- | --- |
| [danshari-skill](https://github.com/swaylq/danshari-skill) | Audit installed skills and archive redundant ones after user approval, with a restore path. |
| [prime-worker](https://github.com/alperiox/prime-worker) | Delegate multi-turn tasks to persistent local prime-agent worker sessions. |
| [reap (skillreaper)](https://github.com/thousandflowers/skillreaper/tree/main/plugins/skillreaper/skills/reap) | Measure unused loaded context from local agent transcripts and review reversible cleanup. |
| [rule-architect](https://github.com/moveju112/rule-architect) | Generate modular project rules with a shared index and runtime-specific entrypoints. |
| [sijiao-skill](https://github.com/swaylq/sijiao-skill) | Build a stateful learning tutor with researched lessons, exercises, and spaced review. |
| [skill-creator][creator] | Create skills, evaluate them, and refine their descriptions. |
| [skill-tuner](https://github.com/DENGYUFAN0/skill-forge/tree/main/skill-tuner) | Refine an installed skill through a small baseline, focused edits, and a rollback decision. |
| [subagent-driven-development][subagents] | Implement a plan through delegated tasks and review steps. |
| [template-skill][template] | Start a skill from a minimal `SKILL.md` template. |
| [whetstone](https://github.com/TbusOS/whetstone) | Distil session lessons into reviewable skill proposals with evidence and duplication checks. |
| [writing-skills][writing-skills] | Write and test skill instructions before distributing them. |

[Back to categories ↑](#browse-skills)

## Skill Collections

Browse these repositories when you want a related set of skills.

| Collection | Focus |
| --- | --- |
| [Anthropic skills](https://github.com/anthropics/skills) | Document processing, design, development, and skill examples. |
| [Superpowers](https://github.com/obra/superpowers) | Planning, testing, debugging, and development workflows. |
| [Affiliate Skills](https://github.com/Affitor/affiliate-skills) | Affiliate research, content, distribution, and analytics. |
| [Agent Skills English Productivity Pack](https://github.com/alapha888/agent-skills-en) | Meeting notes, proofreading, research, code review, and commit messages. |
| [agent-pilot-skills](https://github.com/babyGao/agent-pilot-skills) | Cross-model review, parallel research, outbound sales, illustrations, and Chinese-platform workflows. |
| [AI sales skills](https://github.com/Marchenko-sales/ai-sales-skills) | Company research, sales qualification, and business outreach workflows in Russian. |
| [Baodao skills](https://github.com/tahodev/baodao-skill) | Taiwan public-service lookups for invoices, weather, alerts, transit, and public data. |
| [ChatCrystal](https://github.com/ZengLiangYi/ChatCrystal/tree/main/skills) | Local memory recall and writeback for coding sessions. |
| [Chisanan232/requirement-zero](https://github.com/Chisanan232/requirement-zero) | Review requirement necessity and audit whether existing code still earns its upkeep. |
| [claude-fable-5-skills](https://github.com/kpab/claude-fable-5-skills) | Effort calibration, scope control, and subagent orchestration. |
| [dbhq-uk/marketplace](https://github.com/dbhq-uk/marketplace) | Remote diagnostics, code search, repository checks, research, writing, and work-service integrations. |
| [DurdeuVlad/persona-write](https://github.com/DurdeuVlad/persona-write) | Persona-based drafting, rewriting, sample-based voice extraction, and independent review. |
| [E-commerce skills](https://github.com/mardab96/ecommerce-claude-skills) | Review checkout, product content, margin, inventory, retention, and disputes from store data. |
| [Growth Cab GTM Skills](https://github.com/federicodon/growthcab-gtm-skills) | Sending-domain checks, cold-email grading, lead-list QA, and meeting benchmarks. |
| [iOS agents and skills](https://github.com/apexbymanish/claude-ai-agents-ios) | Swift/iOS implementation, testing, accessibility, performance, security, and release checks. |
| [Kudosity skills](https://github.com/kudosity/skills) | SMS, MMS, WhatsApp, RCS, contact lists, and delivery webhooks through Kudosity. |
| [Kurashi skills](https://github.com/tahodev/kurashi-skill) | Japan public-service lookups for weather, alerts, holidays, taxes, and libraries. |
| [leechen298/Code2Skill](https://github.com/leechen298/Code2Skill) | Extract source-based agent tools and independently review generated workflow and source fidelity. |
| [Lesile-Yin/agent-skills](https://github.com/Lesile-Yin/agent-skills) | Prompt engineering, multi-lens reviews, token budgets, and batch PowerPoint automation. |
| [Mamba Labs Skills](https://github.com/mambalabsdev/mamba-labs-skills) | Prospect research, CRM operations, email deliverability, and go-to-market workflows; some use Apify. |
| [Marketing Skills](https://github.com/coreyhaines31/marketingskills) | SEO, copywriting, email, pricing, advertising, and analytics. |
| [mblode/agent-skills](https://github.com/mblode/agent-skills) | UI, typography, developer experience, documentation, review, and release workflows. |
| [minxnnu-cloud/make-new-things](https://github.com/minxnnu-cloud/make-new-things) | Claude/Codex visual handoffs, representative frame approval, rework limits, and skill-tree sync. |
| [noizai/skills](https://github.com/noizai/skills) | Text-to-speech dubbing and companion voice presets. |
| [Novu skills](https://github.com/novuhq/skills) | Build Novu notification workflows, inboxes, preferences, and hosted agent channels. |
| [suede-creator-skills](https://github.com/JasonColapietro/suede-creator-skills) | Code quality, design, marketing, and shipping. |
| [superseo-skills](https://github.com/inhouseseo/superseo-skills) | SEO audits, content writing, and link building. |
| [YYLO skills](https://github.com/yylo-dev/yylo-skills) | Manage tasks, artifacts, benchmarks, and durable work records through the YYLO CLI. |

<a id="how-to-install-skills"></a>

## Quick Start

Install Anthropic's document skills in Claude Code from your terminal.

```bash
claude plugin marketplace add anthropics/skills
claude plugin install document-skills@anthropic-agent-skills
```

Provide a PDF, then ask Claude to extract its form fields. Compare the result
with your file. [Read Anthropic's installation guide][anthropic-install].

<details>
<summary><strong>Other collections, standalone skills, and updates</strong></summary>

Use each source repository's install guide. Collections may ship as plugins,
individual folders, or both. Choose one route for each collection.

For a standalone Claude Code skill, put its folder in
`~/.claude/skills/<skill-name>/` for personal use, or
`.claude/skills/<skill-name>/` for one project. Keep `SKILL.md` and its supporting
files together. See the [Claude Code skill guide][skill-guide].

Follow the [plugin update guide][plugin-updates] for plugin installs.
For standalone folders, use the source repository's update instructions.
Cloning this directory does not install the listed skills.

</details>

## FAQ

<a id="what-are-skills"></a>

<details>
<summary><strong>What is a skill?</strong></summary>

A skill is a folder containing instructions in `SKILL.md`, with optional
scripts and resources. Claude loads it when relevant to a task, or you can
invoke it directly. See the [skill guide][skill-guide].

</details>

<details>
<summary><strong>Does every skill work in every Claude app?</strong></summary>

The format is shared, but tools and installation differ by host. A Claude Code
plugin does not install itself in Claude.ai or the API. Check the source's
supported environments and [Anthropic's separate install routes][anthropic-install].

</details>

<a id="skills-vs-mcp-vs-system-prompts"></a>

<details>
<summary><strong>Skills, MCP, or project instructions?</strong></summary>

| You need | Use |
| --- | --- |
| A repeatable task or workflow | [Skills][skill-guide] |
| Access to an external service or tool | [Model Context Protocol (MCP)][mcp-guide] |
| Conventions Claude reads for a project | [Project instructions][memory-guide] |

</details>

<details>
<summary><strong>Are the listed skills tested or audited?</strong></summary>

This is a community directory, not a certification program. Read the source
instructions and scripts, then try the skill on a task whose result you can
check. Report broken links or incorrect descriptions through [issues][suggest].

</details>

<details>
<summary><strong>Can I create or contribute a skill?</strong></summary>

Start with [skill-creator][creator] or the [template][template]. To add a
listing, follow the [contribution guide](CONTRIBUTING.md).

</details>

## Skill ideas

These are requests for contributions, not skills you can install.
Know an implementation? [Suggest its source][suggest].

<details>
<summary><strong>Browse ideas by category</strong></summary>

| Category | Ideas awaiting a source |
| --- | --- |
| Testing | e2e-testing-skill, snapshot-testing |
| Debugging | performance-profiling |
| Development | api-development, database-migration, refactoring-patterns |
| Security & performance | security-review, dependency-audit, performance-optimization, load-testing |
| Documentation | documentation-generator, changelog-automation, ci-cd-integration |
| Media | video-editing-helper |
| Data | data-visualization, sql-query-builder, csv-processing |
| Writing | research-assistant, technical-writing |

</details>

<details>
<summary><strong>Looking for an entry from an older version of this list?</strong></summary>

Some entries now live inside other skills or use a different name.

| Earlier entry | Current source |
| --- | --- |
| artifacts-builder | [web-artifacts-builder][artifacts] |
| condition-based-waiting | [Supporting guide in systematic-debugging][waiting] |
| defense-in-depth | [Supporting guide in systematic-debugging][defense] |
| root-cause-tracing | [Supporting guide in systematic-debugging][tracing] |
| testing-skills-with-subagents | [Supporting guide in writing-skills][testing-skills] |
| testing-anti-patterns, sharing-skills | No standalone skill found in the [current Superpowers catalog][superpowers-catalog]. |

</details>

## Resources

- [Claude Code skill guide][skill-guide]
- [Agent Skills specification](https://agentskills.io/specification)
- [How Anthropic designed Skills][skills-deep-dive]
- [Skills announcement](https://www.anthropic.com/news/skills)
- [Simon Willison on Claude Skills][simon-skills]
- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude](https://github.com/alvinunreal/awesome-claude)
- [Claude Skills Hub](https://claudeskills.info/)
- [Claudebin](https://claudebin.com) and its
  [source](https://github.com/wunderlabs-dev/claudebin.com/)
- [AgentHub](https://myagenthub.cn): offers a Chinese-language directory of MCP
  servers and agent skills.
- [Hypit video guide](https://hypit.video/guides/how-to-clone-a-video/): walks
  through planning and rendering a video from a reference format.
-
  [awesome-claude-code-hooks](https://github.com/loqimean/awesome-claude-code-hooks):
  Related directory of Claude Code hook workflows.
- [500k.io Skills Bank](https://500k.io/skills): Related directory of skills,
  MCP servers, GPTs, and agent tools.
- [PolySkill](https://polyskill.ai): Skill registry and CLI with [public
  source](https://github.com/MrSpacemann/polyskill).

<a id="contributors"></a>

## Contributing

Add a skill, fix a link, or improve a description. Read the
[contribution guide](CONTRIBUTING.md), then open a pull request.

Built with contributions from the [community][contributors], including skills
from [Anthropic](https://github.com/anthropics/skills) and
[obra](https://github.com/obra/superpowers).
Maintained by [Karan Bansal](https://karanbansal.in) · [Blog][blog].

## License

[MIT](LICENSE) covers this directory. Each listed skill has its own license.

[pdf]: https://github.com/anthropics/skills/tree/main/skills/pdf
[docx]: https://github.com/anthropics/skills/tree/main/skills/docx
[pptx]: https://github.com/anthropics/skills/tree/main/skills/pptx
[xlsx]: https://github.com/anthropics/skills/tree/main/skills/xlsx
[webapp-testing]: https://github.com/anthropics/skills/tree/main/skills/webapp-testing
[mcp-builder]: https://github.com/anthropics/skills/tree/main/skills/mcp-builder
[artifacts]: https://github.com/anthropics/skills/tree/main/skills/web-artifacts-builder
[algorithmic-art]: https://github.com/anthropics/skills/tree/main/skills/algorithmic-art
[canvas-design]: https://github.com/anthropics/skills/tree/main/skills/canvas-design
[slack-gif-creator]: https://github.com/anthropics/skills/tree/main/skills/slack-gif-creator
[brand-guidelines]: https://github.com/anthropics/skills/tree/main/skills/brand-guidelines
[internal-comms]: https://github.com/anthropics/skills/tree/main/skills/internal-comms
[creator]: https://github.com/anthropics/skills/tree/main/skills/skill-creator
[template]: https://github.com/anthropics/skills/tree/main/template
[tdd]: https://github.com/obra/superpowers/tree/main/skills/test-driven-development
[debugging]: https://github.com/obra/superpowers/tree/main/skills/systematic-debugging
[verification]: https://github.com/obra/superpowers/tree/main/skills/verification-before-completion
[brainstorming]: https://github.com/obra/superpowers/tree/main/skills/brainstorming
[executing-plans]: https://github.com/obra/superpowers/tree/main/skills/executing-plans
[finishing]: https://github.com/obra/superpowers/tree/main/skills/finishing-a-development-branch
[receiving-review]: https://github.com/obra/superpowers/tree/main/skills/receiving-code-review
[requesting-review]: https://github.com/obra/superpowers/tree/main/skills/requesting-code-review
[worktrees]: https://github.com/obra/superpowers/tree/main/skills/using-git-worktrees
[writing-plans]: https://github.com/obra/superpowers/tree/main/skills/writing-plans
[subagents]: https://github.com/obra/superpowers/tree/main/skills/subagent-driven-development
[writing-skills]: https://github.com/obra/superpowers/tree/main/skills/writing-skills
[waiting]: https://raw.githubusercontent.com/obra/superpowers/main/skills/systematic-debugging/condition-based-waiting.md
[defense]: https://raw.githubusercontent.com/obra/superpowers/main/skills/systematic-debugging/defense-in-depth.md
[tracing]: https://raw.githubusercontent.com/obra/superpowers/main/skills/systematic-debugging/root-cause-tracing.md
[testing-skills]: https://raw.githubusercontent.com/obra/superpowers/main/skills/writing-skills/testing-skills-with-subagents.md
[superpowers-catalog]: https://github.com/obra/superpowers/tree/main/skills
[anthropic-install]: https://github.com/anthropics/skills#try-in-claude-code-claudeai-and-the-api
[skill-guide]: https://code.claude.com/docs/en/skills
[plugin-updates]: https://code.claude.com/docs/en/discover-plugins#keep-plugins-updated
[mcp-guide]: https://code.claude.com/docs/en/mcp
[memory-guide]: https://code.claude.com/docs/en/memory
[skills-deep-dive]: https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills
[simon-skills]: https://simonwillison.net/2025/Oct/16/claude-skills/
[suggest]: https://github.com/karanb192/awesome-claude-skills/issues/new/choose
[contributors]: https://github.com/karanb192/awesome-claude-skills/graphs/contributors
[blog]: https://karanbansal.in/blog/
