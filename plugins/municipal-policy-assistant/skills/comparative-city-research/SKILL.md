---
name: comparative-city-research
description: Method for researching how other cities have tackled a municipal problem — selecting comparator cities for instrument and constraint rather than prestige, writing per-city case studies covering the municipal instrument used, who paid, the adoption politics on the council, the measured results and the failures, and an argued transferability verdict. Load when building the comparative half of a municipal evidence base or writing policy/<area>/research/04-comparative.md.
---

# Comparative city research

The comparative review answers one question: **has any city actually solved this, and with an
instrument of a kind our municipality could hold?**

That last clause is what separates this from the national version. A national comparative review
can look at any policy in any country, because a national government can in principle legislate
anything. A city cannot. A case study about something a foreign mayor did with powers our
municipality does not have is not evidence, it is decoration — so this stage runs **after**
`02-jurisdiction.md`, and comparator selection is constrained by it.

Follows the evidence standards in the `municipal-policy-methodology` skill. Everything there
applies here; this skill adds the city-comparative method.

## Outputs

```
policy/<area>/research/
├── 04-comparative.md            the synthesis — read this alone and you have the argument
└── comparative/
    ├── <city>.md                one case study per comparator city
    └── ...
```

The synthesis is the deliverable; the case studies are its evidence. Do not write only a
synthesis — an unfootnoted summary of five cities is exactly the artifact this project exists to
avoid.

## Selecting comparators

Pick 4–6 case studies. Choose on **instrument availability and constraint similarity**, not on
how well-regarded the city is.

Aim for a spread across these roles, and say in the synthesis which role each plays:

- **The Israeli comparator — mandatory, and usually the most useful.** Another Israeli
  municipality operating under the same Municipalities Ordinance, the same ministries, the same
  arnona rules and the same planning system. If Tel Aviv-Yafo, Haifa, Beersheba or a small
  council has done this, the legal, fiscal and political feasibility questions are answered by
  demonstration rather than by argument. **At least one Israeli comparator in every review**,
  and if none exists, that absence is itself a finding to state prominently.
- **The canonical success** — the instrument worked and there is measured evidence it did.
- **The constrained near-neighbour** — comparable population, density, poverty rate, fiscal
  dependence on central government, or a comparably fragmented council. For Jerusalem the
  structural analogues are usually large, poor, religiously plural, tourism-heavy or divided
  cities, not the wealthy European capitals that get cited.
- **The instructive failure** — a city that tried this and it did not work, or worked and was
  reversed by the next administration. **At least one is mandatory.** A comparative review with
  no failures in it is advocacy.
- **The over-cited case** — whichever city gets name-checked in the local debate. Research it
  precisely so the paper can correct the record, whichever way it falls.

Record the ones you rejected and why, in a "Comparators considered and rejected" section.
Selection is an analytic choice and must be visible.

## What each case study must contain

Each file in `comparative/` uses this structure. A section with nothing in it says "no evidence
found", never nothing.

1. **Frontmatter** — `jurisdiction` (city, country), `instrument`, `adopted` (year), `status`
   (in force / amended / reversed), `last-verified` (date), `role` (which of the roles above).
2. **The city, briefly** — population, the governance form (strong mayor / council-manager /
   two-tier metropolitan), and its fiscal position. Governance form is not trivia: it determines
   whether their mayor's power maps onto ours at all.
3. **The problem as they framed it** — in their terms, not ours. Framing differences are often
   the finding.
4. **The instrument, mechanically** — the actual by-law, ordinance, tender clause, permit
   condition, charge, or agency. Official name in the original language with translation, year,
   and the operative provisions. *Who* administers it, *how* it is enforced, *how* it is funded.
   This is the section the policy paper will lift from; vagueness here makes the case study
   useless.
5. **Was it the city's own power?** — explicitly. Did the municipality act on its own authority,
   under a national enabling law, with a special grant, or as an agent of a regional body? Map
   it onto our A/B/C/D classes and say which of ours it corresponds to. **A case study without
   this section cannot be used**, because it cannot tell us whether we could do the same.
6. **Who paid** — the funding source and share, in original currency and in ILS with the
   conversion date. Municipal budget, national grant, charge on users, developer contribution,
   philanthropy.
7. **Adoption politics** — who proposed it, who opposed it, what majority passed it, how long it
   took, whether it survived a change of administration, and whether it required a crisis, a
   court ruling or a referendum. For a project whose question is always passability, *how it got
   through the council* is as transferable as the policy.
8. **Evidence of results** — measured outcomes with sources and dates, before and after.
   Distinguish the city's own claims from independent evaluation (national audit office,
   statistics agency, university studies). Where evidence is contested, present both sides.
9. **What went wrong** — implementation failures, cost overruns, exemptions that hollowed it
   out, enforcement that never materialised, subsequent reversals. Every real policy has this
   section.
10. **Transferability** — a judgement, argued. Address at least: the powers question from §5;
    population, density and neighbourhood structure; municipal fiscal capacity and dependence on
    central-government grant; the council's electoral system and fragmentation; the
    administrative capacity of the relevant municipal department; and any factor specific to our
    city — for Jerusalem, at minimum, the demographic and political division of the city, the
    proportion of the population outside the labour market, holy-site and security constraints,
    tourism load, and the status of East Jerusalem residents.
11. **Sources** — full list with links and access dates.

## The synthesis (`04-comparative.md`)

Structure it as an argument, not a city-by-city recital:

1. **The comparative question**, stated in one paragraph, with the class of instrument the
   jurisdiction map says we are shopping for.
2. **Comparator table** — city, instrument, year, our-equivalent class, status, one-line result,
   transferability verdict (high / partial / low, with the criterion stated).
3. **Findings across cases** — 3–6 numbered findings, each supported by more than one case where
   possible. These are the transferable claims the paper will actually make.
4. **What does not transfer, and why** — the honest constraint list, with the powers gap first.
5. **The instructive failures** — its own section, prominently placed.
6. **The Israeli evidence** — its own section. What other Israeli municipalities have done under
   identical constraints carries more weight than everything else combined, and the synthesis
   should say so.
7. **Comparators considered and rejected**, with reasons.

## Rules specific to comparative city work

- **Never cite a city from memory.** Municipal instruments are amended, defunded and quietly
  dropped, and the change is rarely reported outside the local press. Verify current status and
  date it: "as of <date>". Search and fetch; do not recall.
- **Beware the city-ranking source.** Liveability indices, smart-city awards, consultancy
  white papers and mayoral conference material recycle each other. Trace every headline number
  to the city's own data or a national statistics agency, or mark it
  `[UNVERIFIED — verify before publication]`.
- **Report effect sizes, not directions.** "Bus use rose" is not a finding; "bus boardings rose
  8.4% in year one against a 1.1% metropolitan trend" is.
- **Normalise for scale.** Per capita, per household, per kilometre of street, per dunam — a raw
  budget figure from a city of a different size tells you nothing.
- **Distinguish the instrument from the context that made it work.** A fare policy sits on a
  network; a cleanliness policy sits on a labour contract. Say so explicitly rather than letting
  the paper imply the instrument alone produced the outcome.
- **Give the term in the original language.** Municipal instruments have untranslatable names,
  and the original is what finds the primary source.
