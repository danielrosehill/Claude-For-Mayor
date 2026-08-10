---
title: Policy comparison matrices
description: One matrix per policy area, comparing every council faction's position — and its actual voting record — against ours, on the same scale.
sidebar:
  label: Comparison matrices
  order: 4
---

One matrix per policy area, comparing what each faction on the council proposes — and what it did
when it had the chance — against our proposal.

Built by `/compare-council <area>`. None exist yet; the first arrives with the first policy area.

## File format

`<policy-area>.md`, matching the `policy/<area>/` slug. Frontmatter:

```yaml
---
policy-area: example-area
election: 2024
last-verified: 2026-08-10
sources-cutoff: 2026-08-10   # material published after this date is not reflected
---
```

## Required sections

1. **Scope** — the specific questions the matrix compares on (the rows). Chosen *before* filling
   in the columns, so the rows are not gerrymandered to favour a predetermined winner.

2. **Rating scale** — if cells are rated, the scale defined explicitly. Suggested default:

   | Symbol | Meaning |
   |--------|---------|
   | ●● | Concrete commitment with a named mechanism (bylaw, budget line, tender clause, council decision) |
   | ● | Commitment stated, mechanism unspecified |
   | ○ | Mentioned as an aspiration only |
   | — | No stated position |
   | ✗ | Actively opposes |

   The distinction that does the work is **●● vs ●**: "we will clean up the neighbourhood" is `●`;
   "we will amend bylaw X to require Y, funded from budget line Z" is `●●`. Most municipal
   campaign material is `●` or `○`, and the matrix should show that plainly rather than inflating
   it.

3. **The matrix** — rows are the scope questions, columns are the council factions plus a final
   column for this project. Cells carry the rating and a short quoted or closely-paraphrased
   position, with a footnote to the source document.

4. **The voting record** — a second matrix, and at municipal level **the more important one**.
   Council votes are recorded in the protocols, they are recent, and they concern the actual
   instruments in play. What a faction voted for is better evidence of its position than anything
   it published. Where the vote and the platform conflict, show both and say which is which; note
   where a vote was bound by coalition discipline.

5. **The deliverability row** — for each column, how many of that faction's commitments in this
   area are class A/B/C/D against our [jurisdiction map](../../method/powers-doctrine.md). A
   faction promising things no municipality can do is a factual finding about that platform, and
   it is checkable. It applies to our column too, and this row is the one most likely to be
   uncomfortable for us.

6. **Gap analysis** — the payoff section. Which of our proposals are:
   - **Already adopted or already funded** → drop, or reframe as implementation and enforcement
   - **Already promised by others** → not distinctive; either adopt their framing and credit it,
     or explain what ours adds
   - **Genuinely unaddressed** → the core of the paper
   - **Actively opposed by a bloc** → costed politically against
     [the council arithmetic](../city-hall/index.md); the paper needs to answer their objection
     specifically

   Also the inverse: proposals *other* factions make that we have not considered and should.

7. **Sources** — every position traced to a document (protocol, motion, campaign page, budget
   vote) with a reference and an access date. Where a faction has published nothing on the
   subject and moved no motion, say so explicitly — absence of policy is a finding, not a blank
   cell.

## Honesty constraints

- Fill in every faction's column from its **own material and its own votes** first. Journalistic
  characterisation is a fallback, flagged as such.
- Read the Hebrew original. Council protocols and most municipal campaign material exist in Hebrew
  only, and a faction's English-language material, where it exists at all, is written for a
  different audience.
- Expect thin material. Municipal factions publish far less than national parties; record the
  thinness rather than filling the gap with inference about what they probably think.
- Do not conflate a faction with the coalition it sits in.
- A faction you disagree with on everything else may have the best instrument in one row. Record
  it.
