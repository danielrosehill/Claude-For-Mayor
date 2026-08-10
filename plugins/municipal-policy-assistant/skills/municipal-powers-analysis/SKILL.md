---
name: municipal-powers-analysis
description: Method for establishing who actually holds the lever on a city problem — mapping a policy area across municipality, government ministries, statutory corporations and municipal companies, classifying each possible instrument A/B/C/D, and finding the powers City Hall already has and does not use. Load when writing policy/<area>/research/02-jurisdiction.md, when running /map-powers, or whenever asked "can the mayor actually do this".
---

# Municipal powers analysis

Every other stage of this pipeline is recognisable from national policy work. This one is the
reason the municipal version needs its own pipeline at all.

The question is narrow and it is answered with documents, not reasoning: **for this problem,
who holds each available lever?** Not who is blamed, not who has a department with the right
name on the door, not who the mayor said was responsible. Who is named in the instrument.

Two failures are equally bad and this stage exists to prevent both:

- **The false promise** — proposing something the municipality cannot do. It is the standard
  municipal campaign move and it discredits everything around it.
- **The missed lever** — concluding "that's the government's" about something the municipality
  has been able to do by bylaw or licensing condition for thirty years and has not. This is the
  more common error in practice, and finding one of these is the highest-value output this
  project can produce.

Follows the evidence standards in the `municipal-policy-methodology` skill. Everything there
applies here; this skill adds the jurisdictional method and the vires gate's evidentiary basis.

## Output

```
policy/<area>/research/
└── 02-jurisdiction.md      the powers map for this area — who holds what, with citations
```

Written **before** the comparative review and before any proposal drafting. A comparative
review conducted without knowing which class of instrument is available produces case studies
about powers we do not have.

## The classes

Every lever gets exactly one:

| Class | Definition |
|-------|------------|
| **A** | Municipality decides and funds. Council resolution, bylaw, tender term, licensing condition, budget line, enforcement priority, or a discretionary power already delegated to an official. |
| **B** | Municipality decides, an external body must approve. Bylaws requiring the Interior Minister's confirmation, arnona deviations, budget items needing district approval, plans needing the district planning committee. |
| **C** | Shared. Delivery, employment, funding and policy split between municipality and a national body — education, welfare, some enforcement. The municipality holds real leverage inside the arrangement; the point of the analysis is to find where. |
| **D** | No municipal power. Policing, national infrastructure, health funds, primary legislation, national taxation. Legitimate as advocacy, never as a promise. |

For every class-A and class-B lever, add the load-bearing question: **has it been used, by this
municipality or any other?** An unused class-A power is the best finding available.

## Method

1. **Enumerate the levers before assigning any of them.** List every mechanism that could
   bear on the problem — regulatory, fiscal, contractual, planning, informational,
   convening — without yet asking who owns it. Contractual and informational levers are the
   ones consistently forgotten, and they are disproportionately class A.

2. **Trace each to a named instrument.** A lever exists when you can cite the provision that
   creates it. Sources, in the order to try them:
   - The **Municipalities Ordinance** (פקודת העיריות [נוסח חדש]) — the general grant of
     municipal powers and duties, and the bylaw-making chapter. This is the foundational text;
     read the current consolidated version, not a summary.
   - The **municipality's own bylaws** (חוקי עזר) — the existing local legislation, per subject.
     What is already on the books is routinely more than anyone assumes.
   - **Subject-specific statutes** that assign a function to a local authority — planning and
     building, business licensing, education, welfare, sanitation, animals, signage, noise.
     Each names its authority explicitly; that name settles the class.
   - **Ministerial orders, regulations and directives** (תקנות, חוזרי מנכ"ל) — the Interior
     Ministry director-general's circulars in particular bind municipal practice and are
     published.
   - **The municipal budget and organisational chart** — a department with staff and a budget
     line is a power in practice whatever the statute says; a statutory power with no staff is
     not.
   - **Tenders, concessions and contracts** the municipality is party to. Conditions the city
     can attach at renewal are class-A levers hiding in procurement.

3. **Map the other actors by name, not by category.** For each problem the list typically
   includes some of: the relevant government ministry and its Jerusalem district office; the
   local planning and building committee (ועדה מקומית) and the district committee
   (ועדה מחוזית) — note which one the municipality controls; the Israel Land Authority
   (רשות מקרקעי ישראל); the police district; statutory corporations and government companies;
   the municipal companies and quasi-municipal bodies the city acts through; and, in Jerusalem,
   the community administrations (מנהלים קהילתיים). Record what each one's formal role is and
   what its actual role is, and note where those differ.

4. **Find the consultee and consent points.** Where the municipality is class C or D, it will
   usually still appear somewhere in the other body's process — as a statutory consultee, as
   the owner of the land, as the issuer of a required permit, as the body whose objection
   triggers a hearing. **These are the leverage points and they are the whole reason a class-D
   problem can still yield a real proposal.** Name each one and cite the provision that creates
   it.

5. **Check the money separately from the power.** Power and funding are separated constantly in
   Israeli local government: functions the municipality must perform and the state must fund,
   matched-funding arrangements, ring-fenced ministry budgets administered locally, and
   earmarked grants. Establish for each lever who pays, in what proportion, and whether the
   money is discretionary or formula-driven. A duty with no funding attached is a finding.

6. **Test the classification against precedent.** Has another Israeli municipality done this?
   Tel Aviv-Yafo, Haifa, Beersheba, Rishon LeZion, Netanya, and the smaller councils that
   innovate cheaply. **If another municipality has already done it, it is class A or B by
   demonstration, whatever the legal analysis suggested** — and the surviving question is why
   Jerusalem has not. This test overrides theoretical reasoning and should be run early.

7. **Write the map**, then state the constraint it imposes on the proposal.

## Structure of `02-jurisdiction.md`

1. **The lever table** — the document's spine. One row per lever: what it is, the instrument
   and citation, who holds it, class, currently used (yes / no / partially), and evidence.
2. **What the municipality can do on its own motion** — the class-A levers, in order of how
   available they are. For each, whether it has ever been used here or elsewhere.
3. **What needs approval, and from whom** — class B, with the approving body's stated criteria
   and its record on comparable requests. "Requires ministerial approval" is not a verdict
   until you know how that ministry decides.
4. **The shared arrangements** — class C, with the split set out precisely and the municipal
   leverage points inside it named.
5. **What is not the municipality's at all** — class D, stated plainly, with the consultee and
   consent points from step 4 and the realistic advocacy route for each.
6. **The unused powers** — a dedicated section. Class-A and class-B levers that exist and are
   not being used, with whatever evidence exists as to why. Flag each explicitly for the policy
   paper.
7. **Who residents think is responsible** — where the testimony or public debate misattributes
   responsibility. This is a finding about the accountability gap in its own right, and it
   usually points at an information proposal.
8. **Implications for the proposal** — the design constraint each of the above imposes, and the
   classes the paper is permitted to draw on.

## Rules specific to powers work

- **Cite the provision or do not claim the power.** "The municipality is responsible for X" with
  no citation is exactly the kind of confident, unsourced statement this project exists to
  avoid. Unsourced attributions are marked `[UNVERIFIED — verify before publication]` and block
  stage advancement like any other.
- **Hebrew sources are primary.** Ordinances, bylaws, regulations, circulars and protocols are
  authoritative in Hebrew; English summaries are partial, dated, and frequently describe a
  pre-amendment position. Quote the Hebrew name with an English translation.
- **Verify the current version.** Municipal powers move — functions have been transferred to
  national authorities and back, and reform bills to replace the Municipalities Ordinance have
  been attempted repeatedly without passing. State the position and the date you checked it.
- **Do not reason from the department's name.** A municipal department may deliver a service it
  has no authority over, and hold authority over something it does not deliver. The instrument
  decides.
- **Distinguish "cannot" from "has chosen not to".** Political impossibility, coalition
  arithmetic on the council, and Treasury resistance are real and belong in the record research —
  but they are not the same as absence of power, and collapsing them lets a live lever get
  written off. Where a power exists and is unused, say that, then explain the politics
  separately.
- **The mayor is not the municipality.** Mayoral powers, council powers, committee powers and
  officials' delegated powers are different things. A proposal that needs a council majority
  needs a council majority; say so and count it.
