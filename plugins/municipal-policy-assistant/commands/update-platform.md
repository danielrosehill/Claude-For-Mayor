---
description: Roll completed policy papers up into the program for the city (stage 4 of the pipeline)
argument-hint: (no arguments — processes all completed papers)
---

Update the meta-proposal at `platform/program-for-the-city.md` from the completed policy papers.

## Rules

1. **Only stage-3-complete areas enter the program.** Check each `policy/<area>/index.md` stage table; skip areas without a compiled paper.

2. **The program is a distillation, not a concatenation.** Each policy area gets a section of roughly one page: the problem in two or three sentences, then the recommendations (numbered, cross-referenced to the paper, e.g. "MP-001 §6.2", **each carrying its A/B/C/D class**), then a one-line honest note on cost and losers. Readers who want the evidence go to the paper.

3. **Sort the whole program by deliverability, not by theme.** The reader's first question about a municipal platform is "which of this could you actually do?", and the document should answer it before it argues anything. Open with three tables:
   - **What the council can do on its own motion** — all class-A recommendations across every area, with their costs.
   - **What needs an approval, and from whom** — class B, with the approving body.
   - **What needs a partner or is advocacy only** — class C and D, with the counterpart named.

   A platform whose class-A table is short and whose class-D table is long is telling the truth about the office. Do not pad the first table by reclassifying.

4. **Coherence check across areas** — this is the step's real value:
   - Do any two areas' proposals conflict (fiscally, administratively, spatially, politically)?
   - **Do they compete for the same department?** Municipal delivery capacity is more binding than money. If four proposals all land on the same understaffed unit, that is a conflict even if each is individually funded.
   - Do the combined costs fit a plausible municipal budget envelope? Keep a running "total fiscal impact" table, stated as a share of the relevant budget lines rather than in absolute shekels alone.
   - Does anything depend on the same ministerial approval, such that one refusal takes out several planks?
   - Does every promise still have a mechanism? No aspirational language that a paper doesn't back.

   Record conflicts found in an "Open tensions" section at the end of the program rather than papering over them.

5. **The council arithmetic.** State, for the class-A and class-B recommendations, what majority they need and whether any plausible council coalition delivers it. See `context/city-hall/`. A program that cannot pass its own council is a finding worth publishing, not a reason to soften the program.

6. **Structure of the program document**: preamble (what this program is and how it was built, linking to `pipeline.md`) → the three deliverability tables → one section per policy area, ordered by the priority the papers justify → fiscal summary → council arithmetic → open tensions.

7. Finish by updating each included area's stage table (stage 4 ✅), keeping `policy/index.md`, `tasks.md`, `README.md` and `site/src/pages/index.astro` in step, and — if the program's priorities changed — noting why in the commit message.
