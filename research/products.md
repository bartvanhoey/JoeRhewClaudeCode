# Anthropic Product Lineup — Research Notes

**Research date:** 2026-06-20
**Method:** WebSearch + WebFetch against anthropic.com, claude.com, docs.anthropic.com / platform.claude.com, code.claude.com, plus press coverage (CNBC, CNN, Bloomberg, TechCrunch, Cybersecurity Dive, MarkTechPost) for context not yet reflected on owned properties.

> **IMPORTANT CALIBRATION NOTE:** The assistant's model training cutoff is August 2025, but the current date is June 2026, so roughly 10 months of product history below comes entirely from live web research rather than prior knowledge. Some of what follows (the "Mythos" model tier, "Claude Fable 5," Project Glasswing, a government order suspending access to those models) sounded implausible at first pass and was cross-checked against multiple independent, reputable sources (Anthropic's own news page, CNBC, CNN, Bloomberg, TechCrunch) before being included — it appears to be real and current, not hallucination. Still, flag anything below to a human fact-checker before using it in a customer-facing GTM asset, especially the most recent items (last 4-6 weeks), since fast-moving stories sometimes get details revised.

---

## 1. The Claude Model Family

### Naming/tier structure
Three perennial size tiers — **Haiku** (fastest/cheapest), **Sonnet** (balanced speed/intelligence), **Opus** (most capable, highest cost) — were introduced together with Claude 3 in March 2024 and have persisted since. As of June 2026, a fourth, higher tier called **Mythos-class** sits above Opus, currently represented by two models: Claude Fable 5 (generally available) and Claude Mythos 5 (limited-access, invitation-only). (https://platform.claude.com/docs/en/docs/about-claude/models/overview)

### Version history (chronological)
- **Claude (original)** — Mar 14, 2023. Limited release to selected users. (https://en.wikipedia.org/wiki/Claude_(language_model))
- **Claude 2** — Jul 11, 2023. First version broadly available to the public; improved reasoning/coding and API access. (https://en.wikipedia.org/wiki/Claude_(language_model))
- **Claude Instant 1.2** — Aug 9, 2023. Lower-cost/lower-latency variant. (https://en.wikipedia.org/wiki/Claude_(language_model))
- **Claude 2.1** — Nov 21, 2023. Doubled context window to **200,000 tokens** (~500 pages); added system prompts and early tool use, aimed at enterprise workflows. (https://en.wikipedia.org/wiki/Claude_(language_model))
- **Claude 3 family (Haiku / Sonnet / Opus)** — Mar 4, 2024. Established the three-tier naming convention still in use. (https://en.wikipedia.org/wiki/Claude_(language_model); model card: https://www-cdn.anthropic.com/de8ba9b01c9ab7cbabf5c33b80b7bbc618857627/Model_Card_Claude_3.pdf)
- **Claude 3.5 Sonnet** — Jun 20, 2024. Outperformed the larger Claude 3 Opus on several benchmarks; introduced **Artifacts**. (https://en.wikipedia.org/wiki/Claude_(language_model))
- **Claude 3.5 Sonnet (updated) + Claude 3.5 Haiku + "Computer Use" (beta)** — Oct 22, 2024. First frontier model with a public-beta computer-use capability (screen viewing, cursor/click/type control via the API). (https://www.anthropic.com/news/3-5-models-and-computer-use)
- **Claude 3.7 Sonnet** — Feb 24, 2025. Added configurable "extended thinking" / reasoning duration — Anthropic's first hybrid reasoning model. (https://en.wikipedia.org/wiki/Claude_(language_model))
- **Claude Opus 4 & Claude Sonnet 4** — May 22, 2025. Stronger coding/agentic abilities, code-execution tools, Files API, and MCP connectors introduced around this release. Opus 4 was classified by Anthropic's own responsible-scaling framework as a higher-risk ("ASL-3"-type) model. (https://en.wikipedia.org/wiki/Claude_(language_model); https://www.anthropic.com/news/claude-4)
- **Claude Opus 4.1** — Aug 5, 2025. Added ability to end abusive/harmful conversations. **Deprecated, scheduled retirement Aug 5, 2026** (confirmed directly in current Anthropic docs as of this research). (https://platform.claude.com/docs/en/docs/about-claude/models/overview)
- **Claude Sonnet 4.5** — Sep 29, 2025.
- **Claude Haiku 4.5** — Oct 15, 2025. Positioned as "fastest with near-frontier intelligence," aimed at cost-sensitive/high-volume use.
- **Claude Opus 4.5** — Nov 24, 2025. Improved coding/workplace-task performance; "Infinite Chats" feature addressing context-window limits in claude.ai.
- **Claude Opus 4.6** — Feb 5, 2026. Added "Agent Teams" and a Claude-in-PowerPoint integration.
- **Claude Sonnet 4.6** — Feb 17, 2026. Marketed as near-Opus-4.6 performance at Sonnet pricing.
- **Claude Opus 4.7** — Apr 16, 2026. New tokenizer (≈30% more tokens for the same text vs. prior models); some user reports of increased refusal rates circulated this month.
- **Claude Opus 4.8** — May 28, 2026. Current flagship Opus-tier model ("most capable Opus-tier model for complex reasoning, long-horizon agentic coding, and high-autonomy work"). (https://www.anthropic.com/news — post titled "Introducing Claude Opus 4.8")
- **Claude Mythos Preview** — first introduced ~Apr 7, 2026 as an invitation-only research-preview model (initially ~11 organizations) under **Project Glasswing**, Anthropic's defensive-cybersecurity initiative; can autonomously find zero-day vulnerabilities and build exploits for them. Anthropic states it does **not** plan to make Mythos Preview generally available. (https://www.anthropic.com/glasswing; https://www.anthropic.com/research/glasswing-initial-update)
- **Claude Fable 5 + Claude Mythos 5** — Jun 9, 2026. First public debut of the "Mythos-class" tier (positioned above Opus). Fable 5 (`claude-fable-5`) is generally available via the Claude API, AWS Bedrock, Vertex AI, and Microsoft Foundry. Mythos 5 (`claude-mythos-5`) is limited-availability only, via Project Glasswing. Pricing: **$10/$50 per MTok** input/output (2x Opus 4.8). 1M-token context window, 128K max output, "adaptive thinking" always on, no manually-configurable extended thinking. (https://platform.claude.com/docs/en/docs/about-claude/models/overview)
- **US government directive suspending Fable 5 / Mythos 5 — Jun 12, 2026.** The US government issued an export-control directive (citing national security authorities) ordering Anthropic to suspend all access to Fable 5 and Mythos 5 by foreign nationals, anywhere, including foreign-national Anthropic employees. Anthropic disabled the models for **all** customers (not just foreign nationals) to ensure compliance, while disputing the order's scope; other Claude models were unaffected. Anthropic's own statement suggests the trigger may have been the government learning of a jailbreak method for Fable 5. **This is corroborated by Anthropic's own news page plus CNBC, CNN, Bloomberg, and TechCrunch — it is real, not a search-result hallucination — but it is extremely recent (8 days old at research time) and the GTM team should treat the current commercial availability of Fable 5/Mythos 5 as fluid/pending further updates.** (https://www.anthropic.com/news/fable-mythos-access; https://www.cnbc.com/2026/06/12/anthropic-disables-access-to-fable-5-and-mythos-5-to-comply-with-government-directive.html; https://www.cnn.com/2026/06/13/business/anthropic-mythos-model-national-security)

### Current model line-up at a glance (per official docs, June 2026)
| Model | API ID | Context window | Max output | Extended thinking | Pricing (in/out per MTok) |
|---|---|---|---|---|---|
| Claude Fable 5 | `claude-fable-5` | 1M tokens | 128K | No (adaptive thinking always on) | $10 / $50 |
| Claude Mythos 5 (limited access) | `claude-mythos-5` | 1M tokens | 128K | No (adaptive thinking always on) | $10 / $50 |
| Claude Opus 4.8 | `claude-opus-4-8` | 1M tokens | 128K | No (adaptive thinking yes) | $5 / $25 |
| Claude Sonnet 4.6 | `claude-sonnet-4-6` | 1M tokens | 64K | Yes | $3 / $15 |
| Claude Haiku 4.5 | `claude-haiku-4-5` | 200K tokens | 64K | Yes | $1 / $5 |
| Claude Opus 4.7 (legacy) | `claude-opus-4-7` | 1M tokens | 128K | No | $5 / $25 |
| Claude Opus 4.6 (legacy) | `claude-opus-4-6` | 1M tokens | 128K | Yes | $5 / $25 |
| Claude Sonnet 4.5 (legacy) | `claude-sonnet-4-5` | 200K tokens | 64K | Yes | $3 / $15 |
| Claude Opus 4.5 (legacy) | `claude-opus-4-5` | 200K tokens | 64K | Yes | $5 / $25 |
| Claude Opus 4.1 (deprecated, retires Aug 5 2026) | `claude-opus-4-1` | 200K tokens | 32K | Yes | $15 / $75 |

Source for full table: https://platform.claude.com/docs/en/docs/about-claude/models/overview — all current models support text + image input, text output, multilingual, and vision.

Note: "Adaptive thinking" is a newer mechanism distinct from the older "extended thinking" toggle — Opus 4.6+/Fable/Mythos models use adaptive thinking instead of (or alongside) manual extended-thinking controls. Worth a follow-up if GTM materials need precise wording (docs link: /docs/en/build-with-claude/adaptive-thinking).

---

## 2. Claude.ai Consumer App

Available via web (claude.ai), desktop apps (macOS, Windows, Windows ARM64), and mobile (iOS, Android). (https://claude.com/product/overview)

### Tiers (as of research date)
- **Free ($0):** chat, code generation, content creation, web search, **Memory** (rolled out to all plans including Free since ~March 2026), file creation/upload (up to 20 files/chat, 30MB max cited by third-party guide), Projects, Artifacts, limited model access (Sonnet 4.6 default, limited Haiku 4.5; Opus not included on Free). (https://claude.com/pricing; secondary corroboration via aggregator guides — treat exact file-size/file-count limits as approximate and verify before quoting externally)
- **Pro ($17/mo billed annually or $20/mo billed monthly):** everything in Free plus more usage, Claude Code access, Claude Cowork, Claude Design, unlimited Projects, "Research" mode, multiple model options (limited Opus access), Microsoft 365/Outlook integration, voice mode. (https://claude.com/pricing)
- **Max (from $100/mo):** choice of 5x or 20x the usage of Pro, higher output limits, early access to new features, priority access at peak load. Two sub-tiers commonly called "Max 5x" ($100/mo) and "Max 20x" ($200/mo). (https://claude.com/pricing; https://claude.com/product/claude-code)
- **Team ($20/seat/mo standard, or $100/seat/mo "Premium" for 5x usage):** aimed at 5-150 person orgs; central billing/admin, SSO, admin controls for connectors, enterprise desktop deployment, enterprise search, org-wide Skill deployment. (https://claude.com/pricing)
- **Enterprise ($20/seat plus usage-based API charges):** all Team features plus role-based access controls, SCIM, audit logs, a compliance API, custom data retention, IP allowlisting, HIPAA-ready configurations. (https://claude.com/pricing)

### Key consumer features
- **Projects** — persistent workspaces holding uploaded files + custom instructions so Claude retains context across many conversations without needing the context re-explained each time. Launched September 2024; project context capacity reportedly expanded ~10x around June 2025. (industry write-ups; verify exact expansion date against an Anthropic primary source before quoting precisely)
- **Artifacts** — a side-panel canvon for live/runnable outputs: React apps, HTML pages, SVGs, Mermaid diagrams, code snippets, markdown docs, rendered in a sandboxed preview. By 2026 Artifacts reportedly support persistent storage, direct API calls from within an artifact, and MCP server connections; published artifacts get a shareable link, and other signed-in users can duplicate/remix them. (aggregator sources — corroborate specifics against claude.ai/artifacts before using in customer-facing copy)
- **Memory** — Claude retains facts about the user, their preferences, and work context across separate conversations; extended to all plans (including Free) reportedly around March 2026.
- **"Infinite Chats"** — introduced with Claude Opus 4.5 (Nov 24, 2025) to address hard context-window ceilings inside long claude.ai conversations.
- **Research mode** — agentic web/source research mode available on paid tiers.
- Computer-use/desktop-extension support and Slack/Google Workspace connectors are listed as part of even the Free tier feature set per claude.com/pricing — worth double-checking the precise free-vs-paid line before using in sales collateral, since this is one of the areas most likely to shift.

---

## 3. Claude API / Developer Platform

Core platform docs now live at **platform.claude.com** (redirected from the historical docs.anthropic.com); console/API access via the Claude Console. (https://platform.claude.com/docs/en/intro)

Key capabilities documented on the platform:
- **Vision** — image understanding/analysis, multimodal input, available on all current models. (https://docs.anthropic.com/en/docs/build-with-claude/vision)
- **Tool use** — function-calling so Claude can invoke external tools/APIs mid-conversation.
- **Computer use** — lets Claude view a screen and control mouse/keyboard to operate software/UIs; first launched in public beta alongside Claude 3.5 Sonnet (updated) and Claude 3.5 Haiku, Oct 22, 2024. (https://www.anthropic.com/news/3-5-models-and-computer-use)
- **Extended thinking** — configurable reasoning/"thinking" budget, first introduced with Claude 3.7 Sonnet (Feb 2025); thinking-process summaries are now streamed with minimal added latency. Note: current top-tier models (Opus 4.6+, Fable 5, Mythos 5) have moved to a related but distinct **"adaptive thinking"** mechanism (always-on for Fable/Mythos) rather than manually configured extended thinking — see /docs/en/build-with-claude/adaptive-thinking.
- **Prompt caching** — caches reusable prompt prefixes to cut latency/cost on repeated large contexts. (https://platform.claude.com/docs/en/build-with-claude/prompt-caching)
- **Batch processing (Message Batches API)** — asynchronous processing at a **50% discount** on input and output tokens; an extended-output beta (`output-300k-2026-03-24` header) now supports up to 300K output tokens on Opus 4.8/4.7/4.6 and Sonnet 4.6. (https://platform.claude.com/docs/en/build-with-claude/batch-processing)
- **Files API** — introduced around the May 2025 Claude 4 release, for persistent file handling across requests.
- **Models API** — lets developers programmatically query a model's `max_input_tokens`, `max_tokens`, and capabilities object.
- **Structured outputs, streaming, compaction** — listed among current Messages API features; "compaction" (context-window compression for long agent sessions) and an "advisor tool" (pairing a fast executor model with a higher-intelligence advisor model) are newer additions per current docs.
- **MCP connectors** — first-class support for connecting the API to Model Context Protocol servers (see Section 6).
- **Priority Tier / service tiers** — paid tier guaranteeing throughput/latency SLAs during high load. (https://platform.claude.com/docs/en/api/service-tiers)
- **Cloud platform availability** — Claude is available not just via Anthropic's own API but via **Claude Platform on AWS**, **Amazon Bedrock**, **Google Cloud Vertex AI**, and (newer) **Microsoft Foundry**. Each has its own model ID scheme and, in some cases, different context-window limits (e.g., Opus 4.8 is 1M tokens on Anthropic's API but 200K tokens specifically on Microsoft Foundry). (https://platform.claude.com/docs/en/docs/about-claude/models/overview)
- **Model deprecation policy** — dated model IDs (e.g., `-20250929`) are permanently pinned; starting with the 4.6 generation, even "dateless" IDs (e.g., `claude-opus-4-6`) are pinned snapshots, not evergreen aliases — a change from the historical pattern where the undated alias always pointed to the latest snapshot. Important nuance for any GTM/technical content about API stability.

### Claude Agent SDK
A separate SDK (Python + TypeScript) that exposes the same agent loop, tool-execution, context management, permissioning, and subagent machinery that powers Claude Code, for developers building their own autonomous agents rather than using Claude Code itself. Distinguished from the plain "Client SDK" in that the Agent SDK "owns the loop" (manages tool execution/retries/context automatically) vs. the client SDK where the developer manages the loop manually. (https://platform.claude.com/docs/en/agent-sdk/overview)

### Agent Skills
Reusable, filesystem-based packets of domain expertise (`SKILL.md` plus supporting resources) that Claude can discover and load on demand, rather than stuffing all instructions into context up front ("staged loading" — cheap metadata first, full resource bundles only when needed). Anthropic ships prebuilt Skills for common document tasks (PowerPoint, Excel, Word, PDF) and supports custom Skills. Skills work across claude.ai, Claude Code, the Agent SDK, and the Messages API (deployment specifics vary by surface). Open-source skill repo: https://github.com/anthropics/skills. (https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview)

---

## 4. Claude Code (CLI Coding Agent) and Developer Tooling

**Claude Code** is Anthropic's agentic coding tool. It reads a codebase, plans multi-file changes, edits code, runs commands/tests, iterates on failures, and can manage git workflows — all through natural-language instruction. (https://claude.com/product/claude-code; https://github.com/anthropics/claude-code)

- **Interfaces:** terminal/CLI, desktop app (macOS/Linux/Windows), VS Code extension (also usable in Cursor / Devin Desktop per third-party coverage), JetBrains plugin, web browser, and a Slack integration for kicking off tasks.
- **Autonomy controls:** default is cautious — Claude Code asks before file edits/command execution; developers can grant more autonomy, with built-in classifiers distinguishing safe vs. risky actions.
- **CI/CD integration:** can monitor GitHub/GitLab pipelines and commit fixes automatically; can turn issues into PRs.
- **Agent Teams** — multiple Claude Code instances working different parts of a problem in parallel, coordinated by a lead agent that assigns subtasks and merges results (feature surfaced via Claude Opus 4.6, Feb 2026).
- **Newer 2026 features per release notes:** "Dynamic Workflows" (parallel subagents, tens to hundreds, with verification before completion — May 28, 2026); "Agent View" (centralized session management — May 11, 2026); "Routines" (scheduled/API-triggered/event-based task execution — Apr 14, 2026); a "Computer Use" capability inside Claude Code itself (Mar 23, 2026). These specific dates come from a third-party release-tracking aggregator (releasebot.io) rather than Anthropic's own changelog directly — corroborate against Anthropic's official Claude Code release notes before treating dates as authoritative.
- **Pricing:** bundled into Claude Pro ($17-20/mo), Max 5x ($100/mo) and Max 20x ($200/mo) consumption allowances; also usable via Console/API token billing. A "Fast Mode" exists at $30/$150 per MTok (Opus 4.8) for consumption-based acceleration.

### Claude Cowork
A newer (per Simon Willison's first-look post dated Jan 12, 2026) desktop agent product for **general knowledge work** (not just code): runs on the desktop, connects to local files/apps, completes multi-step tasks end-to-end (read/edit/create files in user-specified folders) while keeping consequential decisions with the human. Coverage (e.g., AOL/syndicated wire piece) characterized it as a file-managing AI agent with the potential to compete with various productivity-automation startups. (https://www.anthropic.com/product/claude-cowork; https://simonwillison.net/2026/jan/12/claude-cowork/)

### Claude Design
An Anthropic Labs product (research preview) for collaborating with Claude on visual/design work — prototypes, slide decks, one-pagers — powered by Claude's vision capability (cited as Opus 4.7 in the source). During onboarding it builds a team design system by reading the org's codebase/design files, then reuses brand colors/typography/components automatically. Available to Pro/Max/Team/Enterprise. (https://www.anthropic.com/news/claude-design-anthropic-labs)

### Claude Security
A public-beta product (currently Enterprise-only) that performs context-aware code security review — tracing data flows across files to catch complex/multi-component vulnerability patterns that traditional static scanners miss, with a recommended patch attached to each finding for human review/approval. (https://claude.com/product/claude-security)

---

## 5. Claude for Enterprise / Education / Government

### Enterprise / Teams
Covered above under pricing tiers (Team, Enterprise). Enterprise adds SCIM, audit logs, compliance API, custom retention, IP allowlisting, and HIPAA-ready configurations. (https://claude.com/pricing)

### Claude for Education
A specialized offering for higher-ed institutions covering teaching, learning, and administration use cases. Confirmed integrations include **Wiley** and **Panopto** (letting students reference textbooks/lecture transcripts inside Claude) and **Canvas LTI** support (Claude usable directly inside Canvas courses). (https://www.anthropic.com/news/introducing-claude-for-education; https://www.edtechinnovationhub.com/news/anthropic-expands-claudes-role-in-higher-education-and-national-research-with-new-university-tools-and-federal-lab-deployment)

### Claude for Government / Claude Gov
- In **June 2025**, Anthropic introduced a distinct **Claude Gov** model family built specifically for U.S. national-security customers. (per search-result synthesis — verify exact month against Anthropic's news archive before citing precisely)
- In **August 2025**, Anthropic and the U.S. General Services Administration (GSA) struck a "OneGov" deal making Claude for Enterprise and Claude for Government available to all three branches of the U.S. federal government for **$1 per agency for one year**. (https://www.gsa.gov/about-gsa/newsroom/news-releases/gsa-strikes-onegov-deal-with-anthropic-08122025; https://www.cnbc.com/2025/08/12/anthropic-claude-government-ai.html; https://www.anthropic.com/news/offering-expanded-claude-access-across-all-three-branches-of-government)
- **Claude for Government** runs under a **FedRAMP High** Authorization to Operate, is logically isolated from commercial tenants, and is hosted via Anthropic's government-authorized partner infrastructure — positioned for sensitive (but unclassified) federal work. (https://support.claude.com/en/articles/14503590-get-started-with-claude-for-government)
- Lawrence Livermore National Laboratory was cited as an Enterprise deployment example, with access extended to roughly 10,000 researchers/staff (figure from search synthesis — verify against a primary Anthropic or LLNL source before reuse).
- Note the tension with Section 1's item on the **Jun 12, 2026 government directive** suspending foreign-national access to Fable 5/Mythos 5 — i.e., Anthropic's relationship with the U.S. government spans both an active commercial/procurement partnership (GSA OneGov, Claude for Gov, Project Glasswing critical-infrastructure partners) and, very recently, a regulatory/export-control intervention on its newest frontier models. Both threads are real and currently in tension; useful context for GTM teams operating in regulated/public-sector verticals.

---

## 6. Model Context Protocol (MCP)

**What it is:** An open standard, introduced by Anthropic on **November 25, 2024** (some secondary sources round this to "November 2024"), for connecting AI systems/LLMs to external data sources and tools through a single, standardized interface instead of bespoke per-integration code — often described as "a USB-C port for AI applications." (https://www.anthropic.com/news/model-context-protocol; https://en.wikipedia.org/wiki/Model_Context_Protocol)

**How it works:** MCP defines **clients** (AI applications) and **servers** (which expose a data source, system, or capability). Transport is JSON-RPC — standard input/output for local connections, with an HTTP + Server-Sent-Events-based transport for remote connections.

**Launch components (Nov 2024):** the protocol spec + SDKs (open-sourced on GitHub), local MCP server support built into Claude Desktop, and an open-source repository of pre-built servers (Google Drive, Slack, GitHub, Postgres, SQLite, Puppeteer/browser control, etc.).

**Early adopters/partners cited at launch:** Block and Apollo (production integrations); Zed, Replit, Codeium, and Sourcegraph (dev-tools companies building MCP into their platforms for coding-agent context retrieval).

**Where it fits in the product suite:** MCP is the connective tissue across nearly the whole current lineup — Claude Desktop, Claude.ai (Artifacts can now connect to MCP servers per 2026 coverage), Claude Code, the Claude API (first-class MCP connector support), and the Agent SDK all consume the same protocol. Anthropic also publishes engineering guidance on **code execution with MCP** for building more token-efficient agents. (https://www.anthropic.com/engineering/code-execution-with-mcp)

By 2025-2026, MCP was adopted well beyond Anthropic (it has become a broader industry-standard pattern for agent-tool integration), which is itself a notable GTM/positioning point — Anthropic effectively set a standard the rest of the industry converged on.

---

## 7. Integrations, Extensions, and Other Notable Products

- **Claude for Chrome** — browser extension; Claude reads, clicks, and navigates websites in a side panel; in beta, available on all paid plans (Pro/Max/Team/Enterprise). (https://claude.com/claude-for-chrome; https://support.claude.com/en/articles/12012173-get-started-with-claude-in-chrome)
- **Claude for Slack** — Slack workspace bot; requires a Team or Enterprise plan.
- **Claude for Microsoft 365** — add-ins for **Excel**, **PowerPoint**, **Word**, and **Outlook**; Excel add-in specifically aimed at financial analysis/modeling workflows. Organizations on AWS Bedrock, Vertex AI, or an internal LLM gateway can use these add-ins without a separate Claude account, routed through their own infrastructure. (https://support.claude.com/en/articles/12650343-use-claude-for-excel; https://support.claude.com/en/articles/13945233-use-claude-for-microsoft-365-with-third-party-platforms)
- **Claude in GitHub** — code review / issue-to-PR workflows (cited alongside the Chrome/Excel/Slack integrations roundup; verify exact product name/scope against Anthropic's own GitHub integration docs before using in GTM materials).
- **Connectors / Plugins** — general mechanisms (visible in claude.com/product/overview navigation) for linking Claude to third-party apps/services and extending functionality; likely the same underlying mechanism as MCP server connections surfaced as a user-facing feature.
- **Anthropic Console** — for crafting/testing prompts directly in-browser, part of the developer platform.

---

## 8. Uncertain / Needs Follow-Up Before External Use

Flagging these explicitly per the research brief:

1. **Mythos-tier and Fable 5 commercial status post-June 12, 2026 directive** — confirmed suspended for foreign nationals (and de facto for everyone, per Anthropic's own compliance statement) as of the order; current research could not confirm whether/when access has been or will be restored. Treat current availability as a live/moving target.
2. **Exact Memory rollout date to Free tier** ("around March 2026") and **Projects context expansion** ("~10x, around June 2025") — sourced from aggregator/guide sites rather than an Anthropic primary post; recommend finding the specific Anthropic news post before quoting dates in customer-facing material.
3. **Claude for Gov family launch date** (cited as "June 2025") and the **LLNL ~10,000 researchers** figure — both came through search-synthesis rather than a directly fetched primary source; verify against anthropic.com/news or the relevant lab's announcement.
4. **Free-tier feature list specifics** (20 files/chat, 30MB cap; which connectors are truly free vs. paid) — claude.com/pricing was fetched directly and is the best source, but third-party aggregator detail (exact file limits) wasn't independently verified against the primary page's fine print.
5. **"Claude in GitHub" naming/scope** — mentioned in a roundup piece but not verified against an Anthropic-owned page in this pass.
6. General caution: several search results came from SEO/aggregator sites (e.g., suprmind.ai, releasebot.io, glbgpt.com) that are plausible-sounding but not Anthropic-owned or major press — used only for supplementary color where corroborated elsewhere, never as a sole source for a hard claim.

---

## Source List (primary sources used)

- https://claude.com/product/overview
- https://platform.claude.com/docs/en/docs/about-claude/models/overview
- https://claude.com/pricing
- https://claude.com/product/claude-code
- https://www.anthropic.com/product/claude-cowork
- https://www.anthropic.com/news/claude-design-anthropic-labs
- https://claude.com/product/claude-security
- https://www.anthropic.com/news/model-context-protocol
- https://www.anthropic.com/engineering/code-execution-with-mcp
- https://www.anthropic.com/glasswing
- https://www.anthropic.com/research/glasswing-initial-update
- https://www.anthropic.com/news/expanding-project-glasswing
- https://www.anthropic.com/news/fable-mythos-access
- https://www.anthropic.com/news/3-5-models-and-computer-use
- https://www.anthropic.com/news/claude-4
- https://www.anthropic.com/news/introducing-claude-for-education
- https://www.anthropic.com/news/offering-expanded-claude-access-across-all-three-branches-of-government
- https://support.claude.com/en/articles/14503590-get-started-with-claude-for-government
- https://support.claude.com/en/articles/12650343-use-claude-for-excel
- https://support.claude.com/en/articles/13945233-use-claude-for-microsoft-365-with-third-party-platforms
- https://support.claude.com/en/articles/12012173-get-started-with-claude-in-chrome
- https://claude.com/claude-for-chrome
- https://platform.claude.com/docs/en/build-with-claude/prompt-caching
- https://platform.claude.com/docs/en/build-with-claude/batch-processing
- https://platform.claude.com/docs/en/api/service-tiers
- https://platform.claude.com/docs/en/agent-sdk/overview
- https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview
- https://github.com/anthropics/skills
- https://github.com/anthropics/claude-code
- https://en.wikipedia.org/wiki/Claude_(language_model)
- https://en.wikipedia.org/wiki/Model_Context_Protocol
- https://www.gsa.gov/about-gsa/newsroom/news-releases/gsa-strikes-onegov-deal-with-anthropic-08122025
- https://www.cnbc.com/2025/08/12/anthropic-claude-government-ai.html
- https://www.cnbc.com/2026/06/12/anthropic-disables-access-to-fable-5-and-mythos-5-to-comply-with-government-directive.html
- https://www.cnn.com/2026/06/13/business/anthropic-mythos-model-national-security
- https://www.helpnetsecurity.com/2026/05/26/anthropic-project-glasswing-update/
- https://techcrunch.com/2026/06/02/anthropic-scales-claude-mythos-to-critical-infrastructure-in-15-countries/
- https://simonwillison.net/2026/jan/12/claude-cowork/
- https://www.edtechinnovationhub.com/news/anthropic-expands-claudes-role-in-higher-education-and-national-research-with-new-university-tools-and-federal-lab-deployment
