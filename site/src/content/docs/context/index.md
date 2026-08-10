---
title: Context
description: "The ground truth the platform is written against: the municipal electoral system, the council as it stands, the standing map of municipal power, and what every faction proposes."
sidebar:
  label: Overview
  order: 1
---

The ground truth the platform is written against.

Stages 1–4 of the [pipeline](../pipeline.md) build *our* policy. This directory records
everything that constrains it — how the city is elected, who currently governs it, what a
municipality is and is not able to do, and what the other factions are promising. It exists for
four reasons:

1. **The powers baseline.** Every policy area's jurisdiction map starts from the standing one in
   [powers](./powers/index.md) rather than rebuilding it, and adds the area-specific levers.
2. **Gap analysis.** A proposal is only worth making if it is not already adopted, already
   promised by five factions, or already tried and dropped. The
   [comparison matrices](./matrices/index.md) are how we check.
3. **Honest positioning.** Where another faction has a good policy, we say so and adopt it. Where
   ours is genuinely distinct, we should be able to point at the row in the matrix that proves
   it.
4. **Falsifiability.** Claims about "nobody is addressing X" are checkable claims. They get
   sourced like any other.

## Structure

```
context/
├── the-election/     The municipal electoral system, the 2024 result, the next election
├── city-hall/        The current council: factions, coalition, the mayor and his record
├── powers/           The standing powers primer: bodies, instruments, constraints
└── matrices/         Policy comparison matrices, one per policy area
```

## Rules

These carry the same evidence standards as the policy research (see the
`municipal-policy-methodology` skill):

- **Everything is dated.** Council coalitions shift mid-term, factions split, and officials move.
  Every factual claim states *as of* when, and files carry a `last-verified` date in frontmatter.
- **The voting record outranks the platform.** Council votes are recorded in the protocols, they
  are recent, and they concern the actual instruments in play. Where a faction's votes and its
  published material conflict, both are shown and the conflict is the finding.
- **Positions are quoted, not paraphrased into our framing.** If a faction's position is vague,
  the matrix cell says "vague" and quotes the vague text — it does not silently steelman or
  strawman it.
- **No score without a criterion.** If a matrix rates positions, the rating scale is defined in
  the matrix file and applied identically across factions, including to our own column.

## Our own column

Every matrix includes a column for this project's proposal, held to the same standard and rated
on the same scale — including on deliverability, against the same A/B/C/D classes from
[the powers doctrine](../method/powers-doctrine.md). A comparison matrix in which the author's
own policy wins every row is marketing, not analysis. Where another faction's instrument is
better than ours, the matrix says so and the policy paper is expected to change.
