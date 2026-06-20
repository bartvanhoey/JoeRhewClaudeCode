# Anthropic — Macro Narrative

The company's orientation: what it believes, why it exists, and why it needs to be at the frontier now. For day-to-day messaging style/voice, see `messaging.md`. For leadership bios and org structure, see `company.md`.

---

## Mission

Anthropic describes itself as **"an AI safety and research company"** building "reliable, interpretable, and steerable AI systems." The throughline across its own materials:

> "We believe AI will have a vast impact on the world."

> "Anthropic's mission is to ensure the world safely makes the transition through transformative AI."

A more human-centered variant it also uses: "we build AI to serve humanity's long-term well-being."

Two operating principles from the Company page do most of the work in explaining how that mission cashes out in practice:
- **"Act for the global good"** — optimize decisions for humanity's long-run interest, not just the company's.
- **"Ignite a race to the top on safety"** — use competitive pressure deliberately, to make safety (not just capability) the thing labs compete on.

Anthropic also frames itself as one actor among many ("AI companies are one piece of a big puzzle"), not the sole arbiter of how AI should go.

**Structural backing:** Anthropic is a Delaware **public benefit corporation**, with a stated purpose of "the responsible development and maintenance of advanced AI for the long-term benefit of humanity." This is reinforced by a **Long-Term Benefit Trust** — financially disinterested trustees with eventual influence over the board — designed to make the mission a governance fact, not just marketing copy.

Source: [Company \ Anthropic](https://www.anthropic.com/company)

---

## Why Anthropic Exists (Founding Rationale)

Dario Amodei (VP of Research) and Daniela Amodei (VP of Safety & Policy), along with several OpenAI colleagues (Jared Kaplan, Jack Clark, Chris Olah, Ben Mann, Sam McCandlish, Tom Brown among the core group), left OpenAI in late 2020/early 2021 and founded Anthropic in February 2021 as a PBC, with ~$124M in seed funding.

The split was as much about **trust** as a specific policy disagreement. Dario Amodei:

> "When you don't share the same vision and don't trust someone, there is little value in continuing the argument."
(Widely reported as directed at then-OpenAI CEO Sam Altman.)

The substantive concern: the departing group believed OpenAI's safety work was losing ground to the push to commercialize and scale — that safety "couldn't keep up" with deployment pace. Anthropic was built to fuse frontier capability work and frontier safety work in one institution, with safety carrying real organizational weight rather than being bolted on downstream. In Anthropic's own words:

> "A major reason Anthropic exists as an organization is that we believe it's necessary to do safety research on 'frontier' AI systems. This requires an institution which can both work with large models and prioritize safety."

**Early proof point:** after finishing an early version of Claude in summer 2022, Anthropic chose not to release it — citing further safety testing needs and "a desire to avoid initiating a potentially hazardous race to develop increasingly powerful AI systems." They sat on a finished, competitive model rather than ship first.

Daniela Amodei on the human-centered intent behind the name and mission:
> "We want to contribute to making AI systems safer from day one." / "There are real risks to artificial intelligence, we need to mitigate those risks, but if we're able to do that, the potential upside is almost unbounded."

Sources: [Yahoo Tech](https://tech.yahoo.com/ai/claude/articles/dario-amodei-why-left-sam-174405308.html) · [Core Views on AI Safety \ Anthropic](https://www.anthropic.com/news/core-views-on-ai-safety) · [Wikipedia — Anthropic](https://en.wikipedia.org/wiki/Anthropic) · [Stripe Newsroom — Daniela Amodei](https://stripe.com/newsroom/stories/anthropic-interview)

---

## Core Philosophy

### The central tension, stated plainly
> "We must make every effort to avoid accelerating dangerous technology deployment. But we also cannot let excessive caution prevent vital safety research from engaging frontier systems."

Anthropic's argument for why it has to build frontier models at all, rather than studying safety from the sidelines: "many of our most serious safety concerns might only arise with near-human-level systems" — so safety research has to happen *at* the frontier. Critics call this a convenient justification for competing with OpenAI/DeepMind anyway; Amodei has engaged the criticism directly rather than dodge it, arguing frontier safety testing also makes Anthropic's own models better.

### Constitutional AI
Anthropic's signature alignment technique: training models against an explicit, written set of principles (a "constitution") instead of relying solely on implicit human-feedback signal (RLHF). Goal: an AI that is "helpful, honest, and harmless," with values that can be "easily specified, inspected, and understood" rather than opaque.

Notably, Anthropic frames this as deliberately *not* wanting to be the sole arbiter of AI values:
> "Our long-term goal isn't trying to get our systems to represent a specific ideology, but rather to be able to follow a given set of principles."

The constitution was released under a CC0 license so others could adopt or adapt it — and Anthropic is explicit that it's a work in progress, not a finished doctrine: "our current constitution is neither finalized nor is it likely the best it can be."

Source: [Claude's Constitution \ Anthropic](https://www.anthropic.com/news/claudes-constitution)

### Responsible Scaling Policy (RSP)
Introduced September 2023; built around **AI Safety Levels (ASL)** — crossing defined capability thresholds triggers stricter safeguards. Anthropic implemented **ASL-3** safeguards (chem/bio weapon uplift protections) in May 2025, offered as proof the model is operationally workable, not just theoretical. Anthropic credits the RSP with shaping external policy, including California's **SB 53**, New York's **RAISE Act**, and parts of the **EU AI Act's Codes of Practice**.

A v3.0 rewrite separates Anthropic's own unilateral commitments from broader industry asks, and adds recurring public **Risk Reports** (every 3-6 months) plus **Frontier Safety Roadmaps**.

*Caveat:* some 2025-2026 press has framed the v3.0 rewrite as Anthropic "weakening" its safety pledge under competitive pressure. Anthropic disputes this, framing the rewrite as a transparency upgrade. Treat as a live, contested narrative rather than settled fact.

Source: [Responsible Scaling Policy \ Anthropic](https://www.anthropic.com/responsible-scaling-policy)

### "Race to the top," not "race to the bottom"
Anthropic's standing answer to "aren't you just racing like everyone else?" From Dario Amodei's 2023 Senate testimony:
> "We want to trigger a 'race to the top' on safety. If we implement safety measures and they work, other companies will be pressured to follow."

And on the alternative:
> "When you have a race to the bottom, it doesn't matter who wins. Everyone loses."

The logic chain: frontier AI is coming regardless of any one lab's choices → it's better for the world if the labs at the frontier are safety-focused → therefore Anthropic should be at the frontier, prove safety measures are commercially viable, and use competitive and regulatory pressure to pull the rest of the industry along.

Sources: [Senate Judiciary testimony, July 2023](https://www.judiciary.senate.gov/imo/media/doc/2023-07-26_-_testimony_-_amodei.pdf) · [Big Technology Podcast](https://singjupost.com/transcript-anthropic-ceo-dario-amodeis-interview-on-big-technology-podcast/)

### The worldview essays
Two long Dario Amodei essays form a deliberately matched pair — citing one without the other misrepresents the company's position:

- **"Machines of Loving Grace" (Oct. 2024)** — the optimistic case, built around a "country of geniuses in a datacenter": AI exceeding Nobel-laureate level across domains, run as millions of parallel instances. Predicts compressed biomedical progress (cures for cancer, infectious disease, Alzheimer's; "50-100 years of progress in 5-10 years"), 10-20% annual GDP growth in developing economies, and a democratic "entente strategy" for spreading the benefits — explicitly **not guaranteed**, since the same tools could entrench authoritarianism instead.

- **"The Adolescence of Technology" (Jan. 2026)** — the risk-focused companion. Core framing:
> "Humanity is about to be handed almost unimaginable power, and it is deeply unclear whether our social, political, and technological systems possess the maturity to wield it."

  Lays out five risk categories: autonomy/misalignment risk, mass-destruction misuse (bioweapons, the most catastrophic concern), misuse for seizing power (CCP-style authoritarian weaponization ranked as the top threat), economic disruption (entry-level white-collar displacement, potentially ~50% within 1-5 years), and indirect systemic effects. Amodei explicitly rejects "doomerism" as a frame while treating these as real, measurable engineering and policy problems.

Together, the two essays state Anthropic's official self-narrative: ambitious optimism about the upside, paired with sober realism about the risk — not pure boosterism, not pure doom.

Sources: [Machines of Loving Grace](https://darioamodei.com/essay/machines-of-loving-grace) · [The Adolescence of Technology](https://darioamodei.com/essay/the-adolescence-of-technology)

A related, shorter essay, **"The Urgency of Interpretability,"** makes the case that understanding *why* models behave as they do is itself a race against capability growth: "We are thus in a race between interpretability and model intelligence." It also supplies a useful one-line summary of Anthropic's stance on technological determinism: progress is "inexorable," but society retains the ability to **steer** how it unfolds.

Source: [The Urgency of Interpretability](https://darioamodei.com/post/the-urgency-of-interpretability)

---

## Policy & "Why Now" Positioning

Anthropic's regulatory posture is the practical extension of "race to the top": push for rules that lock in safety practices industry-wide, rather than relying on voluntary goodwill (including its own).

- **Favors mandatory disclosure over pure self-governance.** Supports legislation requiring companies to publish catastrophic-risk evaluations and safety-testing summaries — citing California's **SB 53** and the **EU AI Act Code of Practice** by name as models it has actually signed onto. Anthropic frames the EU Code as advancing "transparency, safety and accountability," consistent with its own RSP.
- **Supports strict export controls on advanced AI chips to China**, calling this "perhaps the most important single action we can take" to keep frontier AI development concentrated within the U.S. and allied democracies — a position repeated from the 2025 Paris AI Action Summit statement through "The Adolescence of Technology."
- **Engages government directly rather than avoiding it** — providing Claude access across all three branches of the U.S. government, signing agreements with allied nations, and backing well-funded evaluation capacity at bodies like NIST.
- **Acknowledges and funds responses to labor disruption** it expects its own technology to cause, via an "Economic Futures Program."
- **Most recent shift (June 2026): "Policy on the AI Exponential."** Dario Amodei's essay argues government policymaking moves far slower than AI capability does, and calls for **binding, enforceable regulation** of frontier models — explicitly modeled on aviation safety (mandatory third-party testing, government authority to block or reverse unsafe releases):
> "Frontier AI models, like airplanes, should be required to go through technical testing and auditing, and their release should be blocked or reversed as a threat to public safety if they do not meet high standards of safety."

  This marks a move beyond "transparency is enough" toward asking for real regulatory teeth — and arrived just before the U.S. Commerce Department issued an export-control directive against two of Anthropic's own models, a case where Anthropic found itself contesting the application of the same kind of authority it had just asked government to take on. Some critics have read the broader proposal as risking "regulatory capture" (setting a compliance bar smaller competitors may struggle to meet). Worth knowing as context for policy-literate audiences, not load-bearing for most GTM conversations.

**The "why now" case, in short:** Anthropic's argument is that frontier AI is coming on a 1-3 year timeline regardless of who builds it, the safety problems that matter most only show up in near-human-level systems, and government oversight is moving too slowly to catch up on its own — so a safety-focused lab has to be at the frontier, demonstrating and exporting safety practice via product, research, and policy, simultaneously.

Sources: [anthropic.com/policy](https://www.anthropic.com/policy) · [EU Code of Practice announcement](https://www.anthropic.com/news/eu-code-practice) · [Policy on the AI Exponential](https://darioamodei.com/post/policy-on-the-ai-exponential)

---

## Sources

1. [Company \ Anthropic](https://www.anthropic.com/company)
2. [Core Views on AI Safety \ Anthropic](https://www.anthropic.com/news/core-views-on-ai-safety)
3. [Claude's Constitution \ Anthropic](https://www.anthropic.com/news/claudes-constitution)
4. [Responsible Scaling Policy \ Anthropic](https://www.anthropic.com/responsible-scaling-policy)
5. [Machines of Loving Grace — Dario Amodei](https://darioamodei.com/essay/machines-of-loving-grace)
6. [The Adolescence of Technology — Dario Amodei](https://darioamodei.com/essay/the-adolescence-of-technology)
7. [The Urgency of Interpretability — Dario Amodei](https://darioamodei.com/post/the-urgency-of-interpretability)
8. [Policy on the AI Exponential — Dario Amodei](https://darioamodei.com/post/policy-on-the-ai-exponential)
9. [Senate Judiciary Committee testimony, July 26, 2023](https://www.judiciary.senate.gov/imo/media/doc/2023-07-26_-_testimony_-_amodei.pdf)
10. [anthropic.com/policy](https://www.anthropic.com/policy)
11. [EU Code of Practice announcement \ Anthropic](https://www.anthropic.com/news/eu-code-practice)
12. [Wikipedia — Anthropic](https://en.wikipedia.org/wiki/Anthropic)
13. [Stripe Newsroom — Daniela Amodei interview](https://stripe.com/newsroom/stories/anthropic-interview)
