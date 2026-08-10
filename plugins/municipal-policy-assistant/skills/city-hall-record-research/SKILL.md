---
name: city-hall-record-research
description: Method for researching what the municipality has already tried on a problem — council and committee decisions, bylaws proposed and dropped, budget lines that appeared and vanished, pilots, master plans, tenders, municipal auditor and State Comptroller findings — ending in the named veto point and the recurring failure mode. Load when writing policy/<area>/research/06-city-hall-record.md or when asked "has the city tried this before".
---

# City Hall record research

The comparative review asks *has any city solved this?* This one asks the harder question:
**has our city already tried, and what happened?**

At municipal level the answer is almost always yes, and almost always more than once. A council
motion that passed and was never funded. A bylaw drafted and left with the legal adviser. A
pilot in three neighbourhoods that ended when the ministry grant did. A master plan whose
relevant chapter was never implemented. A department reorganised into a different department.
A proposal written in ignorance of that history is not a proposal; it is a re-run, and in a city
the people who watched it fail the first time are still in the building.

Follows the evidence standards in the `municipal-policy-methodology` skill. Everything there
applies here.

## Outputs

```
policy/<area>/research/
├── 06-city-hall-record.md      the synthesis — attempts, outcomes, why they failed
└── record/
    ├── <attempt-slug>.md       one file per significant attempt, where the detail warrants it
    └── ...
```

Cross-reference, do not duplicate. `02-jurisdiction.md` covers **who holds the power**;
`03-municipal-instruments.md` covers **what is on the books today**; this covers **everything
that was attempted**, including what was never adopted and what was later dropped. Council
factions' *campaign* positions belong in `context/city-hall/` and the matrix produced by
`/compare-council`; this document covers what the municipality actually *did*, and links to the
matrix rather than restating it.

## What to look for

Work through each channel; state explicitly in the synthesis if a channel turned up nothing.

**The council and its committees**
- **Council protocols** (פרוטוקולי מועצת העיר) — municipalities publish these. They are the
  single richest and least-read source available, and they contain the objections in the words
  of the officials who raised them. Record the date, the item number, the mover and faction, the
  vote, and who spoke against.
- **Committee decisions** — finance, planning and building, education, tenders, names. The
  planning and building committee (הוועדה המקומית לתכנון ובנייה) is where a large share of real
  municipal decisions are actually made.
- **Motions passed and not implemented.** A council decision with no budget line and no
  responsible official is the municipal equivalent of a shelved report, and it is extremely
  common. Check whether each decision was funded and whether it was executed.

**Legislative and regulatory**
- **Bylaws** (חוקי עזר) proposed, adopted, amended, or drafted and abandoned. Note the date of
  publication in the official gazette and whether the Interior Minister's confirmation was
  sought or granted.
- **Enforcement policy** — a bylaw with no inspectors is not in force in any sense that matters.
  Look for inspector headcount, ticket volumes, and whether enforcement was suspended.

**Fiscal**
- **The approved budget, year on year.** A line that appears, grows, shrinks and disappears is
  a complete narrative. Compare the approved budget to the executed budget where both exist.
- **Tenders and contracts** (מכרזים) — issued, cancelled, re-issued, awarded to a single bidder.
  A cancelled tender usually means something specific.
- **Ministry grants and earmarked funds** received for this purpose, and what happened when they
  ended.

**Plans**
- **Master plans and outline plans** covering the area or subject, their status in the planning
  system, and which chapters were implemented.
- **Strategic plans and multi-year programmes** the municipality has published. These are
  written to be published; the useful question is what fraction of the last one was delivered.

**Oversight**
- **The municipal auditor** (מבקר העירייה) — statutory, reports annually on the municipality's
  own conduct, and is routinely the most direct evidence that a municipal policy does not work.
- **State Comptroller** (מבקר המדינה) reports, including the local-government audit
  (הביקורת על השלטון המקומי), which audits municipalities directly. Cite report year and chapter.
- **Ministry of the Interior** supervision — the district commissioner's decisions, financial
  oversight, and anything relating to the balancing grant.
- **Knesset Research and Information Center** briefs, which frequently contain the
  cross-municipal comparison and sometimes the only published city-level figure.

**Political**
- Which factions have owned this issue and which have blocked it, across council terms —
  including the **coalition agreements** on the council, which are where a commitment is
  typically traded away, and which are sometimes published.
- Whether the blocking interest is a faction, a department, a union, a contractor, a
  neighbourhood, the Interior Ministry, or the Treasury. **Naming the actual veto point is the
  most useful output of this whole document.**

**Local press and civil society**
- Local Jerusalem press and neighbourhood outlets are often the only record that an attempt
  happened at all. Use them to *find* the attempt, then get the protocol or the decision. A
  press report is a lead, not a citation.
- Community administrations (מנהלים קהילתיים), residents' committees, and city-focused NGOs
  publish material and hold institutional memory the municipality does not.

## Structure of `06-city-hall-record.md`

1. **Summary of the record** — one paragraph: has this been tried, how many times, and what is
   the pattern?
2. **Timeline table** — year, instrument (council decision / bylaw / budget line / tender /
   pilot / plan), mover and faction, outcome (adopted / rejected / adopted-unfunded / executed /
   quietly dropped / reversed), source link. This table is the document's spine.
3. **Attempt-by-attempt analysis** — for each significant attempt: what was proposed, the
   mechanism, who supported and opposed it, what killed it or what it achieved, and what the
   evidence says about the outcome.
4. **The pattern of failure** — the recurring failure mode, named. Typical municipal candidates:
   adopted but never funded; funded but never staffed; enforcement never resourced; a ministry
   grant that expired; a departmental reorganisation that orphaned it; contractor performance
   unmanaged because the contract had no measurable standard; a neighbourhood objection that
   killed it politically; jurisdictional stalemate with a ministry; a change of coalition on the
   council.
5. **Veto points and enablers** — who must be neutralised or recruited for anything here to pass
   or persist, with evidence for each. Distinguish the vote (council arithmetic) from the
   delivery (department, contractor, ministry).
6. **What is already live** — anything currently in train: adopted decisions awaiting
   implementation, tenders out, plans in deposit, budget lines allocated in the current year.
   Proposing something already funded is the most avoidable error available to us, and at
   municipal level it is easy to make because so little is announced.
7. **Implications for our proposal** — the design constraints this history imposes, each
   traceable to a specific failure above. If the pattern is "adopted and never funded", the
   proposal must carry a funding mechanism and a reporting requirement; say so here.

## Rules specific to municipal record work

- **Hebrew sources are primary.** Protocols, decisions, bylaws, budgets and auditor reports are
  authoritative in Hebrew. Quote the Hebrew name and give the English translation.
- **Adopted is not implemented, and implemented is not funded.** State which, with the date
  checked. This distinction carries most of the document's value.
- **Get the protocol.** Where a decision matters, read the minutes of the meeting rather than the
  decision text. The reason it was watered down is in the debate, not the resolution.
- **Distinguish record from platform.** What a faction said in a campaign and what it voted for
  in council are separate claims and go in separate columns.
- **Do not paraphrase an objection into a strawman.** If the finance department opposed a
  measure, find its stated reason and quote it. That objection is the one our paper has to
  answer, and unlike national policy it is usually recorded verbatim.
- **A dropped proposal is evidence, not an embarrassment.** Its content is often good and
  already costed; the finding is the dropping, and the useful question is who dropped it and
  why.
- **Absence of a record is a finding too** — but only after you have looked in the protocols. Do
  not conclude "never tried" from a web search.
- Anything unsourced is marked `[UNVERIFIED — verify before publication]` and blocks stage
  advancement, exactly as elsewhere.
