# Startup Opportunity Research Prompt

A structured prompt for using an LLM (with web search) to identify a revenue-generating
startup opportunity for a solo, capital-constrained, technically strong founder.

## Contents

- `PROMPT.md` — the research prompt. Includes founder context (solo dev, Claude +
  Cursor as primary leverage), an exclusion list, a revenue/timeline target,
  explicit phased execution, and per-claim citation requirements.

## Before running

Fill in the bracketed fields near the top of `PROMPT.md`:

- Hard no's (spaces you won't build in even if the pain is real — e.g.
  anything requiring a securities/lending/insurance license, or a regulated-
  health first product)
- Background/network you can lean on for first outreach, even weak ties
- Adjust the $3–5k/90-day, $30k+/year targets if your bar is different

## Usage

Best run with a model that has live web search / research capability, since
the method depends on current Reddit threads, current competitors, and
recent startup launches.

The prompt bakes in phased execution: Phase 1 breadth (Steps 1–3 across 6–8
candidates), Phase 2 narrow (Steps 4–5 competitive research on the top 4–5 —
the stage most likely to get shortchanged), Phase 3 decide (Steps 6–10 +
final output). If your runtime supports multi-turn tool use, let it actually
run as three passes rather than compressing everything into one generation.
