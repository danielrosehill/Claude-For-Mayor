---
title: Testimonies
description: First-person accounts of living in the city that anchor the policy work — evidence of experience, stress-tested against data.
sidebar:
  label: Overview
  order: 1
---

First-person accounts of living in Jerusalem that anchor the platform's policy work. Policy here
starts from lived experience, then gets stress-tested against data, against comparator cities,
and against the question of who actually holds the lever — not the other way around.

**Nine captured**, all from one dictated account on 10 August 2026 given in three sittings, and
between them they open the project's first eight policy areas. Who gave the account, and what it
cannot see, is set out in [whose account this is](../context/whose-account.md).

## Rules

1. **Only cleaned testimonies are committed.** Raw dictations, recordings, and transcripts stay
   out of the public repo. `testimonies-raw/` at the repository root is a gitignored staging area,
   deliberately kept outside the published content tree — drop raw material there for processing.
2. **Every testimony is dated** and named `YYYY-MM-DD-<policy-area>.md`. Where an area gains a
   second testimony on the same date, a short descriptive suffix is added —
   `2026-08-10-construction-disruption-pedestrian.md`.
3. **Cleaning preserves voice and facts.** Editing removes disfluencies and tightens prose; it
   never adds claims, softens them, or changes their substance.
4. **Redaction before commit.** Full names of private individuals, exact addresses, and
   identifying details of third parties are removed or generalized. Municipal testimony
   de-anonymises unusually easily — a street, a building, a school and a date together identify a
   household — so the default is to generalise to the neighbourhood.
5. **Frontmatter is mandatory**: `title`, `date`, `policy-area`, `status`, `source`.

Use the `/capture-testimony` command from the
[municipal-policy-assistant plugin](../method/plugin.md) to process a raw account into this
format.

## What a testimony is for, and what it is not

A testimony is **evidence of experience, not of prevalence**. One resident's street proves
something *can* happen; only data proves it is *common*. At city scale that distinction is sharper
than it is nationally, because a single neighbourhood's problem can be completely real and
completely unrepresentative — and the research stage is expected to find out which.

Testimonies also carry a second payload that is specific to municipal work. Every account
contains assumptions about **who is responsible** for the thing going wrong, and those
assumptions are frequently wrong in an interesting way. `/capture-testimony` extracts them as a
separate list of *attributions to test*, which goes straight to
[the jurisdiction map](../method/powers-doctrine.md). The gap between who residents blame and who
actually holds the lever is one of this project's more reliable findings, and it is not treated
as an error in the testimony — the testimony records what a resident believed, accurately.

## Index

| Date | Policy area | Testimony |
|------|-------------|-----------|
| 2026-08-10 | [renting](../policy/renting/index.md) | [Ten years renting in Jerusalem](./2026-08-10-renting.md) |
| 2026-08-10 | [housing-supply](../policy/housing-supply/index.md) | [A poor city building luxury towers](./2026-08-10-housing-supply.md) |
| 2026-08-10 | [construction-disruption](../policy/construction-disruption/index.md) | [Everything dug up at once](./2026-08-10-construction-disruption.md) |
| 2026-08-10 | [construction-disruption](../policy/construction-disruption/index.md) | [A diversion map like a plate of spaghetti](./2026-08-10-construction-disruption-pedestrian.md) |
| 2026-08-10 | [small-businesses](../policy/small-businesses/index.md) | [Shuttered shops, and nothing offered](./2026-08-10-small-businesses.md) |
| 2026-08-10 | [construction-noise](../policy/construction-noise/index.md) | [One hundred and ten decibels](./2026-08-10-construction-noise.md) |
| 2026-08-10 | [environmental-quality](../policy/environmental-quality/index.md) | [The horns, and the air](./2026-08-10-environmental-quality.md) |
| 2026-08-10 | [capital-priorities](../policy/capital-priorities/index.md) | [A bridge I have never used](./2026-08-10-capital-priorities.md) |
| 2026-08-10 | [buses](../policy/buses/index.md) | [An hour to Talpiot, four hours home](./2026-08-10-buses.md) |

All nine come from one household on one day. That is a real limitation and not a formality:
eight areas resting on a single vantage point is exactly the case where testimony gets mistaken
for prevalence, and the data annexes in stage 2 are what will have to carry them.

The concentration got worse rather than better on 10 August: six of the nine came from a second
sitting offered as a scattergun list, and a ninth from a third. Several are two or three sentences
long. Each area's tracker states how thin its own testimony is; none of them pretends otherwise.
