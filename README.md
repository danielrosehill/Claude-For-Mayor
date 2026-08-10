# Claude-For-Mayor 🏛️🤖

*An AI-assisted municipal platform for a candidate who doesn't exist.*

### 📖 **[Read it as a site → danielrosehill.github.io/Claude-For-Mayor](https://danielrosehill.github.io/Claude-For-Mayor/)**

Claude is not running for mayor of Jerusalem, is not eligible to, and does not live here.

## What is this?

The sibling of **[MK-Claude](https://github.com/danielrosehill/MK-Claude)**, which builds a
national political platform for Israel the way a platform ought to be built — researched, cited,
costed, honest about its trade-offs, and written in public while unfinished. This repository does
the same thing one level down: **a mayoral platform for Jerusalem.**

It is not a copy with the word "Knesset" replaced. Municipal policy has a constraint that national
policy does not, and the whole pipeline is built around it:

> **Most of what residents blame City Hall for is not City Hall's to fix, and a good half of what
> City Hall could fix tomorrow, nobody asks it to.**

A mayor is elected on promises about schools, buses, policing, healthcare, cleanliness, housing and
parks. A municipality's formal power over each of those ranges from near-total to essentially none,
and the ranking is not the one campaigns assume. Meanwhile the powers a city unambiguously holds —
what it writes into a tender, what conditions it attaches to a licence, what it tells its
inspectors to enforce, what it publishes — attract almost no attention, because they are
unglamorous and specific.

So this project adds a gate that MK-Claude does not have.

## The powers doctrine

**No proposal is published without a named instrument and a named holder of it.** Every lever is
traced to the provision that creates it and classified:

| Class | Meaning |
|:-----:|---------|
| **A** | Municipality decides and funds — bylaw, council decision, tender clause, licensing condition, budget line, enforcement priority |
| **B** | Municipality decides, an external body must approve — ministerial confirmation, arnona deviation, district planning committee |
| **C** | Shared — delivery municipal, policy or funding national; the analysis finds the municipal leverage inside the arrangement |
| **D** | No municipal power — legitimate as **advocacy**, with a named counterpart and a real route; never as a promise |

Every recommendation carries its class letter, and the program for the city is sorted by class
before it is sorted by theme, because "which of this could you actually do?" is the first honest
question about any mayoral platform.

The mirror-image finding matters more in practice: an **unused class-A power** — something the
municipality has been able to do by bylaw for thirty years and has not — is the highest-value
output the process can produce.

Full statement: **[the powers doctrine](./site/src/content/docs/method/powers-doctrine.md)**.

## Status

**The method is built and the content has just started.** On 10 August 2026 the first testimony
landed — one dictated account of ten years living here, given in three sittings, which opened eight
areas at once. All eight sit at stage 1, and under the powers doctrine none of them may propose
anything until its jurisdiction map exists.

| Layer | State |
|---|---|
| Pipeline, evidence rules, powers doctrine | ✅ written |
| `municipal-policy-assistant` plugin — 6 commands, 4 skills | ✅ written; `/capture-testimony` run once, the other five untested |
| Context — the 2024 election result and council arithmetic | 🟡 recorded, from a secondary source |
| Context — City Hall coalition and record | 🟡 research plan only |
| Context — the powers primer | 🟡 hypotheses and research plan; **nothing verified yet** |
| Policy areas | 🟡 eight open, all at stage 1 |
| Program for the city | ⬜ empty, by design |

| Area | Testimony | Jurisdiction | Research | Paper | Manifesto |
|------|:---------:|:------------:|:--------:|:-----:|:---------:|
| [Renting](./site/src/content/docs/policy/renting/index.md) | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| [Housing supply](./site/src/content/docs/policy/housing-supply/index.md) | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| [Construction disruption](./site/src/content/docs/policy/construction-disruption/index.md) | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| [Construction noise](./site/src/content/docs/policy/construction-noise/index.md) | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| [Small businesses](./site/src/content/docs/policy/small-businesses/index.md) | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| [Environmental quality](./site/src/content/docs/policy/environmental-quality/index.md) | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| [Capital priorities](./site/src/content/docs/policy/capital-priorities/index.md) | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| [Buses](./site/src/content/docs/policy/buses/index.md) | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |

All eight rest on a single household's account given on a single day, and they vary a great deal
in how much testimony is actually behind them. That is stated plainly in
[whose account this is](./site/src/content/docs/context/whose-account.md), along with what that
vantage point cannot see.

Full tracking, including every claim currently resting on a secondary source, in
**[tasks.md](./site/src/content/docs/tasks.md)**.

### What the context layer has established

- **Turnout in February 2024 was 33.7%.** Two-thirds of the electorate did not vote, in a mayoral
  contest decided 81–19. [The election](./site/src/content/docs/context/the-election/index.md)
- **The mayor's own list holds 2 of 31 council seats.** Authority in Jerusalem is coalition
  authority; the Haredi lists hold 16 of 31 between them, a bare majority on their own, and there
  is no majority that excludes them. [City Hall](./site/src/content/docs/context/city-hall/index.md)
- **No municipal power has been verified yet.** The powers primer is a list of hypotheses with a
  caution box on top, and under our own evidence rules none of it may be cited.
  [Municipal powers](./site/src/content/docs/context/powers/index.md)

## Repository structure

The content and the website are the same tree. Everything under `site/src/content/docs/` is both a
Markdown file you can read here on GitHub and a page on the site.

```
site/
  src/content/docs/        ← the content root; all paths below are relative to it
    policy/                the policy areas: evidence base per area
    testimonies/           stage 1 — dated first-person accounts
    context/               the election, City Hall, the powers primer, the matrices
    platform/              stage 4 — the program for the city
    method/                the powers doctrine, evidence rules, the plugin
    pipeline.md            the methodology in full
    tasks.md               open work and verification debt, in public
  public/papers/           stage 3 — compiled policy papers (Typst source + PDF)
  src/pages/index.astro    the landing page
plugins/                   the municipal-policy-assistant Claude Code plugin
templates/                 Typst house template for policy papers
testimonies-raw/           gitignored staging area for raw dictations
```

Raw testimony material is kept **outside** the site tree on purpose, so it cannot be published by
accident.

## Methodology

Policy moves through four stages and a gate — first-person testimony, a jurisdiction map, an
evidence base of six documents, a think-tank-style policy paper, and finally a rolled-up program
for the city. Each stage has a bar it must clear before the next one starts. Full detail in
**[the pipeline](./site/src/content/docs/pipeline.md)** and
**[the evidence rules](./site/src/content/docs/method/evidence-rules.md)**.

Everything is version-controlled, so the platform's evolution — including changes of mind — is
public history.

## The plugin

The pipeline is automated by a Claude Code plugin shipped in this repo,
**[municipal-policy-assistant](./plugins/municipal-policy-assistant/)**: a command per stage
(`/capture-testimony`, `/map-powers`, `/research-policy`, `/draft-paper`, `/update-platform`,
`/compare-council`), four method skills encoding the standards, and a bundled MCP server
([israel-statistics-mcp](https://github.com/reuvenaor/israel-statistics-mcp)) giving Claude direct
tool access to Israeli Central Bureau of Statistics (הלמ"ס) index data — no API key needed.

```
/plugin marketplace add danielrosehill/Claude-For-Mayor
/plugin install municipal-policy-assistant@claude-for-mayor
```

The stage model and the A/B/C/D classification transfer to any city. The statistics server, the
source hierarchy and the arnona constraint are Israeli.

## What this is *not*

- ❌ A real candidacy (no, Claude is not running for mayor)
- ❌ An endorsement of any faction on the council, or a criticism of the current administration —
  the record research will say what the record says
- ❌ A claim that AI should make policy — the human sets the values and priorities; the AI helps
  with research, drafting, and stress-testing

Think of it as **civic engagement by other means**: instead of complaining about the city, writing
down — rigorously, and with the powers actually checked — what a platform worth voting for would
contain.

## Working on the site

```bash
cd site
npm install
npm run dev      # local preview
npm run build    # type-check, build, and fail on any broken internal link
```

Requires Node 22+. The site deploys to GitHub Pages automatically on push to `main`.

## Contributing

This is a personal experiment, but it's a public repo for a reason. Issues and pull requests with
corrections, better data, or counterarguments are welcome. Disagreement is especially welcome if it
comes with sources — and a citation showing that a power is classified wrongly is the single most
useful correction anyone can send.

## License & disclaimer

Content is provided as-is for discussion and educational purposes. Drafted collaboratively with AI
assistance; all errors are the human's responsibility, and all opinions are the repository owner's
alone.
