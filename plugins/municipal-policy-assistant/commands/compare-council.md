---
description: Build a comparison matrix for an area — what every council faction proposes, how they actually voted, and where our gaps are
argument-hint: <policy-area>
---

Build the comparison matrix for: **$ARGUMENTS**. Output goes to `context/matrices/$ARGUMENTS.md`, following the format defined in `context/matrices/index.md`. Follow the `municipal-policy-methodology` skill's evidence rules — a comparison matrix is a factual claim about other people's positions, and getting one wrong is the fastest way to lose the project's credibility.

## Inputs

- `context/the-election/` and `context/city-hall/` — the electoral situation, the current council and its factions
- `policy/$ARGUMENTS/research/` — our evidence base, especially `02-jurisdiction.md` and `06-city-hall-record.md`
- `site/public/papers/$ARGUMENTS.typ` — our proposals, if the paper is drafted

## Method

1. **Fix the rows first.** Write the scope questions before looking at any faction's position. Rows chosen after reading the platforms get gerrymandered toward a predetermined winner — decide what matters, then see who addresses it.

2. **Fill each column from the faction's own published material.** Campaign material, faction website, council motions its members moved, and the portfolio record of any of its members holding a deputy mayoralty or committee chair. Read the Hebrew original. Municipal factions publish far less than national parties, so expect thin material — and note that thinness in the matrix rather than filling the gap with inference.

3. **Weight the voting record above the platform.** This is the biggest difference from the national version. Council votes are recorded in the protocols, they are recent, and they are about the actual instruments in play. **A faction's votes are better evidence of its position than anything it published**, and where the two conflict the matrix shows both and says which is which.

4. **Record absence explicitly.** "No published position as of <date>; no motion moved in this council term" is a finding and belongs in the cell. Never leave a blank that reads as unknown when it is actually nothing.

5. **Rate on a stated scale**, applied identically to every column including ours. The load-bearing distinction is a concrete mechanism (named bylaw, budget line, tender clause, council decision) versus a stated aspiration.

6. **Add the deliverability row.** For each column, how many of that faction's commitments in this area are class A/B/C/D against our own jurisdiction map. A faction promising things no municipality can do is a factual finding about that platform, and it is checkable. Apply it to our column too.

7. **Write the gap analysis.** For each of our proposals: already adopted or funded / already promised by others / genuinely unaddressed / actively opposed by a bloc on the council. Then the inverse — proposals other factions make that we have not considered and should.

## Rules

- Every position traces to a document — protocol, motion, campaign page, budget vote — with a URL or a reference and an access date.
- Frontmatter carries `last-verified`. Council coalitions shift mid-term; every claim states *as of* when.
- Include our own column and rate it honestly, including on deliverability. If another faction's instrument is better than ours on a row, say so in the matrix and flag it for the policy paper to address — that flag is the entire point of the exercise.
- Do not conflate a faction with the coalition. A faction inside the coalition may have voted for something it opposes; note where the vote was bound.
- Finish by reporting: which of our proposals survive the gap analysis as genuinely distinctive, which are duplicative, which need a political answer because a bloc opposes them, and whether any faction is proposing something better than ours.
