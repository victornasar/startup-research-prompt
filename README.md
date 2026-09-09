# Startup Opportunity Research Prompt

A structured prompt for using an LLM (with web search) to identify a revenue-generating
startup opportunity for a solo, capital-constrained, technically strong founder.

## Contents

- `PROMPT_v2.md` — **use this one.** Adds founder context (solo dev, Claude +
  Cursor as primary leverage), an exclusion list, a revenue/timeline target,
  explicit phased execution, and per-claim citation requirements.
- `PROMPT.md` — original version, kept for reference.
- `NOTES.md` — critique that motivated the v2 changes.

## Before running v2

Fill in the three bracketed fields near the top of `PROMPT_v2.md`:

- Hard no's (spaces you won't build in even if the pain is real — e.g.
  anything requiring a securities/lending/insurance license, or a regulated-
  health first product)
- Background/network you can lean on for first outreach, even weak ties
- Adjust the $3–5k/90-day, $30k+/year targets if your bar is different

## Usage

Best run with a model that has live web search / research capability, since
the method depends on current Reddit threads, current competitors, and
2025–2026 startup launches.

v2 bakes in phased execution directly in the prompt: Phase 1 breadth (Steps
1–3 across 6–8 candidates), Phase 2 narrow (Steps 4–5 competitive research on
the top 4–5 — the stage most likely to get shortchanged), Phase 3 decide
(Steps 6–10 + final output). If your runtime supports multi-turn tool use,
let it actually run as three passes rather than compressing everything into
one generation.

## Known gaps closed in v2 (see NOTES.md for original detail)

- ~~No founder-market-fit / domain-background input~~ — added as a context block.
- ~~No explicit exclusion list~~ — added as a hard-no field.
- ~~No time-to-revenue or revenue target~~ — added ($3–5k/90 days default).
- ~~Citation requirement is a single soft line~~ — now required per claim, and
  Step 4 requires 3+ search phrasings before concluding whitespace exists.
