---
description: Build the evidence base for a policy area — jurisdiction, municipal instruments, comparative cities, data, and City Hall's record (stage 2 of the pipeline)
argument-hint: <policy-area>
---

Build the research evidence base for the policy area: **$ARGUMENTS**. Follow the `municipal-policy-methodology` skill's evidence rules strictly — this stage exists to ground testimony in verifiable fact, and its credibility is the whole project.

## Inputs

- The cleaned testimony (or testimonies) for this area in `testimonies/`
- The scope notes and research hooks in `policy/$ARGUMENTS/index.md`
- `context/powers/` and `context/city-hall/` — the standing municipal context

## Outputs

Create these six documents in `policy/$ARGUMENTS/research/`. Use web search and web fetch extensively; this stage is research, not recall. Hebrew primary sources are usually the authoritative ones.

1. **`01-problem-statement.md`** — What is broken, synthesizing the testimony (evidence of *experience*) with quantified data (evidence of *prevalence*). Every "how big / how many / how much" claim needs a number with a source. Where the data allows, say **which neighbourhoods** — a city-wide average is usually the wrong unit.

2. **`02-jurisdiction.md`** — Who actually holds each lever. **Run `/map-powers $ARGUMENTS` for this, or load the `municipal-powers-analysis` skill and follow it directly.** Produce this document *first*; documents 4 and 6 both depend on knowing which class of instrument is in play, and the paper cannot be drafted without it.

3. **`03-municipal-instruments.md`** — What the municipality has on the books *today*: the relevant bylaws (חוקי עזר) with publication dates and clause numbers, standing council decisions, current budget lines with amounts, live tenders and contracts and the standards written into them, planning instruments in force, and the department and headcount responsible. Then, with evidence, where it fails in practice — enforcement resourcing, execution against the approved budget, contract performance actually measured. Cross-reference `02-jurisdiction.md` rather than repeating it: that document says who *could* act, this one says what is *in force*.

4. **`04-comparative.md`** + **`comparative/<city>.md`** — How other cities have tackled this. **Load the `comparative-city-research` skill and follow its method**: comparators chosen for instrument availability and constraint similarity rather than prestige, one case-study file per city, **at least one Israeli municipality**, at least one instructive failure, and every case study mapped onto our A/B/C/D classes so we know whether we could do the same thing.

5. **`05-data.md`** — The statistical annex: every dataset used, with source, year, exact figure, geographic unit, and a link. Preferred sources in order: the municipality's own published budget and reports → CBS (הלמ"ס) local authorities data and statistical areas → Jerusalem Institute for Policy Research Statistical Yearbook → State Comptroller → Ministry of the Interior → Knesset RIC → OECD → peer-reviewed research → quality journalism (flagged as such). The `israel-statistics` MCP server gives direct access to CBS indices. **Disaggregate by neighbourhood wherever the source permits, and record explicitly where a source does not cover part of the city.**

6. **`06-city-hall-record.md`** (+ `record/` case files where warranted) — What the municipality has already tried: council and committee decisions, bylaws drafted and dropped, budget lines that came and went, tenders, pilots, plans, and the municipal auditor's and State Comptroller's findings. **Load the `city-hall-record-research` skill and follow its method.** Its most important outputs are the named veto point and the recurring failure mode.

Documents 4 and 6 are two halves of the same question — *what has worked elsewhere* and *what has already failed here* — and the policy paper cannot be written honestly without both. Document 2 governs both: it decides which instruments are even worth researching.

## Rules

- A number you cannot source gets written as `[UNVERIFIED — verify before publication]` and listed in a "Verification debt" section at the top of `05-data.md`. The area cannot advance to stage 3 with verification debt outstanding.
- Prefer primary sources in Hebrew where they are authoritative; quote the Hebrew name alongside the English. Council protocols and bylaws exist in Hebrew only.
- Steelman the counter-evidence: if the data complicates the testimony's narrative, record that prominently rather than burying it. If the problem turns out to be concentrated in fewer places or fewer people than the testimony implies, say so and re-scope the argument around what is left.
- Finish by updating the stage table in `policy/$ARGUMENTS/index.md` and reporting: the strongest three facts found, the weakest link in the evidence base, and — separately — whether the jurisdiction map leaves a proposal worth writing at all. If it does not, say so; abandoning an area on the evidence is a legitimate and valuable outcome.
