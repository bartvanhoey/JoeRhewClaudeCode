# Anthropic: Voice & Tone Guide

How Anthropic talks. For the mission/why, see `narrative.md` — this file is purely about register, vocabulary, and the rhetorical patterns to reproduce in GTM copy.

---

## 1. Overall tone

- **Measured-formal with selective warmth.** Mission/safety pages read like a careful research memo (long sentences, subordinate clauses, explicit qualification). Product pages (claude.com) loosen up — second-person, conversational, benefit-driven. Docs are plain and neutral. Social is the most casual but still restrained: no slang, minimal emoji, no hype-speak.
- **Code-switches by audience.** Safety/research content is precise and academic ("we aim to build frontier AI systems that are reliable, interpretable, and steerable"). Product copy strips jargon for a general audience. Docs sit in between.
- **Confident claims, voluntarily hedged — the single most distinctive trait.** Anthropic states strong/best-in-class claims plainly, then wraps them in caveats, risk disclosures, or admissions of uncertainty almost every time. This isn't false modesty — it reads as deliberate epistemic honesty, close to a house style rule.
- **Hedging is selective, not a blanket tic.** It's concentrated around safety/risk claims and claims about Claude's inner nature. Pricing, feature, and UI copy is plain and declarative — don't hedge that.

---

## 2. Recurring vocabulary and phrases

- **"Frontier"** — the house word for "most advanced" ("frontier AI systems," "frontier model," "safety at the frontier"). Using it signals fluency in Anthropic's own vocabulary.
- **"Safety" + "capability," paired** — almost every capability sentence is shadowed by a safety sentence nearby.
- **"Reliable, interpretable, and steerable"** — fixed triad describing the AI systems Anthropic wants to build.
- **"Helpful, honest, and harmless" (HHH)** — foundational values shorthand.
- **"Public Benefit Corporation"** — used structurally in self-identification.
- **"We believe"** — softens a strong assertion into a marked belief rather than a flat fact; lets them state bold views without overclaiming.
- **Risk-acknowledgment verbs**: mitigate, safeguard(s), misuse, robustly, steerable — cluster wherever new capability is introduced.
- **"Thinking partner" / collaboration framing** — Claude is consistently a collaborator, not a tool: "Meet your thinking partner," "expert-level collaboration," "like an expert in your pocket."
- **"Long-term well-being of humanity"** — recurring mission-level phrase.
- **"Hold light and shade"** — one of Anthropic's seven stated values; an unusual, literary way of saying "acknowledge AI's risks and benefits simultaneously rather than picking optimism or doom." Distinctive vs. competitors' blander "responsible AI" language — useful shorthand for the brand's defining move.
- **Avoid**: "revolutionary," "game-changing," "groundbreaking," and other hype adjectives — essentially absent from Anthropic's own copy. "State-of-the-art" / "best" appear only anchored to a named, citable benchmark, never asserted in the abstract.

---

## 3. The claim → caveat → mitigation rhythm (the core pattern)

This is the most distinctive and most important thing to reproduce. Nearly every capability announcement follows the same three-beat structure, often within one paragraph:

1. **Claim** — state the capability plainly, even a record-setting one.
2. **Caveat** — name a *specific* risk or limitation (not a generic disclaimer): a named risk category (cybersecurity misuse, prompt injection, nuclear proliferation) or a methodological limit of the claim itself (what the benchmark doesn't measure).
3. **Mitigation** — name the *specific* fix (a classifier, a safeguard, conservative tuning, a third-party partnership) — and be willing to admit its cost (e.g., "they'll sometimes catch harmless requests").

Example chain: *"Fable 5's capabilities exceed those of any model we've ever made generally available"* → *"Releasing a model this capable comes with risks. Without safeguards, Fable 5's capabilities in areas like cybersecurity could be misused"* → *"we've tuned these safeguards conservatively—they'll sometimes catch harmless requests."*

The specificity (named risk + named mitigation, not boilerplate legal language) is what makes this read as candor rather than CYA disclaimer-stuffing. Anthropic also routinely undercuts its own benchmark wins rhetorically (e.g., questioning what a record score actually means) — a credibility move that signals "we're not just marketing this."

**For GTM copy:** reproduce this rhythm deliberately. State the capability, then a specific limitation or risk, then a specific mitigation. Don't hedge generically and don't hedge pricing/feature copy — only safety, risk, benchmark interpretation, and claims about the model's "inner nature."

---

## 4. Representative snippets

1. **Mission tone, belief-framed:**
   "AI will have a vast impact on the world. Anthropic is a public benefit corporation dedicated to securing its benefits and mitigating its risks."
   — Homepage, https://www.anthropic.com/

2. **Safety humility, high hedge density:**
   "We founded Anthropic because we believe the impact of AI might be comparable to that of the industrial and scientific revolutions, but we aren't confident it will go well."
   — Core Views on AI Safety, https://www.anthropic.com/news/core-views-on-ai-safety

3. **Product tone, casual and partnership-framed:**
   "Meet your thinking partner. Tackle any big, bold, bewildering challenge with Claude."
   — Claude product overview, https://claude.com/product/overview

4. **Signature move — claim immediately undercut by methodological caveat:**
   "Within our prescribed 2-hour time limit, Claude Opus 4.5 scored higher than any human candidate ever... This result... raises questions... [the test] doesn't test for other crucial skills candidates may possess."
   — Claude Opus 4.5 announcement, https://www.anthropic.com/news/claude-opus-4-5

5. **Full claim → risk → mitigation chain:**
   "Fable 5's capabilities exceed those of any model we've ever made generally available... Releasing a model this capable comes with risks. Without safeguards, Fable 5's capabilities in areas like cybersecurity could be misused... we've tuned these safeguards conservatively—they'll sometimes catch harmless requests."
   — Claude Fable 5 / Mythos 5 announcement, https://www.anthropic.com/news/claude-fable-5-mythos-5

6. **Docs register — plain, neutral, instructional:**
   "Claude is a highly performant, trustworthy, and intelligent AI platform built by Anthropic. Claude excels at tasks involving language, reasoning, analysis, coding, and more."
   — Developer docs intro, https://platform.claude.com/docs/en/intro

---

## 5. Quick rules for writing GTM copy in this voice

- Lead with the capability claim, plainly stated — don't bury it in qualifiers.
- Pair it with a *specific* limitation or risk, not a generic disclaimer.
- Close with a *specific* mitigation, and don't be afraid to admit its cost/tradeoff.
- Use "frontier," not "cutting-edge" or "revolutionary."
- Frame Claude as a collaborator/partner, not a tool or assistant.
- Keep pricing, feature, and UI copy plain and confident — save the hedging for safety, risk, and benchmark-interpretation claims.

---

## Sources

Based on close reading in `research/voice-and-tone.md` of: Anthropic homepage, Claude product overview, Company page, Claude Opus 4.5 announcement, Claude Fable 5/Mythos 5 announcement, Core Views on AI Safety, Claude's Character, Claude's new constitution, developer docs intro, careers page, pricing/enterprise page, and @AnthropicAI on X.
