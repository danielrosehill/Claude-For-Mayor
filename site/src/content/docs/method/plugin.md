---
title: The Claude Code plugin
description: municipal-policy-assistant — the Claude Code plugin that runs this pipeline, with a command per stage, four method skills, and direct tool access to Israeli CBS statistics.
sidebar:
  label: The Claude Code plugin
  order: 3
---

The pipeline is not a document describing how the work *should* be done. It is executable: every
stage is a [Claude Code](https://claude.com/claude-code) slash command, shipped in this
repository as a plugin called **municipal-policy-assistant**.

That matters for the experiment. If the methodology lives only in prose, nothing enforces it and
the evidence bar erodes under deadline. If it lives in a command, the bar is applied on every
run, to every policy area, whether or not anyone is watching. The
[powers doctrine](./powers-doctrine.md) in particular is the kind of rule that is easy to agree
with and easy to skip; `/draft-paper` refuses to run on an unmapped area, which is a more
reliable form of agreement.

## Install it

```
/plugin marketplace add danielrosehill/Claude-For-Mayor
/plugin install municipal-policy-assistant@claude-for-mayor
```

The plugin is not Jerusalem-specific in structure — the stage model, the A/B/C/D classification
and the comparative method transfer to any city. The statistics server, the source hierarchy and
the arnona constraint are Israeli.

## Commands

| Command | Stage | What it does |
|---------|:-----:|--------------|
| `/capture-testimony` | 1 | Turns a raw dictation or transcript into a dated, cleaned, redacted testimony. Enforces the redaction and frontmatter rules, updates the index, and creates the policy-area tracker. Extracts two lists: facts to establish, and **attributions to test**. |
| `/capture-observation` | — | Records a problem with no testimony behind it into [`observations/`](../observations/index.md), establishing its lineage *first* and refusing to write without one. Deliberately cannot open a policy area — only testimony does that. |
| `/map-powers <area>` | 2a | Builds the jurisdiction map — every lever traced to a cited instrument and classified A/B/C/D, with a dedicated hunt for municipal powers that exist and are not being used. |
| `/research-policy <area>` | 2 | Builds the six-document evidence base. Web research, not recall — every quantitative claim is sourced or marked `[UNVERIFIED]`. |
| `/draft-paper <area>` | 3 | Compiles the evidence into a Typst policy paper against the house template, with class-tagged, costed proposals and a steelmanned trade-offs section. Refuses to run on an unmapped area or one carrying verification debt. |
| `/update-platform` | 4 | Rolls the completed papers into the program for the city, sorted by deliverability, with cross-plank coherence, department-capacity and council-arithmetic checks. |
| `/compare-council <area>` | — | Builds the [comparison matrix](../context/matrices/index.md) for an area: what every council faction proposes, **how it actually voted**, and where our proposal sits — rated on the same scale as everyone else's. |

## Skills

Four skills carry the method, loaded automatically when the relevant work starts:

- **`municipal-policy-methodology`** — the stage model, the artifacts, the frontmatter schemas,
  the [evidence rules](./evidence-rules.md), the money discipline and the neighbourhood rule.
- **`municipal-powers-analysis`** — the [powers doctrine](./powers-doctrine.md) as a working
  method: enumerate levers before assigning them, trace each to a cited instrument, map the other
  actors by name, find the consultee and consent points, check money separately from power, and
  test the classification against what other Israeli municipalities have already done.
- **`comparative-city-research`** — how to choose comparator cities for *instrument availability*
  rather than prestige, and how to write a case study that says whether we could do the same
  thing, not merely that someone did it.
- **`city-hall-record-research`** — how to establish what this city already tried, why each
  attempt failed, and who the veto point was, out of protocols, budgets, tenders and the
  municipal auditor.

## The statistics server

The plugin bundles an MCP server —
[israel-statistics-mcp](https://github.com/reuvenaor/israel-statistics-mcp) — giving Claude
direct tool access to Israeli Central Bureau of Statistics (הלשכה המרכזית לסטטיסטיקה) index data:
price indices, time series, and the official inflation-linkage calculator. No API key is required.

CBS is not the whole municipal picture — the municipality's own budget and protocols sit above it
in [the source hierarchy](./evidence-rules.md), and those have to be fetched and read rather than
queried — but it is the difference between a sourced statistical annex and a plausible-sounding
one.

## Source

The plugin lives at
[`plugins/municipal-policy-assistant/`](../../../../../plugins/municipal-policy-assistant/) in
the repository. Its commands and skills are plain Markdown — worth reading if you want to see
exactly what standards are being enforced, or to argue that they are the wrong ones.
