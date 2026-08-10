# Claude-For-Mayor — working notes

## Relationship to MK-Claude

This repository is a deliberate fork of the *method* of
[MK-Claude](https://github.com/danielrosehill/MK-Claude), not of its content. Where the two
diverge, the divergence is intentional and should not be "corrected" back:

| MK-Claude | Here | Why |
|---|---|---|
| 5 research documents | **6** | `02-jurisdiction.md` is new |
| `/compare-parties` | `/compare-council` | Council factions and their voting record, not Knesset parties |
| `policy-development-assistant` | `municipal-policy-assistant` | Separate plugin, separate marketplace |
| Paper numbers `PP-NNN` | `MP-NNN` | Municipal paper |
| `program-for-government.md` | `program-for-the-city.md` | |
| 4 stages | 4 stages **+ a gate** | The powers doctrine |

Improvements to the shared parts — the evidence rules, the testimony handling, the Typst
template — are worth porting in both directions. The powers material is this repo's alone.

## The content root

**All pipeline content lives under `site/src/content/docs/`.** That directory is the content root,
and every path in the `municipal-policy-assistant` plugin's commands and skills is relative to it,
not to the repository root:

| Plugin path | Actual location |
|-------------|-----------------|
| `testimonies/` | `site/src/content/docs/testimonies/` |
| `observations/` | `site/src/content/docs/observations/` |
| `policy/<area>/` | `site/src/content/docs/policy/<area>/` |
| `context/` | `site/src/content/docs/context/` |
| `platform/` | `site/src/content/docs/platform/` |
| `policy/<area>/paper/` | `site/public/papers/` (flat: `<area>.typ`, `<area>.pdf`) |
| `testimonies/raw/` | `testimonies-raw/` at the repository root — gitignored |

Raw testimony material is deliberately kept **outside** the content root: anything inside it is
published to the web.

Papers are flat in `site/public/papers/` so the compiled PDF is served as a static download at
`/papers/<area>.pdf`. The Typst import path from there is
`#import "../../../templates/policy-paper.typ": ...`.

## The gate is load-bearing

`/draft-paper` refuses to run on a policy area without `02-jurisdiction.md`. That is not a bug to
work around when a paper seems obvious. The doctrine is in
`site/src/content/docs/method/powers-doctrine.md` and the working method is in the
`municipal-powers-analysis` skill; read both before touching anything in the paper stage.

Two rules from it that are easy to lose under time pressure:

- **A power without a citation is not a power.** Uncited attributions are `[UNVERIFIED]` and block
  advancement like any other unsourced claim.
- **If another Israeli municipality has already done it, it is class A or B by demonstration** —
  whatever the legal analysis suggested. Run that test early; it settles feasibility questions that
  would otherwise take a day of statutory reading.

## Frontmatter is validated

Every Markdown file under the content root is a Starlight page and its frontmatter is schema-checked
at build time:

- `title` is **required**, and Starlight renders it as the page's `<h1>`. Do not also write a
  `# Heading` at the top of the body — that produces two H1s.
- `description` is optional but wanted on index pages; it becomes the meta description.
- The pipeline's own fields (`policy-area`, `document`, `status`, `last-verified`, `date`, `source`,
  `jurisdiction`, `instrument`, `adopted`, `role`, `election`, `sources-cutoff`) are declared in
  `site/src/content.config.ts`. **Adding a new frontmatter field means adding it there first**, or
  the build fails.
- `sidebar: { label, order }` controls navigation. Research documents use `1 ·`…`6 ·` labels.

## Links

Write links as **file-relative Markdown paths** — `../../testimonies/2026-08-10-example.md`,
`./research/05-data.md`. They stay correct when the file is browsed on GitHub, and
`site/plugins/resolve-doc-links.mjs` rewrites them to published URLs at build time. A link that
resolves to nothing becomes a build warning; `npm run build` then fails on it via
`scripts/check-links.mjs`.

Links pointing outside the content root (to `plugins/`, `templates/`) are rewritten to GitHub blob
URLs automatically. Don't hand-write absolute site paths — they break if the base path changes.

## CSS prefix

The landing page's classes use a `cfm-` prefix (`cfm-lede`, `cfm-plank`, `cfm-finding`, …), defined
in `site/src/styles/custom.css`. MK-Claude uses `mk-`; the rename was mechanical when this repo was
forked, so a stylesheet copied across from there needs the same treatment.

## Deployment

`site/site.config.mjs` holds `SITE` and `BASE`; everything else derives from them. Moving to a
custom domain means editing those two values and nothing else.

Node 22+ is required (Astro 7). Locally: `export PATH="$HOME/.nvm/versions/node/v22.21.1/bin:$PATH"`.
Push to `main` deploys via `.github/workflows/deploy.yml`.

The site has **no cover or Open Graph image** yet, unlike MK-Claude — `index.astro` deliberately
does not import one, so adding `cover.jpg`/`og.jpg` means adding the `<Image>` block and the
`og:image` head tag back.

## Keep in step

Four places carry the status table and drift apart easily:

1. `site/src/content/docs/tasks.md` — the source of truth
2. `site/src/content/docs/policy/index.md` — the area table
3. `site/src/pages/index.astro` — the `planks` array on the landing page
4. `README.md` — the repository-level table

When an area advances a stage, update all four. `planks` is populated as of 2026-08-10, so the
empty-state branch in `index.astro` no longer renders; it is kept because areas could in principle
be withdrawn.

The sidebar in `site/astro.config.mjs` is written out by hand rather than autogenerated, so a new
policy area also needs an entry there — an "Overview" link plus an autogenerated "Evidence base"
subgroup over its `research/` directory. MK-Claude's `astro.config.mjs` has the shape to copy.
Testimonies and observations are listed in it by hand too, one line each.

## Testimony is not the only door

Two document classes were added on 2026-08-10, both outside the four stages, both incapable of
advancing anything:

- **`observations/`** — a problem with no first-person account behind it. Its entry condition is a
  mandatory `origin` frontmatter field: a *sentence* saying how the problem came to be on file,
  not a category. The point of the class is to stop inference being laundered into testimony, so
  the rule that makes it safe is the one to defend — **an observation cannot open a policy area**,
  and it is never rewritten into a testimony when better evidence arrives. Written by
  `/capture-observation`; rules in `observations/index.md`.
- **`platform/spine.md`** — cross-area synthesis of what the testimony says, written *before* the
  jurisdiction gate. Legitimate at stage 1 because it analyses what was said rather than claiming
  what can be done: no proposals, no class letters, no citations. It is not a draft of
  `program-for-the-city.md`, which stays empty until an area passes stage 3. Do not let the two
  merge — the distinction between "this is what the evidence is about" and "this is what a mayor
  would do about it" is the whole reason the gate holds.

A new observation touches three files: the observation itself, the index table in
`observations/index.md`, and the sidebar. It must **not** touch `planks`, `policy/index.md` or the
status tables — those are for areas, and areas open on testimony.
