# Startup Opportunity Research Prompt

A structured prompt for using an LLM (with web search) to identify a revenue-generating
startup opportunity for a solo, capital-constrained, technically strong founder.

## Contents

- `PROMPT.md` — the prompt as-is.
- `NOTES.md` — critique and suggested improvements (not yet merged into the prompt).

## Usage

Best run with a model that has live web search / research capability (not from
training data alone), since the whole method depends on current Reddit threads,
current competitors, and 2025–2026 startup launches.

Because this asks for 10 sequential research stages in one shot, consider running
it in phases rather than as a single call:

1. Steps 1–3 across several candidate problems (breadth pass).
2. Steps 4–5 (competitive research + gap-finding) on the 3–5 survivors — this is
   the stage most likely to get shortchanged if run in one pass.
3. Steps 6–10 + final output on the finalists.

## Known gaps (see NOTES.md for detail)

- No founder-market-fit / domain-background input.
- No explicit exclusion list (e.g. regulated verticals you don't want to own the
  compliance burden for).
- No time-to-revenue or revenue target to calibrate "realistic."
- Citation requirement is a single soft line; strengthen if you want inline links.
