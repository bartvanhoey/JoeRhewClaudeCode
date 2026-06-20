# JoeRhewClaudeCode

A GTM/sales-enablement knowledge base about Anthropic and Claude: sourced research notes distilled into condensed reference material for writing sales, marketing, and outbound content. This is a content repository, not a software project — there's no build, test, or lint pipeline.

## Structure

- **`research/`** — long-form, heavily-sourced research notes, one file per topic (company, products, pricing, competitive dynamics, personas, customer proof points, GTM motion/partnerships, leadership/policy, funding/business signals, recent news, voice & tone). Each file opens with a research date and method note, labels claims **[Stated]** (Anthropic's own language) or **[Inference]** (synthesis), and ends with a `Sources` list.
- **`contexts/`** — condensed, GTM-ready distillations of the research files, meant to be loaded as context when drafting actual sales/marketing copy. Each file ends with a `Sources` section pointing back to the research file(s) it was built from.
  - **`contexts/personas/`** — one file per buyer/user persona archetype (builder/developer, enterprise IT/security buyer, regulated-industry risk owner, knowledge worker, startup builder, educator, channel partner/SI), plus a `README.md` index.
- **`prompts/`** — reference screenshots.

## Usage notes

- Figures around pricing, valuation, headcount, and market share move fast — re-check against the cited sources before quoting anything externally.
- `contexts/messaging.md` and `contexts/outbound-voice.md` define how Anthropic-flavored copy should read (tone, recurring vocabulary, the claim → caveat → mitigation pattern, and per-persona differentiation framing) — use them as the style guide when drafting new GTM copy.
