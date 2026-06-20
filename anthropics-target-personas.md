# Anthropic's Target Personas

Anthropic doesn't publish an official persona framework. The table below is **inferred/synthesized** in `contexts/personas/` from public segmentation, role language, and case studies (see `contexts/personas/README.md`) — not a documented Anthropic standard.

| Persona | Who they are | Core need | Tone |
|---|---|---|---|
| **Builder/Developer** | Software engineers, technical founders — largest real usage base (~35-44% of Claude.ai/API traffic is Computer/Math occupations) | Ship faster, autonomy with checkpoints (Claude Code) | Builder/maker, speed & craft |
| **Enterprise IT/Security Buyer** | CIOs, CISOs, procurement/governance leads — the *economic buyer*, not the end user | Governed, auditable rollout; data residency, certs | Risk-mitigation, control |
| **Regulated-Industry Risk Owner** | Compliance officers, actuaries, GC/legal ops, clinical/regulatory staff (finance, healthcare, life sciences, legal, gov) | Defensible/auditable output; augment judgment, not replace it | Time-saved framing, avoids displacement language |
| **Knowledge Worker/Non-Technical Operator** | Analysts, ops, marketing, finance staff who don't code | Document-heavy work without dev tooling (Claude Cowork) | Accessible, "cognitive partnership" |
| **Startup/AI-Native Builder** | Early-stage, often VC-backed founders building on the API | Speed to PMF, non-dilutive credits, community | Scrappy, momentum-focused |
| **Educator/Institutional Steward** | University faculty/admins, ed-tech buyers | Academic integrity, "cognitive atrophy" anxiety | Safety/pedagogy first — rare case where safety *leads* |
| **Channel Partner/SI** | Big consultancies (PwC, Accenture, Deloitte) and vertical SIs (JAKALA) reselling/implementing Claude | Train/certify teams at scale, joint-GTM economics | Co-build, partner-program language |

Notable pattern across all seven: each gets deliberately different framing — speed for builders/startups, governance for IT buyers, augmentation-not-automation for regulated industries, simplicity for non-technical operators, safety-first only for educators.

## Sources

Full detail and sourcing per persona: `contexts/personas/*.md`. Raw research: `research/personas.md`.
