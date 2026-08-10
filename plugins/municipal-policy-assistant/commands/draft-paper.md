---
description: Synthesize a policy area's research into a think-tank-style Typst policy paper with compiled PDF (stage 3 of the pipeline)
argument-hint: <policy-area>
---

Draft the policy paper for: **$ARGUMENTS**. This is the think-tank product — the document a serious reader judges the project by. Follow the `municipal-policy-methodology` skill.

## Preconditions

Stop and report instead of drafting if any of these fail:

- All six research documents exist in `policy/$ARGUMENTS/research/`.
- No outstanding `[UNVERIFIED]` verification debt in `05-data.md`.
- `02-jurisdiction.md` exists and classifies its levers. **A paper cannot be drafted against an unmapped policy area** — without the classification there is no way to tell a commitment from a wish.

## Structure

Write `site/public/papers/$ARGUMENTS.typ` using the house template:

```typst
#import "../../../templates/policy-paper.typ": policy-paper, recommendation, tradeoff
```

Assign the next sequential paper number (`MP-001`, `MP-002`, … — check existing papers). The paper's sections:

1. **Executive summary** (template `abstract` + `key-findings`) — the whole argument in half a page, including how many of the recommendations the municipality can act on alone.
2. **The problem** — quantified, drawing on the problem statement; the testimony appears as a boxed or quoted case study, clearly labeled as one household's experience. Disaggregate by neighbourhood where the data allows.
3. **Who holds the lever** — from `02-jurisdiction.md`. A short, plain section stating what the municipality can do, what needs a ministry, and what is not the city's at all. **This section goes before the proposals, not in an annex.** It is the paper's distinguishing feature and the reason its promises can be believed.
4. **What is in place today and why it falls short** — from `03-municipal-instruments.md` and `06-city-hall-record.md`, including the recurring failure mode the record identifies.
5. **What works elsewhere** — from `04-comparative.md`, with the Israeli comparators first.
6. **Proposals** — each as a `#recommendation[...]` box containing:
   - **the class** — A (municipal own motion) / B (municipal, needs approval) / C (shared) / D (advocacy). Every recommendation carries one. No exceptions, and no proposal enters the paper without a named instrument.
   - **the mechanism** — which bylaw, tender clause, licensing condition, budget line, council decision or plan changes, and which department administers it.
   - **the cost and who pays** — order-of-magnitude honest, marked as an estimate, stated against a named budget line. Anything relying on arnona income addresses the approval constraint.
   - **the route and the elapsed time** — what the council can resolve at its next meeting, what needs the Interior Ministry, what needs a tender cycle. Give realistic timescales.
   - **the failure mode it is designed against** — from the record research. If the city's pattern is "adopted and never funded", say how this one avoids that.
7. **Trade-offs and objections** — each strongest objection as a `#tradeoff(objection, response)`. Steelman: argue the objection as its best advocate would, including the neighbourhood that loses and the department that has to absorb the work.
8. **Sources** — footnotes throughout (`#footnote[...]`); every factual claim traceable.

## Honesty checks before compiling

- Count the recommendations by class and state the tally in the executive summary. A paper that is mostly class D is an advocacy document and must present itself as one.
- Every class-A recommendation should answer, somewhere, why the municipality has not already done it.
- No promise without a mechanism; no mechanism without a funding source.

## Build and check

1. Compile: `typst compile site/public/papers/$ARGUMENTS.typ` — must compile with zero warnings.
2. Render page 1 to PNG (`typst compile --format png --ppi 100 ...`) and inspect it visually; fix layout problems (overflow, orphaned headings, broken boxes).
3. Commit both `.typ` and `.pdf`. The PDF is served at `/papers/$ARGUMENTS.pdf`.
4. Update the stage table in `policy/$ARGUMENTS/index.md` and note the paper number, then keep `policy/index.md`, `tasks.md`, `README.md` and `site/src/pages/index.astro` in step.
