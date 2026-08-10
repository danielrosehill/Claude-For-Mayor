# Municipal Policy Assistant

A Claude Code plugin that turns first-person testimony about living in a city into evidence-based, think-tank-quality municipal policy papers — and ultimately a program for the city.

Built for (and shipped with) the [Claude-For-Mayor](https://github.com/danielrosehill/Claude-For-Mayor) experiment, but the pipeline is generic: it works for any project developing local-government policy from lived experience, grounded in the municipality's own budget and bylaws, official statistics and comparator cities, with a paper trail.

It is a sibling of [policy-development-assistant](https://github.com/danielrosehill/MK-Claude), which does the same job at national level. The difference is one stage, and that stage is the point — see below.

## Install

```
/plugin marketplace add danielrosehill/Claude-For-Mayor
/plugin install municipal-policy-assistant@claude-for-mayor
```

(Inside the Claude-For-Mayor repo itself the plugin is pre-enabled via `.claude/settings.json`.)

## Requirements

- [Typst](https://typst.app) on `PATH` (for compiling policy papers to PDF)
- Node.js / `npx` (for the bundled CBS statistics MCP server, below)
- A repo laid out per the pipeline — the commands will create the structure as they go

## The extra stage: who actually holds the lever

National policy work can propose anything and argue about whether it is a good idea. Municipal policy work cannot, because **most of what residents blame City Hall for is not City Hall's to fix, and a good half of what City Hall could fix tomorrow nobody asks it to.**

So this pipeline inserts a jurisdiction map before any proposal is drafted, and gates the paper on it. Every lever is traced to a cited instrument and classified:

| Class | Meaning |
|:-----:|---------|
| **A** | Municipality decides and funds — bylaw, council decision, tender clause, licensing condition, budget line, enforcement priority |
| **B** | Municipality decides, an external body must approve — ministerial confirmation, arnona deviation, district planning committee |
| **C** | Shared — delivery municipal, policy or funding national; the analysis finds the municipal leverage inside the arrangement |
| **D** | No municipal power — legitimate as **advocacy**, with a named counterpart and route; never as a promise |

Every recommendation in every paper carries its class letter, and the program for the city is sorted by class before it is sorted by theme. A class-D proposal presented as something a mayor can deliver is the standard dishonesty of municipal campaigning, and the gate exists so this project cannot commit it.

The mirror-image finding matters more in practice: an **unused class-A power** — something the municipality has been able to do by bylaw for thirty years and has not — is the highest-value output the pipeline can produce.

## Commands

| Command | Stage | What it does |
|---------|:-----:|--------------|
| `/capture-testimony <raw>` | 1 | Cleans a raw dictated account into a dated, redacted testimony file; extracts facts to establish *and* attributions to test |
| `/map-powers <area>` | 2a | Builds the jurisdiction map: every lever traced to an instrument and classified A/B/C/D, with a dedicated hunt for unused municipal powers |
| `/research-policy <area>` | 2 | Builds the full six-document evidence base: problem statement, jurisdiction, municipal instruments in force, comparator cities, sourced data annex, City Hall's own record |
| `/draft-paper <area>` | 3 | Synthesizes the research into a Typst policy paper (house template) and compiles the PDF. Refuses to run on an unmapped area or one carrying verification debt |
| `/update-platform` | 4 | Rolls completed papers into the program for the city, sorted by deliverability, with cross-plank coherence, department-capacity and council-arithmetic checks |
| `/compare-council <area>` | — | Builds a comparison matrix: every council faction's position, its actual voting record, and where our proposals sit — rated on the same scale as everyone else's |

## Skills

| Skill | What it governs |
|-------|-----------------|
| `municipal-policy-methodology` | The house rulebook: the stage model, the vires gate, the municipal source hierarchy (city's own record → CBS → city research institute → State Comptroller → Interior Ministry → Knesset RIC), money discipline including the arnona constraint, neighbourhood disaggregation, testimony ethics, Typst house style. Every command defers to it. |
| `municipal-powers-analysis` | How to establish who holds each lever: enumerate before assigning, trace to a cited instrument, map the other actors by name, find the consultee and consent points that make class-D problems tractable, check money separately from power, and test classification against what other municipalities have already done. |
| `comparative-city-research` | How to research other cities: comparators chosen for instrument availability and constraint similarity rather than prestige, at least one Israeli municipality, at least one instructive failure, every case study mapped onto our own A/B/C/D classes so it can tell us whether we could do the same. |
| `city-hall-record-research` | How to establish what the city already tried: council and committee protocols, bylaws drafted and dropped, budget lines that came and went, tenders, pilots, plans, the municipal auditor — ending in the named veto point and the recurring failure mode. |

## Bundled MCP server: Israeli CBS statistics

The plugin ships with an MCP server configuration (`.mcp.json`) for [israel-statistics-mcp](https://github.com/reuvenaor/israel-statistics-mcp) (MIT, by Reuven Naor), which exposes the Israeli Central Bureau of Statistics (הלמ"ס) public API as tools: CPI and sub-index search, catalog navigation, historical index series, housing-market indices, and the official CBS inflation/linkage calculator. No API key is required.

## Design principles

- **No proposal without a named instrument and a named holder of it** — the vires gate.
- **Testimony is evidence of experience, not prevalence** — stories motivate; data justifies. At city scale, say *which neighbourhoods*.
- **No invented numbers** — unverifiable claims are marked and block the pipeline.
- **No promise without a mechanism, and no mechanism without a funding source** — named budget line, named payer, and an honest answer on whether arnona can be touched.
- **Adopted is not implemented, and implemented is not funded** — the distinction that carries most of the record research.
- **Steelmanned trade-offs** — every paper argues the opposition's best case, including the neighbourhood that loses.
