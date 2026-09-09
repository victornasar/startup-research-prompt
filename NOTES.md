# Critique & Suggested Additions

## Strengths
- Step 1 draws a hard line between "annoying" and evidenced pain
  ("I spend 20 hours/week..."). This is the single highest-leverage instruction
  in the prompt — most idea-generation prompts skip it.
- Step 4 requires killing ideas that are already commoditized, with an explicit
  ban on "there's always room for another player" hand-waving.
- Step 9 rules out thin API wrappers as a valid answer — addresses the most
  common failure mode of AI-generated startup ideas right now.
- Final output format forces a single winner with a 30-day plan, not a list of
  options to choose from.

## Gaps worth closing before running this for real

1. **No founder-market fit input.** Add a block describing your actual
   background, industries you've worked in/adjacent to, and any weak-tie
   network (even "I know two people in logistics"). Step 7 assumes all
   identifiable markets are equally reachable by cold outreach, but reply
   rates differ a lot based on perceived credibility.

2. **No exclusion list.** Step 2 explicitly looks for regulatory/compliance
   burden as a pain *signal*, but nothing stops the model from recommending
   an opportunity where you'd personally inherit that burden (health data,
   licensed financial activity, etc.) with no capital or legal support to
   handle it. Add a "hard no" list.

3. **No time/revenue target.** "Revenue-generating" is undefined. Pin down
   something like "$3–5k MRR within 90 days, path to $30k MRR in a year" so
   the model can actually filter for realism instead of just plausibility.

4. **One-shot mega-prompt risk.** 10 sequential research stages in a single
   generation will likely under-invest in Steps 4–5 (the most important,
   least fun to do exhaustively). Consider splitting into a 3-phase run (see
   README).

5. **Soft citation requirement.** "Cite your sources" at the very end of a
   long prompt is easy to drop. If specific links matter, ask for them
   inline per claim, not as a general instruction.

## Optional addition block (not yet merged)

```
## MY BACKGROUND (for founder-market fit)
- Industries I've worked in or have exposure to: [fill in]
- Any weak-tie network I can use for first outreach: [fill in]
- Hard no's (won't build in these spaces even if pain is real): [e.g. healthcare data, consumer lending, anything requiring a broker license]
- Target: $X MRR within Y days as the bar for "realistic"
```
