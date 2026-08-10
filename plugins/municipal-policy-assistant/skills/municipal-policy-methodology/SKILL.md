---
name: municipal-policy-methodology
description: House methodology for evidence-based municipal policy development — the stage model, evidence standards, the municipal source hierarchy, the vires gate, arnona and budget discipline, testimony handling, and the think-tank writing style. Load whenever cleaning testimony, researching a city policy area, drafting a policy paper, or updating the program for the city.
---

# Municipal policy development methodology

This project turns lived experience of a city into a credible program for governing it. Its
only asset is credibility; these rules protect it.

The national version of this problem lets you propose almost anything and argue about whether
it is a good idea. A municipal platform cannot. **Most of what residents blame City Hall for is
not City Hall's to fix, and a good half of what City Hall could fix tomorrow nobody asks it
to.** Establishing which is which is not a preliminary to the policy work — it *is* the policy
work, and it is what the extra stage in this pipeline exists for.

## The pipeline

Four stages, each with a gate (full detail in the repo's `pipeline.md`):

1. **Testimony** (`testimonies/`) — dated, cleaned, redacted first-person accounts of living
   in the city. Raw material never committed.
2. **Research** (`policy/<area>/research/`) — six documents: problem statement, jurisdiction
   map, municipal instruments, comparative city review, data annex, City Hall's own record.
   Three of the six have their own method skills: `municipal-powers-analysis`,
   `comparative-city-research` and `city-hall-record-research`.
3. **Paper** (`site/public/papers/`) — Typst + PDF using `templates/policy-paper.typ`.
4. **Platform** (`platform/program-for-the-city.md`) — the distilled meta-proposal.

Each policy area has a stage tracker at `policy/<area>/index.md`. Keep it current.

Paths above are relative to the repository's **content root**. This repository publishes its
content as a site and puts the root at `site/src/content/docs/` — see `CLAUDE.md` for the
mapping table, and resolve every path in this skill against it.

## The vires gate

The rule that distinguishes this project from a wish list, and the one to apply hardest:

> **No proposal enters a policy paper without a named instrument and a named holder of it.**

For every recommendation, state which of these it is:

| Class | Meaning | What the paper must show |
|-------|---------|--------------------------|
| **A — Municipal, own motion** | The municipality already has the power and the money | The instrument (bylaw section, tender clause, licensing condition, budget line, council decision), the department that administers it, and why it has not been used |
| **B — Municipal, needs approval** | Council can act but a ministry must sign off | The approving body, the statutory basis for its consent, and evidence about how it has decided comparable requests |
| **C — Joint** | Delivery is municipal, decision or funding is national | The split, precisely — who sets policy, who employs the staff, who pays what share — and the lever the municipality holds inside the arrangement |
| **D — National** | The municipality has no formal power at all | Say so plainly, then either drop it or reclassify it as an **advocacy** proposal with a named counterpart, an ask, and a realistic route |

A class-D proposal presented as something a mayor can deliver is the single most common
dishonesty in municipal campaigning. This project does not get to commit it. Advocacy
proposals are legitimate and stay in — labelled as advocacy, with the mayor's actual leverage
(convening power, statutory consultee status, planning consent, land, publicity) named rather
than assumed.

Classification is done in `02-jurisdiction.md` by the `municipal-powers-analysis` skill, and
**every recommendation in the paper carries its class letter.**

## Evidence standards

- **Never invent a number.** If you cannot find a source, write
  `[UNVERIFIED — verify before publication]`. Unverified claims block stage advancement.
- **Municipal source hierarchy** (prefer higher):
  1. **The municipality's own published record** — the approved budget (תקציב), council and
     committee protocols (פרוטוקולי מועצת העיר וועדותיה), bylaws (חוקי עזר), tenders
     (מכרזים), city plans lodged in the planning system, and the municipal auditor's reports
     (מבקר העירייה). These are primary and they are what a mayor would actually be handed.
  2. **CBS** (הלשכה המרכזית לסטטיסטיקה) — the local authorities file
     (הרשויות המקומיות בישראל), the social-economic ranking (מדד חברתי-כלכלי) and the
     municipality's own CBS profile. Neighbourhood-level statistical areas (אזורים סטטיסטיים)
     are the resolution most municipal arguments actually need.
  3. **Jerusalem Institute for Policy Research** (מכון ירושלים למחקרי מדיניות) — the
     Statistical Yearbook of Jerusalem, published annually since 1983 ahead of Jerusalem Day,
     and *Jerusalem: Facts and Trends*. It compiles CBS and municipal data at city and
     neighbourhood level. Treat it as an excellent secondary source and follow its own
     footnotes to the primary where a claim is load-bearing.
  4. **State Comptroller** (מבקר המדינה) — including the dedicated local-government audit
     (הביקורת על השלטון המקומי), which audits municipalities directly.
  5. **Ministry of the Interior** (משרד הפנים) — municipal financial reporting, the balancing
     grant (מענק איזון), and the district commissioner's (הממונה על המחוז) decisions.
  6. **Knesset Research and Information Center** (מרכז המחקר והמידע של הכנסת) — frequently has
     already done the cross-municipal comparison you are about to attempt.
  7. Bank of Israel, OECD and international official statistics, peer-reviewed research.
  8. Quality journalism — last resort, always flagged. Local Jerusalem press (*Kol Ha'Ir*,
     *Jerusalem Post*, *Ynet* Jerusalem desk, *Ha'aretz*) is often the only record of a council
     row, but a council row is reported, not proven; find the protocol.

- **Legislation and subordinate legislation are cited precisely**: official name (Hebrew and
  English), year, amendment number, specific sections. Municipal work leans heavily on
  *subordinate* instruments — bylaws, ministerial orders, licensing conditions, tender terms —
  and these get the same treatment: name, publishing authority, date, clause. Verify clause
  numbers against the actual text; do not cite provisions from memory.
- **Testimony is evidence of experience, not prevalence.** One resident's street proves
  something *can* happen; only data proves it is *common*. At municipal scale this trap is
  sharper than nationally, because a single neighbourhood's problem can be genuinely
  unrepresentative of the city while being completely real. Papers keep the distinction
  explicit and, where the data allows, say *which neighbourhoods*.
- **Steelman opposing evidence.** If data complicates the narrative, it goes in the main text,
  not a footnote. Every proposal names its losers and answers the strongest objection.
- **Costs are order-of-magnitude honest, and stated against the actual budget.** See below.

## Money discipline

A municipal proposal that does not say where the money comes from is not a proposal. Every
costed recommendation states its funding class:

- **Within an existing budget line** — name the line and the year's allocation, and say what
  gets less.
- **Reallocation** — name both lines. "Efficiency savings" is not a source.
- **Arnona** (ארנונה, municipal property tax) — the default assumption is that the
  municipality *cannot* simply raise it. Rates are updated annually by a nationally set
  formula, and a deviation (חריגה) requires the joint approval of the Ministers of the
  Interior and Finance. Any proposal relying on arnona income must establish the current rule
  and cite it, and must address the approval risk. Changes to classifications, discounts and
  exemptions (הנחות ופטורים) are a separate and often more available lever than the headline
  rate — check both.
- **A government ministry** — this makes the proposal class C or D. Say so, and name the
  budget and the decision-maker.
- **A municipal company or external body** — Jerusalem delivers a great deal through municipal
  and quasi-municipal corporations and through philanthropy. Name the entity, its ownership,
  and whether the mayor actually controls it.

State the estimate's basis and confidence. "Fiscally neutral" requires showing the offset.

## Neighbourhood discipline

City-wide averages hide the thing municipal policy is for. Where the data supports it, report
by neighbourhood or statistical area rather than city-wide, and state explicitly:

- whether the problem is concentrated or general;
- whether the proposal's benefit is concentrated or general, and whether those are the same
  places;
- what it does to the gap between the best-served and worst-served parts of the city.

In Jerusalem specifically, an analysis that does not disaggregate East Jerusalem, the Haredi
neighbourhoods, and the rest of the city will be wrong about almost any service question, and
will be *seen* to be wrong. Where a data source does not cover a part of the city, say so —
missing data about a neighbourhood is itself a finding, and often the most important one.

## Testimony handling

- Cleaning removes disfluencies and transcription artifacts; it **never adds, softens,
  strengthens, or renumbers** a claim. Ambiguity in the raw stays ambiguous or gets resolved by
  asking the author.
- Redact private individuals' names, exact addresses, third-party identifying details.
  Institutions and public figures stay named. Municipal testimony is unusually easy to
  de-anonymise — a street, a building, a school and a date will identify a household. Generalise
  to the neighbourhood unless the specific location is the point, and if it is, get the author's
  explicit agreement.
- Frontmatter schema: `title`, `date` (YYYY-MM-DD), `policy-area` (kebab-case, matches
  `policy/<area>/`), `status` (`cleaned` | `synthesized-into-research`), `source` (one line,
  where the raw is retained privately).

## Writing style (papers and platform)

- Think-tank register: measured, concrete, mechanism-first. Anger belongs in the testimony; the
  paper's force comes from evidence.
- No promise without a mechanism: every recommendation says what instrument changes, who
  administers it, what it costs, who pays, and **which class (A/B/C/D) it is**.
- Distinguish what the council can resolve at its next meeting from what needs a ministry, and
  give the realistic elapsed time for each.
- Hebrew terms on first use: transliteration + Hebrew + gloss, e.g.
  "Arnona (ארנונה, municipal property tax)". Where a term has a standard Arabic form used in
  the city, give it too on first use in any East Jerusalem context.
- Footnote every factual claim. A reader should be able to check anything without asking.

## Typst conventions

- Import from `templates/policy-paper.typ`: `policy-paper` (show rule), `#recommendation[...]`,
  `#tradeoff(objection, response)`.
- Paper numbers are sequential `MP-NNN` across the whole project (*municipal paper*).
- Must compile warning-free with `typst compile`; visually inspect page 1 via PNG render before
  committing. Commit both `.typ` and `.pdf`.
