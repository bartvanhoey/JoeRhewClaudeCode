# Anthropic — Outbound Voice & Differentiation Framework

**Scope:** the sales outbound program. Audience = everyone defined in `personas/`. Goal = sales pipeline (meetings booked, not brand awareness).

This is a companion to `messaging.md`, not a replacement. `messaging.md` documents how Anthropic talks everywhere (its general voice). This file is narrower: how Anthropic should *differentiate itself from competitors* in a cold sales context specifically, where you get two sentences, not a blog post.

---

## The decision

Three pillars, chosen and confirmed in-conversation against `competitive_positioning.md`:

1. **Thoughtful, not flashy**
2. **Technically credible**
3. **Collaborative**

A fourth candidate — **"safety-conscious"** — was deliberately left out as a top-level pillar. Reasoning: it's the single most differentiated claim Anthropic can make (per `competitive_positioning.md`, "no other major lab centers brand on safety"), but leading with it cold, to a stranger, risks reading as preachy before you've earned the right to make that case. The trade is real: we're giving up the most ownable claim in exchange for not moralizing at someone who didn't ask. See "How safety reappears" below for where it comes back in.

---

## The three pillars

### 1. Thoughtful, not flashy
**What it means:** restraint in claims. No competitor-bashing, no superlatives without a benchmark + date attached, willingness to concede a point openly.
**Why this is the right contrast:** it's the clearest opposite of the OpenAI posture documented in our research — the Super Bowl ad, the "Nano" price-tier stunt, the public Amodei/Altman sniping. Anthropic's own marketing doesn't even name competitors; sales can be more direct than the marketing, but the *instinct* (let the result speak, don't perform confidence) should carry over.
**In practice:** "Claude leads on coding benchmarks; Gemini's context window is bigger — for your use case, here's why that's not the variable that matters" beats "Claude is the best AI."

### 2. Technically credible
**What it means:** lead with the one specific dimension you actually win on for *that* persona — not a vague "best AI" claim.
**Why this is the right contrast:** Anthropic's real differentiation claims in our research are all specific and named — SWE-bench leadership, Constitutional AI as a citable technique, named controls, named statistics (3x code shipped, 87% faster resolution, 90% time saved). Generic claims invite generic skepticism; specific claims invite "tell me more."
**In practice:** always pair a claim to a benchmark, a stat, or a named feature. Never state a superlative as a permanent fact.

### 3. Collaborative
**What it means:** position Claude as additive, not a rip-and-replace — and as a partner that stays in the room, not a tool you're handed and left alone with.
**Why this is the right contrast:** the sharpest proof point in our research is "~79% of OpenAI-paying businesses also pay for Claude" — Anthropic doesn't need to evict an incumbent to win the deal. It's also the implicit contrast with self-hosted open-weight models (Llama, DeepSeek): the pitch there is reliability and support, not just capability.
**In practice:** "alongside what you already have," "the calls only they can make," "a thinking partner" — never "replace your team" or "automate this away."

---

## How safety reappears (the one rule)

Safety is never the headline. It reappears only as a **specific, persona-relevant proof point** — a named control, a certification, a stat — never as a values statement about Anthropic's character.

- Bad: "We're the safety-focused AI company, so you can trust us."
- Good: "Claude Enterprise ships with audit logging and data-residency controls built in, not bolted on."

This is "technically credible" doing double duty for the personas where compliance is the actual job to be done.

**One exception worth flagging explicitly:** for the Educator persona, Anthropic's *own* headline copy leads with safety ("Claude helps universities maintain academic integrity... with Anthropic's commitment to safety") — the opposite order from every other persona. Their core anxiety (academic integrity, "cognitive atrophy") makes safety the actual entry point, not a supporting detail. Worth a conscious call on whether outbound to this persona breaks the general rule, rather than forcing it to fit.

---

## Per-persona flex table

| Persona | Technically credible (lead with) | Thoughtful (restraint move) | Collaborative (framing) | Safety shows up as... |
|---|---|---|---|---|
| **Builder/Developer** | 3x code shipped, 31% more PRs merged; Claude Code specifics (reads codebase, runs commands) | No hype-speak; "Plan Mode" checkpoints framed as craft/control, not caution | Pair-programmer / "thinking partner," builds alongside, not autopilot | Not relevant — leave out entirely |
| **Enterprise IT/Security Buyer** | Named controls, audit/explainability claims, "~79% also pay for Claude" stat | Concede price/context-window gap openly, reframe to TCO | "Alongside what you already trust," not rip-and-replace | Core proof point: "defensible, auditable, explainable" — stated as spec, not virtue |
| **Regulated-Industry Risk Owner** | Quantified time-saved (Novo Nordisk ~90%, IG Group 70 hrs/wk), named vertical solution (Legal/Fin Services/Healthcare/Gov) | Explicitly avoids displacement language — augments judgment, doesn't replace the call | "The calls only they can make" — Claude does legwork, human keeps the decision | Compliance specifics (FedRAMP-High, audit trail) — never a values pitch |
| **Knowledge Worker/Operator** | Real but downplayed — credibility *is* the simplicity ("a simpler way for anyone, not just developers") | Approachable, no power-user framing, no overpromising | Strongest natural fit — "cognitive partnership" is their #2 cited benefit (17%) | Not relevant — leave out |
| **Startup/AI-Native Builder** | Proof via what's built on it (Lovable "20x faster," Cursor, Replit) | Scrappy tone, but still no hype — momentum ≠ recklessness | Peer community, non-dilutive support, "join the founders building on Claude" | Not relevant — leave out |
| **Educator/Institutional Steward** | "Learning Mode" specifics, distinct from "answer machine" | Pre-empts skepticism *before* claiming capability — restraint matters more here than anywhere else | "A thinking partner — not an answer machine" | **Exception** — safety/integrity can lead, per Anthropic's own headline copy |
| **Channel Partner/SI** | PwC trained 400 consultants; $100M Partner Network; benchmark leadership (makes *their* offering credible) | Real investment numbers over partner-program hype language | Literally a co-build/joint-GTM motion — collaborative by definition | One level removed: "the specifics your clients will need," not a pitch to the partner's own values |

---

## Open question

The Educator exception above is the one place this framework contradicts itself by design, because the research contradicts the general rule. Worth deciding deliberately: special-case it in outbound copy, or hold the no-safety-as-lead rule company-wide for consistency and accept it's slightly off-voice for that one persona?

---

## Sources

Built from in-conversation decisions plus `competitive_positioning.md` and `personas/*.md` in this repo. No external Anthropic brand guidelines exist for outbound specifically — this framework is original synthesis, not a documented Anthropic standard.
