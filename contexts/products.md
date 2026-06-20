# Anthropic Product Lineup

GTM-ready summary of Anthropic's product line, as of June 2026. Condensed from `research/products.md` — see that file for full citations and detail.

> **Caveat:** Anthropic's newest model tier ("Mythos-class": Claude Fable 5 / Claude Mythos 5, launched Jun 9, 2026) hit an export-control snag days after launch — a US government directive ordered access suspended for foreign nationals, and Anthropic disabled it for all customers pending compliance review. Treat current commercial availability of Fable 5 / Mythos 5 as unsettled; verify before quoting in customer-facing material.

---

## 1. Models

Three perennial tiers — **Haiku** (fast/cheap), **Sonnet** (balanced), **Opus** (most capable) — since Claude 3 (Mar 2024). A fourth tier, **Mythos-class**, now sits above Opus (see caveat above).

**Why it matters for GTM:** the tier structure maps directly to buyer budget/latency tradeoffs — Haiku for high-volume/cost-sensitive, Sonnet for general-purpose default, Opus for hardest reasoning/coding/agentic work. Pricing and context windows are the two numbers prospects ask for first.

Current line-up (per platform.claude.com, June 2026):

| Model | Context | Max output | Pricing (in/out per MTok) |
|---|---|---|---|
| Claude Fable 5 (GA, access disputed — see caveat) | 1M | 128K | $10 / $50 |
| Claude Mythos 5 (invite-only) | 1M | 128K | $10 / $50 |
| Claude Opus 4.8 (flagship) | 1M | 128K | $5 / $25 |
| Claude Sonnet 4.6 | 1M | 64K | $3 / $15 |
| Claude Haiku 4.5 | 200K | 64K | $1 / $5 |
| Claude Opus 4.1 (deprecated, retires Aug 5 2026) | 200K | 32K | $15 / $75 |

Notable trajectory: Claude 2.1 (Nov 2023) brought the 200K context window that defined the line for two years; Claude 3.7 Sonnet (Feb 2025) added configurable "extended thinking" (Anthropic's first hybrid reasoning model); Claude Opus 4 / Sonnet 4 (May 2025) brought strong agentic/coding ability and is the generation most current enterprise deployments are built on. Newer Opus/Fable/Mythos models use an always-on "adaptive thinking" mechanism rather than the manual extended-thinking toggle — useful distinction if a prospect asks about reasoning controls.

---

## 2. Claude.ai (Consumer App)

Web, desktop (macOS/Windows), and mobile (iOS/Android).

**Tiers:** Free (chat, Memory, Projects, Artifacts, limited models — no Opus); Pro ($17-20/mo: Claude Code access, Research mode, more model choice); Max ($100/$200 mo, 5x/20x usage, priority access); Team ($20-100/seat: SSO, admin controls, org-wide Skills); Enterprise ($20/seat + usage: RBAC, SCIM, audit logs, compliance API, HIPAA-ready).

**Why it matters for GTM:** this is the self-serve/PLG funnel and the tier ladder sales conversations usually start from. Team/Enterprise are the seats that matter for B2B deals.

**Key features:**
- **Projects** — persistent workspace (files + instructions) so context doesn't need re-explaining every chat.
- **Artifacts** — side-panel canvas for runnable outputs (code, React apps, docs, diagrams); shareable/remixable, now connects to MCP servers.
- **Memory** — retains user facts/preferences across conversations; available on all plans including Free.
- **Infinite Chats** — works around context-window ceilings in long conversations (added with Opus 4.5).
- **Research mode** — agentic web research, paid tiers only.

---

## 3. Claude API / Developer Platform

Docs at platform.claude.com; console access via Claude Console.

**Why it matters for GTM:** this is the build-on-Claude pitch — pricing, reliability guarantees, and cross-cloud availability are what technical buyers evaluate against OpenAI/Gemini.

Core capabilities: vision (multimodal input), tool use (function calling), computer use (screen/mouse/keyboard control, beta since Oct 2024), extended/adaptive thinking, prompt caching, batch processing (50% discount, async), Files API, Models API, structured outputs/streaming/context compaction, MCP connector support, and a paid Priority Tier for throughput/latency SLAs.

**Distribution:** available directly via Anthropic's API and through **AWS Bedrock**, **Google Cloud Vertex AI**, and **Microsoft Foundry** — each with its own model IDs and occasionally different limits (e.g., Opus 4.8 context is 1M on Anthropic's API, 200K on Microsoft Foundry). Worth flagging to prospects already committed to a cloud platform.

**Model deprecation policy:** dated model IDs are pinned permanently; as of the 4.6 generation even "dateless" IDs are pinned snapshots rather than evergreen aliases — a real shift from older behavior, relevant for any customer asking about API stability/upgrade risk.

**Claude Agent SDK** — Python/TypeScript SDK exposing the same agent loop/tool-execution/context-management machinery that powers Claude Code, for teams building their own autonomous agents. Differs from the plain Client SDK in that it "owns the loop" automatically.

**Agent Skills** — reusable, filesystem-based expertise packets (`SKILL.md` + resources) Claude loads on demand instead of front-loading context. Prebuilt Skills ship for PowerPoint/Excel/Word/PDF; works across claude.ai, Claude Code, Agent SDK, and the API. Open-source repo: github.com/anthropics/skills.

---

## 4. Claude Code and Developer Tooling

**Claude Code** is Anthropic's agentic coding tool — reads a codebase, plans multi-file changes, edits, runs tests, iterates, handles git workflows via natural language.

**Why it matters for GTM:** this is Anthropic's flagship developer-facing product and a major driver of Pro/Max upgrades; "autonomy with guardrails" (asks before risky actions, classifiers separate safe vs. risky changes) is the core trust pitch.

- **Interfaces:** terminal/CLI, desktop app, VS Code/JetBrains plugins, browser, Slack.
- **CI/CD:** can monitor pipelines, auto-commit fixes, turn issues into PRs.
- **Agent Teams** — multiple Claude Code instances split a problem in parallel under a coordinating lead agent.
- **Pricing:** bundled into Pro/Max consumption allowances or billed via Console/API tokens; a paid "Fast Mode" exists for accelerated throughput.

**Adjacent products:**
- **Claude Cowork** — desktop agent for general knowledge work (not just code): reads/edits/creates files across local apps for multi-step tasks, keeping consequential decisions with the human.
- **Claude Design** — Labs research preview for visual/design work (decks, prototypes); learns a team's design system from its codebase. Pro/Max/Team/Enterprise.
- **Claude Security** — Enterprise-only public beta for context-aware code security review, tracing data flows across files with suggested patches.

---

## 5. Enterprise, Education, and Government

**Enterprise/Team:** see Section 2 tiers — SCIM, audit logs, compliance API, custom retention, IP allowlisting, HIPAA-ready.

**Claude for Education:** higher-ed offering for teaching/learning/admin. Integrations include Wiley, Panopto, and Canvas LTI (Claude usable inside Canvas courses).

**Claude for Government / Claude Gov:** a separate model family for U.S. national-security customers (introduced ~mid-2025). Anthropic struck a "OneGov" deal with the GSA (Aug 2025) putting Claude for Enterprise/Government in front of all three federal branches for $1/agency for one year. Runs under FedRAMP High authorization, logically isolated from commercial tenants. Lawrence Livermore National Lab is a cited Enterprise deployment example.

**Why it matters for GTM:** strong public-sector momentum (FedRAMP High, GSA deal) is a genuine differentiator — but sits in tension with the Jun 12, 2026 export-control directive on Fable 5/Mythos 5 (see top caveat). Both are real and current; worth knowing both threads before a public-sector conversation.

---

## 6. Model Context Protocol (MCP)

**What it is:** an open standard Anthropic introduced (Nov 2024) for connecting AI systems to external data/tools through one standardized interface instead of bespoke integrations — "a USB-C port for AI applications." Defines clients (AI apps) and servers (data/capability sources); JSON-RPC transport (stdio locally, HTTP+SSE remotely).

**Why it matters for GTM:** MCP is a genuine standards win — adoption spread well beyond Anthropic across the industry, which is a strong positioning point ("Anthropic set the standard the rest of the industry converged on"). It's also the connective tissue across the whole product line: Claude Desktop, claude.ai (Artifacts), Claude Code, the API, and the Agent SDK all consume the same protocol, and a large open-source server registry (Slack, GitHub, Postgres, Google Drive, etc.) already exists.

---

## 7. Integrations and Extensions

- **Claude for Chrome** — browser extension; Claude reads/clicks/navigates sites in a side panel. Beta, all paid plans.
- **Claude for Slack** — workspace bot, Team/Enterprise.
- **Claude for Microsoft 365** — add-ins for Excel (financial modeling focus), PowerPoint, Word, Outlook; usable via Bedrock/Vertex/internal gateway without a separate Claude account.
- **Claude in GitHub** — code review / issue-to-PR workflows.
- **Connectors/Plugins** — general mechanism for linking Claude to third-party apps, largely MCP under the hood.
- **Anthropic Console** — in-browser prompt crafting/testing, part of the developer platform.

---

## Sources

Primary: claude.com (product/pricing pages), platform.claude.com/docs, anthropic.com/news, support.claude.com. Press corroboration for recent items: CNBC, CNN, Bloomberg, TechCrunch. Full source list and per-claim citations: `research/products.md`.
