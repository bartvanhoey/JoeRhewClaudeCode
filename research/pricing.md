# Anthropic / Claude Pricing — Research Notes

**Research date:** 2026-06-20
**Purpose:** GTM reference (sales/marketing/positioning). Public sources only.

> **Important caveat on currency of this data:** Pricing for frontier AI products changes frequently — Anthropic has updated rate cards, launched new model generations, and even reversed a billing-policy change within the last six weeks (see "Recent changes" below). Treat the numbers below as a snapshot as of the research date and re-verify against [claude.com/pricing](https://claude.com/pricing) and [platform.claude.com/docs/en/docs/about-claude/pricing](https://platform.claude.com/docs/en/docs/about-claude/pricing) before using in a customer-facing deliverable.
>
> **Model-name caveat:** This research surfaced two model names — "Claude Fable 5" and "Claude Mythos 5" — that are unfamiliar from training data and read like internal codenames rather than typical "Claude X.Y" branding. They are corroborated by multiple independent sources (official docs page + several press/blog writeups describing a June 9, 2026 release), so they appear to be real, very recent releases rather than a scraping artifact — but flagging this explicitly since it's outside normal naming conventions and very recent. One source claims customer access to Fable 5 / Mythos 5 was "suspended" on June 12, 2026, which is also unverified beyond secondary blogs — confirm before citing.

---

## 1. Claude.ai Consumer Plan Pricing

Source: [claude.com/pricing](https://claude.com/pricing) (official, fetched 2026-06-20)

| Plan | Price | Billing notes | What's included |
|---|---|---|---|
| **Free** | $0/month | — | Web/mobile/desktop chat, code generation, content creation, web search, memory, file creation, code execution, desktop extensions, Slack/Google Workspace integration, connectors, extended thinking |
| **Pro** | $20/month (monthly) or **$17/month** billed annually ($200/yr upfront) — a 15% annual discount | Individual | Everything in Free, plus increased usage allowance, **Claude Code**, Claude Cowork, Claude Design, unlimited projects, Research access, multiple model options, Microsoft 365/Outlook integration |
| **Max** | **From $100/month** (5x tier); **$200/month** (20x tier) | Monthly only — no annual discount reported as of this research (per third-party aggregator; not independently confirmed on official page) | Everything in Pro, plus elevated output limits, early access to advanced features, priority access during peak traffic. The two tiers offer 5x or 20x more usage than Pro |
| **Team — Standard seat** | $25/seat/month (monthly) or **$20/seat/month** billed annually | Minimum 5 seats (per third-party sources) | All Claude capabilities with enhanced usage; centralized billing, admin controls |
| **Team — Premium seat** | $125/seat/month (monthly) or **$100/seat/month** billed annually | Same seat minimum | Standard seat features plus 5x increased usage |
| **Enterprise** | Custom — reported to start around **$20/seat/month minimum**, plus API usage billed separately on top | Sales-negotiated | All Team features plus enterprise search, SSO, SCIM, audit logs, compliance APIs, HIPAA options, no model training on user content, custom terms |

Sources:
- [claude.com/pricing](https://claude.com/pricing) — official page, confirms Free/Pro/Max/Team tiers, annual discount percentages, and that Claude Code is bundled into Pro and above.
- Team seat minimum and Max plan no-annual-discount claim are from secondary aggregator sources and **not independently confirmed** on the official page during this research pass: [Finout — Claude Pricing 2026](https://www.finout.io/blog/claude-pricing-in-2026-for-individuals-organizations-and-developers), [Tygart Media — Claude Pricing 2026](https://tygartmedia.com/claude-pricing-tiers-compared-free-pro-max-team-enterprise/).

**Note:** Anthropic's marketing site has moved from anthropic.com/pricing to **claude.com/pricing** (301 redirect observed during this research) — reflects the broader Claude.ai consumer brand separating from the anthropic.com corporate site. Likewise docs.anthropic.com now redirects to **platform.claude.com**.

---

## 2. Claude API Pricing (per-model token rates)

Source: [platform.claude.com/docs/en/docs/about-claude/pricing](https://platform.claude.com/docs/en/docs/about-claude/pricing) (official docs, fetched 2026-06-20). All prices per million tokens (MTok), USD.

### Standard API rate card

| Model | Base Input | 5-min Cache Write | 1-hr Cache Write | Cache Hit/Refresh | Output |
|---|---|---|---|---|---|
| Claude Fable 5 *(very recent; verify before use)* | $10 | $12.50 | $20 | $1 | $50 |
| Claude Mythos 5 *(limited availability; very recent)* | $10 | $12.50 | $20 | $1 | $50 |
| Claude Opus 4.8 | $5 | $6.25 | $10 | $0.50 | $25 |
| Claude Opus 4.7 | $5 | $6.25 | $10 | $0.50 | $25 |
| Claude Opus 4.6 | $5 | $6.25 | $10 | $0.50 | $25 |
| Claude Opus 4.5 | $5 | $6.25 | $10 | $0.50 | $25 |
| Claude Opus 4.1 *(deprecated)* | $15 | $18.75 | $30 | $1.50 | $75 |
| Claude Opus 4 *(retired except Vertex AI)* | $15 | $18.75 | $30 | $1.50 | $75 |
| Claude Sonnet 4.6 | $3 | $3.75 | $6 | $0.30 | $15 |
| Claude Sonnet 4.5 | $3 | $3.75 | $6 | $0.30 | $15 |
| Claude Sonnet 4 *(retired except Bedrock/Vertex)* | $3 | $3.75 | $6 | $0.30 | $15 |
| Claude Haiku 4.5 | $1 | $1.25 | $2 | $0.10 | $5 |
| Claude Haiku 3.5 *(retired except Bedrock/Vertex)* | $0.80 | $1 | $1.60 | $0.08 | $4 |

**Note on tokenizer change:** Opus 4.7 and later use a new tokenizer vs. earlier models, which "may use up to 35% more tokens for the same fixed text" — relevant for cost comparisons across model generations. Source: [platform.claude.com pricing page](https://platform.claude.com/docs/en/docs/about-claude/pricing).

### Prompt caching pricing (multipliers on base input rate)

| Cache operation | Multiplier | Duration |
|---|---|---|
| 5-minute cache write | 1.25x base input price | 5 minutes |
| 1-hour cache write | 2x base input price | 1 hour |
| Cache read (hit) | **0.1x** base input price | Same as preceding write |

A cache hit costs 10% of standard input price. Caching "pays off" after one read (5-min cache) or two reads (1-hr cache). Caching discounts stack with Batch API and data-residency multipliers. Source: [platform.claude.com pricing — Prompt caching](https://platform.claude.com/docs/en/docs/about-claude/pricing).

### Batch API pricing (50% discount)

| Model | Batch Input | Batch Output |
|---|---|---|
| Claude Fable 5 / Mythos 5 | $5 | $25 |
| Claude Opus 4.8 / 4.7 / 4.6 / 4.5 | $2.50 | $12.50 |
| Claude Opus 4.1 / Opus 4 | $7.50 | $37.50 |
| Claude Sonnet 4.6 / 4.5 / 4 | $1.50 | $7.50 |
| Claude Haiku 4.5 | $0.50 | $2.50 |
| Claude Haiku 3.5 | $0.40 | $2 |

Flat 50% off both input and output vs. standard rates, for asynchronous large-volume processing. Source: [platform.claude.com pricing — Batch processing](https://platform.claude.com/docs/en/docs/about-claude/pricing).

### Other API pricing levers

- **Fast mode** (research preview, Opus only): premium pricing for faster output. Opus 4.6/4.7: $30 input / $150 output per MTok. Opus 4.8: $10/$50 per MTok (i.e., Fast Mode price came down at the 4.8 release). Stacks with caching and data-residency multipliers; not available with Batch API or on Claude Platform on AWS. Source: [platform.claude.com pricing — Fast mode](https://platform.claude.com/docs/en/docs/about-claude/pricing).
- **Data residency / inference geography**: For Opus 4.6, Sonnet 4.6, and later, specifying US-only inference (`inference_geo: "us"`) adds a **1.1x multiplier** across all token categories. Global routing (default) is standard pricing. Source: same pricing page.
- **Long context (1M token window)**: Fable 5, Mythos 5, Opus 4.8/4.7/4.6, and Sonnet 4.6 include the full 1M-token context window at standard per-token pricing — no long-context surcharge. (Press coverage frames this as eliminating an industry-standard long-context surcharge at the Opus 4.6 launch — see Section 5.) Source: [platform.claude.com pricing — Long context pricing](https://platform.claude.com/docs/en/docs/about-claude/pricing).
- **Tool use overhead**: Tool definitions/schemas add input tokens; the API auto-injects a tool-use system prompt (e.g., ~290–675 tokens depending on model and tool-choice mode). Source: same pricing page.
- **Web search tool**: $10 per 1,000 searches, plus standard token costs for search-generated content. Source: same page.
- **Web fetch tool**: No additional charge beyond standard token costs for fetched content. Source: same page.
- **Code execution tool**: Free when paired with web search/fetch tools (recent SKUs). Standalone: billed by execution time (5-min minimum), 1,550 free container-hours/month per org, then $0.05/hour/container. Source: same page.
- **Claude Managed Agents** (a newer product surfaced on the pricing page): billed on tokens (standard model rates) **plus** session runtime at **$0.08 per session-hour**, metered to the millisecond while a session is actively `running`. Batch discount, Fast Mode, and data-residency multipliers do not apply to these sessions. Source: [platform.claude.com pricing — Claude Managed Agents](https://platform.claude.com/docs/en/docs/about-claude/pricing). *(Flagging as a fairly new/niche SKU worth confirming current relevance for GTM use.)*
- **Claude Platform on AWS**: Bills via AWS Marketplace using "Claude Consumption Units" (CCU) at $0.01/CCU; token usage is rated in USD at standard per-model rates then converted to CCUs. Source: same page.
- **Cloud platform availability**: Claude models also sold via Amazon Bedrock and Google Vertex AI, with independent pricing set by those platforms (generally mirrors first-party list price; regional/multi-region endpoints carry a 10% premium on Bedrock/Vertex for Claude 4.5+ models). Sources: [AWS Bedrock pricing](https://aws.amazon.com/bedrock/pricing/), [Vertex AI pricing](https://cloud.google.com/vertex-ai/generative-ai/pricing#claude-models).
- **Volume / enterprise discounts**: Anthropic states volume discounts "may be available for high-volume users... negotiated on a case-by-case basis," and that academic/research discounts may also be available. No public rate card. Source: [platform.claude.com pricing — Volume discounts](https://platform.claude.com/docs/en/docs/about-claude/pricing).

---

## 3. Claude Code Pricing Model

Source: [code.claude.com/docs/en/costs](https://code.claude.com/docs/en/costs) (official docs, fetched 2026-06-20)

- **No separate Claude Code price tag** for interactive use — it's bundled into Pro, Max, Team, and Enterprise subscriptions ("Includes Claude Code" per the plan comparison on [claude.com/pricing](https://claude.com/pricing)), drawing from the same usage pool as regular Claude.ai chat.
- **Pure API users** pay standard token rates (Section 2) with no subscription needed; Claude Code "charges by API token consumption" when run against an API key rather than a Pro/Max login.
- **Enterprise cost benchmark (official):** Anthropic publishes real usage data: average cost is **~$13 per developer per active day**, and **$150–250 per developer per month**, with 90% of users staying under $30/active-day. Source: [code.claude.com/docs/en/costs](https://code.claude.com/docs/en/costs).
- **Cost controls**: workspace spend limits (API/Console), `/usage-credits` monthly spend cap (Pro/Max), usage breakdown via `/usage` command, rate-limit tuning by team size (a published TPM/RPM-per-user table scaling from 200k–300k TPM for 1–5 users down to 10k–15k TPM for 500+ users).
- **Cost levers documented**: prompt caching (auto-applied), model selection (Sonnet vs. Opus vs. Haiku for subagents), extended-thinking budget tuning, context/compaction management, and offloading verbose output to subagents/hooks.

### Recent billing-policy change (notable, still unsettled as of research date)
- Anthropic announced (~May 14, 2026) plans to split **non-interactive/programmatic usage** — Claude Agent SDK, `claude -p` headless runs, GitHub Actions integration, third-party apps authenticating via a Claude subscription — out of the normal subscription rate-limit pool and into a separate dollar-denominated **"Agent SDK credit"** billed at standard API list rates, sized roughly $20 (Pro) / $100 (Max 5x) / $200 (Max 20x) per month, with overage billed at API rates. Planned effective date: **June 15, 2026**.
- **However**, multiple sources report Anthropic **paused/reversed this change on June 15, 2026** itself, confirming via Help Center that the Agent SDK/`claude -p`/third-party split is "no longer happening" and that they will revise the plan and give advance notice before any future change.
- **This is a live, fast-moving area — confirm current status before using in any customer-facing material.** Sources (secondary/press, not yet cross-checked against an official Anthropic post): [TechTimes](https://www.techtimes.com/articles/317625/20260602/anthropic-ends-subscription-subsidy-agents-june-15-credit-pool-replaces-flat-rate-access.htm), [Digital Applied — Claude Credit Overhaul](https://www.digitalapplied.com/blog/anthropic-claude-credit-overhaul-june-15-2026), [Zed.dev blog](https://zed.dev/blog/anthropic-subscription-changes), [andrew.ooo decision guide](https://andrew.ooo/answers/anthropic-claude-code-june-15-billing-change-may-2026/), [UsageBox](https://usagebox.com/articles/anthropic-june-15-agent-sdk-credit-split-claude-4-retirement).

---

## 4. Enterprise / Custom Pricing — What's Publicly Known

There is **no public enterprise rate card** — Anthropic's own docs repeatedly direct enterprise prospects to "contact sales@anthropic.com" / the Claude.com sales-contact form for custom pricing. What is publicly visible:

- **Structural pattern reported by analysts/third parties** (not Anthropic-confirmed): enterprise contracts combine (a) a per-seat fee, (b) a committed annual token volume or spend commitment negotiated up front (often discounted off list API rates in exchange for the commitment), and (c) metered token usage billed on top at standard or negotiated rates. Minimum seat counts (e.g., 50-seat minimums) and base seat fees in the **$20–60/user/month** range are cited by third-party "benchmark" sites, but these are not sourced to Anthropic and should be treated as estimates/inference, not confirmed list price. Sources: [Morph — Anthropic Enterprise Pricing](https://www.morphllm.com/anthropic-enterprise-pricing), [VendorBenchmark](https://vendorbenchmark.com/blog/anthropic-claude-enterprise-pricing-benchmark), [Redress Compliance — Negotiating Claude Contracts](https://redresscompliance.com/negotiating-anthropic-claude-contracts-enterprise-playbook.html), [SpendHound](https://www.spendhound.com/marketplace/anthropic-pricing).
- **Official confirmation of the general shape**: the official pricing page does confirm Enterprise = Team features + custom terms, with a stated **$20/seat/month minimum** plus API usage billed separately — consistent with the third-party "seat + committed token spend" framing above. Source: [claude.com/pricing](https://claude.com/pricing) (via WebFetch summary, this research pass).
- **Notable named enterprise deals reported in press** (illustrative of deal scale/structure, not list pricing):
  - **Snowflake**: $200M multi-year partnership to embed Claude (Sonnet 4.5 powering "Snowflake Intelligence") into Snowflake's data cloud, reaching Snowflake's 12,600+ global customers. Sources: [Snowflake press release](https://www.snowflake.com/en/news/press-releases/snowflake-and-anthropic-announce-200-million-partnership-to-bring-agentic-ai-to-global-enterprises/), [TechTarget](https://www.techtarget.com/searchdatamanagement/news/366635815/Snowflake-Anthropic-boost-partnership-with-200M-commitment).
  - **Deloitte**: Anthropic's largest enterprise deployment to date — Claude rolled out to 470,000+ Deloitte employees across 150 countries (figure varies 420k–470k across outlets — likely reflects different snapshot dates of a phased rollout). Includes a joint certification program to train/certify 15,000 Deloitte professionals on Claude, and a "Claude Center of Excellence." No dollar figure disclosed by either party. Sources: [CNBC](https://www.cnbc.com/2025/10/06/anthropic-deloitte-enterprise-ai.html), [Anthropic's own news post](https://www.anthropic.com/news/deloitte-anthropic-partnership), [IT Pro](https://www.itpro.com/technology/artificial-intelligence/deloitte-signs-up-anthropic-in-ai-enterprise-deal).
  - **IBM**: Reported partnership integrating Claude into IBM software products; no public pricing/deal-size figure found in this research pass. Source: general press coverage, not independently deep-dived here — flag for follow-up if needed.
- **Strategic framing in press**: Anthropic's enterprise-deal-led strategy (named large accounts, embedded platform partnerships) is repeatedly contrasted with OpenAI's more consumer/developer-breadth-led approach — this is analyst commentary, not Anthropic's own positioning. Source: [aibusiness.com — Snowflake deal](https://aibusiness.com/generative-ai/snowflake-deal-an-example-of-anthropi-influence).

**Caveat:** None of the seat-fee or committed-spend numbers above come from an Anthropic-published rate card — they are third-party inference/benchmarking or deal-specific press disclosures. Useful for GTM scoping conversations, but should not be quoted to a customer as official pricing.

---

## 5. Notable Pricing Changes Over Time

| Change | What happened | Source |
|---|---|---|
| **Opus price cut, ~67%** (Opus 4.6 launch, reported 2026-02-05) | Opus dropped from $15 input / $75 output per MTok (Opus 4.1) to $5 input / $25 output per MTok (Opus 4.5 and later) — a list-price cut of roughly two-thirds on the flagship tier. Also coincided with eliminating a long-context surcharge that had been standard industry practice. | Corroborated by official docs pricing table (Opus 4.1/4 at $15/$75 vs. Opus 4.5+ at $5/$25) and press/analyst recap: [Finout — Opus 4.7 pricing piece](https://www.finout.io/blog/claude-opus-4.7-pricing-the-real-cost-story-behind-the-unchanged-price-tag) |
| **Haiku price increase, ~4x** (Claude 3.5 Haiku vs. Claude 3 Haiku) | Claude 3 Haiku was $0.25 input / $1.25 output per MTok; Claude 3.5 Haiku launched at $1 input / $5 output per MTok — roughly a 4x increase for the "cheap/fast" tier as capability increased. | Third-party recap, not independently re-verified against an Anthropic primary source in this pass — flag as likely accurate (consistent with widely-reported Claude 3.5 Haiku launch pricing) but unconfirmed citation: search-aggregated result, no single authoritative URL captured. |
| **Fast Mode price cut at Opus 4.8** | Fast Mode (premium low-latency tier) dropped from $30/$150 per MTok (Opus 4.6/4.7) to $10/$50 per MTok at Opus 4.8 — a 67% cut on that specific SKU. | [platform.claude.com pricing — Fast mode section](https://platform.claude.com/docs/en/docs/about-claude/pricing) |
| **Claude Fable 5 / Mythos 5 priced above Opus** | Launched ~June 9, 2026 at $10 input / $50 output per MTok — double the Opus 4.8 rate ($5/$25), making it the most expensive flagship Anthropic has shipped for general use. One report claims customer access was suspended June 12, 2026 days after launch. | [claudefa.st — Fable 5 piece](https://claudefa.st/blog/models/claude-fable-5-mythos-5) — secondary source, recommend independent confirmation given the highly unusual "launch then suspend" claim. |
| **Claude Code billing policy churn** | See Section 3 — announced split of Agent SDK/non-interactive usage out of subscriptions (~May 14, 2026), planned effective June 15, 2026, then reportedly paused same day. | See Section 3 sources. |
| **Pricing page consolidation** | anthropic.com/pricing now 301-redirects to claude.com/pricing; docs.anthropic.com redirects to platform.claude.com — suggests an ongoing brand/site consolidation moving consumer-facing Claude content off the anthropic.com root domain. | Observed directly via WebFetch redirect responses, this research pass. |

**General observation for GTM:** the pattern across the last several model generations is "flagship (Opus) gets cheaper or flat over time while capability rises," which is a usable talking point against the narrative that frontier AI always gets more expensive — but the new Fable 5/Mythos 5 tier pricing above Opus complicates that narrative for the very newest tier. Worth confirming current state before using in customer conversations given the volatility flagged above.

---

## 6. Competitor Pricing Comparisons (as reported in press/analyst pieces — not our own analysis)

These are points of comparison **found in secondary sources**, not independent competitive analysis (that's a separate research file per the task brief).

| Comparison point | Claim found | Source |
|---|---|---|
| Flagship API rate, Claude vs. Gemini | "Gemini 3.1 Pro is the cheapest flagship at $2/$12 per 1M tokens, 60% under Claude Opus 4.7 ($5/$25)." | Search-aggregated analyst commentary, e.g. [nicolalazzari.ai pricing comparison](https://nicolalazzari.ai/articles/ai-api-pricing-comparison-2026), [usagebox.com](https://usagebox.com/articles/gpt-5-vs-gemini-3-vs-claude-opus-pricing-may-2026) |
| Flagship API rate, Claude vs. OpenAI | GPT-5.2 reported at $1.75 input / $14 output per MTok; GPT-5.5 reported at $5/$30 per MTok — roughly comparable to or somewhat above Claude Opus on output pricing depending on which OpenAI tier is compared. | Same aggregator sources above; **note**: GPT-5.x naming/pricing is outside this researcher's training-data knowledge and was not independently verified against openai.com — treat as unconfirmed. |
| Consumer subscription comparison | ChatGPT: Free / Plus $20 / Pro $200 (unlimited advanced reasoning). Claude: Free / Pro $20 / Max $100 (5x) or $200 (20x). Google: AI Pro $19.99 / AI Ultra $249.99. | Same aggregator sources; broadly consistent with what we found directly on official pages for Claude's own tiers (Section 1). |
| Strategic contrast | Press frames Anthropic as enterprise-deal-led (Snowflake, Deloitte, IBM) vs. OpenAI's broader consumer/developer-breadth approach. | [aibusiness.com](https://aibusiness.com/generative-ai/snowflake-deal-an-example-of-anthropi-influence) |

**Caveat:** All competitor figures above came from blog/aggregator-style sources surfaced via search, not fetched directly from openai.com or Google's own pricing pages in this research pass. Given how fast this space moves and that several of these sites read as SEO/programmatic content (not primary journalism), **treat every competitor number in this section as needing independent re-verification** before quoting it externally. Recommend the separate competitive-analysis research file fetch pricing directly from OpenAI's and Google's official pricing pages rather than relying on these secondary aggregations.

---

## 7. Open Questions / Follow-ups for Other Research Files

- IBM partnership financial/deal-size details were not deep-dived here (low signal in this pass) — worth a targeted look if the partnerships/ecosystem research file covers it.
- The Claude Code Agent SDK billing change is unresolved as of the research date — needs a re-check closer to publication of any GTM deliverable.
- "Claude Fable 5" / "Claude Mythos 5" are very new and unfamiliar — confirm naming, positioning, and pricing stability directly against claude.com/pricing before quoting in customer-facing material.
- Team plan seat minimums (5-seat vs. other figures cited) and Enterprise seat-fee ranges ($20–60/user/month cited by aggregators) were not found stated explicitly on the official pricing page text we fetched — worth a direct re-check if exact seat minimums matter for a deal.
