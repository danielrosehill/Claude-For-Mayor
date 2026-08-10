---
description: Establish who actually holds the lever on a policy area — the jurisdiction map that gates every later proposal (stage 2a of the pipeline)
argument-hint: <policy-area>
---

Build the jurisdiction map for the policy area: **$ARGUMENTS**. Output goes to `policy/$ARGUMENTS/research/02-jurisdiction.md`.

**Load the `municipal-powers-analysis` skill and follow its method.** This command is that skill's execution; the skill carries the classes, the structure and the rules. The `municipal-policy-methodology` skill's evidence standards apply throughout.

This runs **before** the comparative review and before any proposal drafting. Everything downstream depends on it: the comparative review shops for instruments of a class we can actually hold, and the paper's vires gate is enforced against this document.

## Inputs

- The cleaned testimony for this area in `testimonies/`, in particular its **"Attributions to test"** list
- The scope notes in `policy/$ARGUMENTS/index.md`
- `context/powers/` — the city-wide powers primer, for the standing constraints and the bodies already mapped

## What to produce

The eight sections set out in the `municipal-powers-analysis` skill, with the lever table as the spine. Every lever classified **A** (municipal own motion) / **B** (municipal, needs approval) / **C** (shared) / **D** (national), each traced to a cited instrument.

## Rules

- **A power without a citation is not a power.** Unsourced attributions are marked `[UNVERIFIED — verify before publication]` and block stage advancement.
- Run the **precedent test** early: if another Israeli municipality has already done it, it is class A or B by demonstration whatever the legal analysis suggested, and the live question becomes why this city has not.
- Do not stop at class D. For every class-D lever, find the consultee point, the consent point, the land, or the permit — the places the municipality appears inside someone else's process. That is what turns a class-D problem into a real advocacy proposal instead of a complaint.
- Hunt actively for **unused class-A powers**. They get their own section, and finding one is the highest-value output this stage can produce.

## Finish by reporting

1. The **most available lever** found, and whether it has ever been used.
2. Any **unused class-A power** — flagged prominently.
3. What the map **rules out**, so the user knows which instincts from the testimony cannot be delivered by a mayor.
4. Whether the testimony's attributions were right, and where the accountability gap sits.

Then update the stage table in `policy/$ARGUMENTS/index.md`.
