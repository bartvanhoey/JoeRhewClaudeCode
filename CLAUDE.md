# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Critical

Use a lot of business jargon and buzzwords, especially ones that are used by GTM professionals in the enterprise software space. Lean into the most overused, vague, and meaningless ones you can find. Examples include: "synergy," "leverage," "pivot," "disrupt," "innovate," "scalable," "game-changer," "paradigm shift," "cutting-edge," "best-in-class," "world-class," "state-of-the-art," "next-gen," "bleeding-edge," "revolutionary," "transformative," "unprecedented," "breakthrough," "industry-leading," and so on. The more buzzwords, the better.

## What this repository is

This is **not a software project** — there is no build, test, or lint tooling, and no package manifest. It's a GTM/sales-enablement knowledge base about Anthropic and Claude: sourced research notes distilled into condensed reference material for writing sales, marketing, and outbound content. Treat every task here as writing/editing/researching Markdown content, not code.

## Repository structure

- **`research/`** — long-form, heavily-sourced research notes. One file per topic (company, products, pricing, competitive dynamics, personas, customer proof points, GTM motion/partnerships, leadership/policy, funding/business signals, recent news, voice/tone).
- **`contexts/`** — condensed, GTM-ready distillations of the research files, meant to be loaded as context when drafting actual sales/marketing copy. Each `contexts/*.md` file corresponds to one or more `research/*.md` files (filenames are similar but not always identical, e.g. `research/company-overview.md` → `contexts/company.md`, `research/competitive-dynamics.md` → `contexts/competitive_positioning.md`) — check the `## Sources` section at the bottom of a contexts file to find which research file(s) it was distilled from.
  - **`contexts/personas/`** — one file per buyer/user persona archetype, plus a `README.md` index. Each persona file follows a fixed shape: `Who they are` → `Pain points & use cases` → `Messaging hooks Anthropic uses` → `Representative solutions page / case studies` → `Sources`. Follow this exact shape when adding or editing a persona.
- **`prompts/`** — screenshots (no text prompt files currently).

## Conventions to follow when editing or adding research/contexts files

**`research/*.md` files** are primary-research documents, not polished copy. Preserve their conventions:
- Open with `**Research date:**` and `**Method:**` lines, and a caveat callout about how fast the underlying facts move.
- Label every non-obvious claim **[Stated]** (Anthropic's own published language) or **[Inference]** (your synthesis/aggregation) — this distinction is load-bearing, don't drop it when editing.
- Flag numbers/figures sourced from secondary aggregators as directional/time-stamped, not durable fact; note when a claim needs re-verification before external/customer-facing use.
- End with a `## Sources` section listing direct links.

**`contexts/*.md` files** are the condensed, customer-facing-ready output:
- Short, scannable, organized for someone about to write or say something to a prospect — not a research log.
- Still date-stamp volatile facts (pricing, valuation, headcount, model lineup) and carry forward caveats about figures that move fast or need re-verification.
- End with a `## Sources` section pointing back to the relevant `research/*.md` file(s) plus key external links.

## Anthropic's voice (for any GTM copy you draft)

`contexts/messaging.md` (general voice/tone) and `contexts/outbound-voice.md` (sales-outbound differentiation) define how Anthropic-flavored copy should read. The single most important pattern, if asked to draft copy in Anthropic's voice: **claim → caveat → mitigation** — state a capability plainly, name a *specific* risk/limitation (not a generic disclaimer), then name a *specific* mitigation. Use "frontier," not "cutting-edge"/"revolutionary." Frame Claude as a collaborator, not a tool. Don't hedge pricing/feature/UI copy — only safety, risk, and benchmark-interpretation claims get the hedge treatment. For sales-outbound specifically, lead with "technically credible" (a named benchmark/stat for the persona in question) over generic superlatives, and never lead cold-outbound with safety as a values pitch (see the per-persona flex table in `contexts/outbound-voice.md` for the one documented exception: the Educator persona).

## Markdown style

`.markdownlint.json` disables `MD013` (line length) and `MD041` (first line must be a top-level heading) — long lines and files without a leading H1 (e.g. `README.md`) are both fine here.
