---
title: Policy Development Pipeline
description: "How raw experience becomes a program for the city: four stages, each with a defined artifact and a quality bar it must clear — and one gate that has no national equivalent."
sidebar:
  label: The pipeline
  order: 1
---

How raw experience of living in a city becomes a program for governing it. Every policy area
moves through the same stages, each with a defined artifact and a bar it must clear. The stages
are automated by the [municipal-policy-assistant plugin](./method/plugin.md).

## The stage that only exists here

This pipeline is a fork of [MK-Claude](https://github.com/danielrosehill/MK-Claude), which does
the same work at national level. One stage was added, and it changes the character of everything
downstream.

A national platform can propose anything, because a national government can in principle
legislate anything; the argument is about whether it is a good idea. A mayor's platform cannot.
**Most of what residents blame City Hall for is not City Hall's to fix, and a good half of what
City Hall could fix tomorrow nobody asks it to.** Establishing which is which is not a
preliminary to the policy work — it is the policy work.

So before any proposal is drafted, every lever in a policy area is traced to a cited instrument
and classified. The rule is set out in full in [the powers doctrine](./method/powers-doctrine.md),
and it gates the policy paper: no recommendation is published without a named instrument, a
named holder of it, and a class letter.

## The stages

```
raw testimony (private)
        │  /capture-testimony
        ▼
testimonies/YYYY-MM-DD-<area>.md         dated, cleaned, redacted
        │
        │  /map-powers <area>            ← the gate
        ▼
policy/<area>/research/02-jurisdiction.md
        │                                every lever, cited and classified A/B/C/D
        │  /research-policy <area>
        ▼
policy/<area>/research/                  the evidence base
├── 01-problem-statement.md              testimony synthesised with quantified data
├── 02-jurisdiction.md                   who actually holds each lever
├── 03-municipal-instruments.md          what is on the books today, and where it fails
├── 04-comparative.md + comparative/     what other cities did, and whether we could
├── 05-data.md                           CBS, the city's own budget, the yearbook
└── 06-city-hall-record.md               what this city already tried, and why it failed
        │
        │  /draft-paper <area>
        ▼
../../../public/papers/                  the think-tank product, served for download
├── <area>.typ                           Typst source (house template)
└── <area>.pdf                           compiled policy paper
        │
        │  /update-platform
        ▼
platform/program-for-the-city.md         rolled up from all papers, sorted by deliverability
```

Paths are relative to the content root, `site/src/content/docs/` — the same tree the site is
built from, so every document is both a source file in the repository and a page here.

## The context layer

Running alongside the four stages, `context/` records the political ground truth the platform is
written against — the electoral situation, the council as it stands, the standing map of
municipal powers, and what every faction proposes. It is not a pipeline stage; it is the baseline
that makes gap analysis possible.

```
context/
├── the-election/     the municipal electoral system, the last result, the next one
├── city-hall/        the current council, its factions and coalition, the mayor's record
├── powers/           the standing powers primer — bodies, instruments, constraints
└── matrices/         policy comparison matrices, one per area  ← /compare-council
```

The matrix answers a question a policy paper cannot answer about itself: *is this proposal
actually needed, actually distinctive, actually passable?* Proposals that turn out to be already
adopted, already promised by four other factions, or dead on arrival with a blocking bloc get
reframed or dropped. See [the context layer's rules](./context/index.md) for the evidence
standards, which include rating our own column on the same scale as everyone else's.

## The holding area

Not everything worth writing down is a testimony, and stage 1 was originally the only way in.
`observations/` is the second door: a problem recorded without a first-person account behind it,
carrying a mandatory `origin` line that states exactly how it came to be on file.

```
observations/            problems with no testimony behind them, lineage stated
platform/spine.md        what the areas have in common, read before the gate
```

Neither is a pipeline stage and neither can advance anything. An observation is not evidence, and
**an area still opens only on testimony** — otherwise the project would start generating the
evidence it is supposed to be gathering. What an observation does is tell you which testimony is
worth going out and getting. The rules are in [observations](./observations/index.md).

`platform/spine.md` is the same idea one level up: eight areas opened in a day are describing
fewer than eight things, and naming the recurring mechanisms is analysis of what was said rather
than a claim about what can be done. It proposes nothing and carries no class letters, so it does
not touch the gate.

## Stage gates

A policy area does not advance until the current stage meets its bar:

| Stage | Artifact | Bar |
|-------|----------|-----|
| 1. Testimony | Dated markdown in `testimonies/` | Cleaned, redacted, frontmatter complete; attributions extracted for testing |
| 2a. Jurisdiction | `02-jurisdiction.md` | Every lever traced to a cited instrument and classified A/B/C/D; precedent test run against other Israeli municipalities; unused class-A powers identified |
| 2. Research | Six research documents | Every quantitative claim sourced or marked `[UNVERIFIED]`; bylaws and budget lines cited by name, date and clause; ≥4 comparator cities including ≥1 Israeli municipality and ≥1 instructive failure; city-hall record names a veto point and a recurring failure mode |
| 3. Paper | Typst source + PDF | Compiles clean; follows house template; every recommendation carries a class letter, a mechanism, a funding source and a route; steelmanned trade-offs section |
| 4. Platform | Section in the program | Sorted by deliverability; consistent with other planks; passes the department-capacity and council-arithmetic checks; no promise without a mechanism |

## Evidence rules

Non-negotiable, and applied at every stage. They are set out in full in
[the evidence rules](./method/evidence-rules.md) — no invented numbers, a municipal source
hierarchy that starts with the city's own published record, precise citation of subordinate
instruments, neighbourhood disaggregation, a named funding source for every cost, and a
mandatory trade-offs section in every proposal.
