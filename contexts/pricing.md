# Anthropic / Claude Pricing

**Pricing as of: 2026-06-20.** Frontier AI pricing changes often — re-verify against [claude.com/pricing](https://claude.com/pricing) and [platform.claude.com/docs/en/docs/about-claude/pricing](https://platform.claude.com/docs/en/docs/about-claude/pricing) before quoting to a customer.

---

## 1. Consumer Plans (Claude.ai)

| Plan | Price | Notes |
|---|---|---|
| **Free** | $0/mo | Web/mobile/desktop chat, code gen, web search, memory, file creation, code execution, connectors |
| **Pro** | $20/mo, or $17/mo billed annually ($200/yr) | + Claude Code, Claude Cowork, Claude Design, unlimited projects, Research access, multiple models |
| **Max 5x** | $100/mo | 5x Pro usage, elevated output limits, priority access |
| **Max 20x** | $200/mo | 20x Pro usage; no annual discount reported on either Max tier |
| **Team — Standard** | $25/seat/mo, or $20/seat/mo annual | Centralized billing, admin controls (5-seat minimum reported, not officially confirmed) |
| **Team — Premium** | $125/seat/mo, or $100/seat/mo annual | Standard + 5x usage |
| **Enterprise** | Custom; reported **$20/seat/mo minimum** + API usage billed separately | SSO, SCIM, audit logs, compliance APIs, HIPAA options, no training on user content |

Note: anthropic.com/pricing now redirects to **claude.com/pricing**; docs.anthropic.com redirects to **platform.claude.com**.

---

## 2. API Pricing (per million tokens, USD)

### Standard rate card

| Model | Input | 5-min Cache Write | 1-hr Cache Write | Cache Hit | Output |
|---|---|---|---|---|---|
| Claude Fable 5 *(new, verify)* | $10 | $12.50 | $20 | $1 | $50 |
| Claude Mythos 5 *(new, limited availability)* | $10 | $12.50 | $20 | $1 | $50 |
| Claude Opus 4.8 / 4.7 / 4.6 / 4.5 | $5 | $6.25 | $10 | $0.50 | $25 |
| Claude Opus 4.1 *(deprecated)* / Opus 4 *(retired except Vertex)* | $15 | $18.75 | $30 | $1.50 | $75 |
| Claude Sonnet 4.6 / 4.5 | $3 | $3.75 | $6 | $0.30 | $15 |
| Claude Sonnet 4 *(retired except Bedrock/Vertex)* | $3 | $3.75 | $6 | $0.30 | $15 |
| Claude Haiku 4.5 | $1 | $1.25 | $2 | $0.10 | $5 |
| Claude Haiku 3.5 *(retired except Bedrock/Vertex)* | $0.80 | $1 | $1.60 | $0.08 | $4 |

Caveat: Fable 5 / Mythos 5 are very recent (~June 9, 2026) and unverified beyond official docs + secondary press; one report claims access was briefly suspended days after launch — confirm before citing.

Tokenizer note: Opus 4.7+ uses a new tokenizer that can use up to 35% more tokens for the same text vs. earlier models — factor in when comparing costs across generations.

### Prompt caching (multiplier on base input price)

| Operation | Multiplier | Duration |
|---|---|---|
| 5-min cache write | 1.25x | 5 min |
| 1-hr cache write | 2x | 1 hr |
| Cache hit/read | 0.1x | same as write |

Pays off after 1 read (5-min cache) or 2 reads (1-hr cache). Stacks with Batch and data-residency multipliers.

### Batch API (flat 50% off input + output)

| Model | Batch Input | Batch Output |
|---|---|---|
| Fable 5 / Mythos 5 | $5 | $25 |
| Opus 4.8 / 4.7 / 4.6 / 4.5 | $2.50 | $12.50 |
| Opus 4.1 / Opus 4 | $7.50 | $37.50 |
| Sonnet 4.6 / 4.5 / 4 | $1.50 | $7.50 |
| Haiku 4.5 | $0.50 | $2.50 |
| Haiku 3.5 | $0.40 | $2 |

### Other levers

- **Fast Mode** (Opus only, research preview): Opus 4.6/4.7 = $30 in/$150 out; Opus 4.8 = $10 in/$50 out (price cut at 4.8). No Batch/AWS combo.
- **Data residency**: forcing US-only inference adds a 1.1x multiplier (Opus 4.6+, Sonnet 4.6+). Global routing = standard price.
- **Long context (1M tokens)**: Fable 5, Mythos 5, Opus 4.8/4.7/4.6, Sonnet 4.6 include the full 1M window at standard rates — no surcharge.
- **Tool use**: tool schemas add input tokens; auto-injected tool-system-prompt ~290–675 tokens.
- **Web search tool**: $10 per 1,000 searches + standard token costs.
- **Web fetch tool**: no extra charge beyond token costs.
- **Code execution**: free when paired with web search/fetch; standalone billed by execution time (5-min minimum), 1,550 free container-hours/month/org, then $0.05/hour/container.
- **Claude Managed Agents** *(new/niche SKU)*: standard token rates + $0.08/session-hour runtime, metered to the millisecond. Batch/Fast Mode/data-residency multipliers don't apply.
- **Claude Platform on AWS**: billed via AWS Marketplace "Claude Consumption Units" at $0.01/CCU.
- **Bedrock / Vertex AI**: generally mirrors first-party list price; regional/multi-region endpoints carry a 10% premium for Claude 4.5+ on Bedrock/Vertex.
- **Volume/enterprise discounts**: available case-by-case, no public rate card; academic/research discounts may also apply.

---

## 3. Claude Code

- **No separate price tag** for interactive use — bundled into Pro, Max, Team, and Enterprise, drawing from the same usage pool as Claude.ai chat.
- **API-key users** (no subscription) pay standard token rates from Section 2.
- **Official enterprise benchmark**: ~$13/developer/active day average; $150–250/developer/month typical; 90% of users stay under $30/active-day.
- **Cost controls**: workspace spend limits, `/usage-credits` monthly cap (Pro/Max), `/usage` breakdown, per-team-size TPM/RPM tuning (200k–300k TPM for 1–5 users down to 10k–15k TPM for 500+ users).
- **Cost levers**: auto-applied prompt caching, model selection per task (Sonnet/Opus/Haiku), extended-thinking budget tuning, context/compaction management.

**Caveat — unsettled billing change**: Anthropic announced (~May 14, 2026) splitting non-interactive/programmatic usage (Agent SDK, `claude -p`, GitHub Actions, third-party apps) into a separate "Agent SDK credit" (~$20 Pro / $100 Max-5x / $200 Max-20x, overage at API rates), planned for June 15, 2026 — then reportedly paused/reversed that same day. Status is fluid; confirm current state before using in customer-facing material.

---

## 4. Enterprise / Custom Deals

No public enterprise rate card — Anthropic directs prospects to sales@anthropic.com. Publicly visible shape:

- **Structure** (third-party inference, not Anthropic-confirmed): per-seat fee + committed annual token volume/spend (often discounted off list in exchange for commitment) + metered overage at standard/negotiated rates. Seat fees cited in the **$20–60/user/month** range; minimums (e.g., 50 seats) reported by aggregators only.
- **Officially confirmed**: Enterprise = Team features + custom terms, $20/seat/month minimum + API usage billed separately.
- **Named deals** (illustrate scale, not list pricing):
  - **Snowflake** — $200M multi-year deal embedding Claude (Sonnet 4.5) into "Snowflake Intelligence" for Snowflake's 12,600+ customers.
  - **Deloitte** — Anthropic's largest deployment to date: Claude rolled out to 420k–470k employees across 150 countries, plus a certification program for 15,000 staff and a "Claude Center of Excellence." No dollar figure disclosed.
  - **IBM** — reported partnership integrating Claude into IBM software; no deal-size figure found.

Caveat: seat-fee and committed-spend figures are third-party estimates/press disclosures, not an Anthropic rate card — fine for GTM scoping conversations, not for quoting as official pricing.

---

## 5. Notable Pricing Changes

- **Opus cut ~67%** at Opus 4.6 launch (Feb 2026): $15in/$75out (4.1) → $5in/$25out (4.5+); also dropped the long-context surcharge.
- **Haiku rose ~4x**: Claude 3 Haiku ($0.25in/$1.25out) → Claude 3.5 Haiku ($1in/$5out) as capability increased. (Third-party recap, not independently re-verified.)
- **Fast Mode cut ~67%** at Opus 4.8: $30/$150 → $10/$50 per MTok.
- **Fable 5 / Mythos 5 priced above Opus**: launched ~June 9, 2026 at $10in/$50out — 2x Opus 4.8 — the most expensive flagship tier Anthropic has shipped.

GTM talking point: flagship (Opus) pricing has trended flat-to-cheaper across generations even as capability rises — useful counter to "frontier AI always gets pricier" — though the new Fable 5/Mythos 5 tier complicates that narrative at the very top end.

---

## Sources

- [claude.com/pricing](https://claude.com/pricing) — official consumer/enterprise plan page
- [platform.claude.com/docs/en/docs/about-claude/pricing](https://platform.claude.com/docs/en/docs/about-claude/pricing) — official API rate card
- [code.claude.com/docs/en/costs](https://code.claude.com/docs/en/costs) — official Claude Code cost docs
- Third-party/press (deal scale, unconfirmed seat figures): Finout, Tygart Media, Morph, VendorBenchmark, Redress Compliance, SpendHound, Snowflake press release, CNBC, Anthropic news post, IT Pro, claudefa.st
- Full citations and per-claim sourcing: `research/pricing.md`
