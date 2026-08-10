---
title: The powers doctrine
description: The rule that separates a mayoral platform from a wish list — every proposal traced to a named instrument and a named holder of it, and classified by whether the municipality can actually deliver it.
sidebar:
  label: The powers doctrine
  order: 1
---

This is the one methodological commitment that makes a municipal platform different from a
national one, and it is the reason this project exists as a separate experiment rather than a
chapter of [MK-Claude](https://github.com/danielrosehill/MK-Claude).

## The problem it solves

A mayor is elected on promises about schools, buses, policing, healthcare, cleanliness, housing
and parks. Of those seven, a municipality's formal power over each ranges from near-total to
essentially none, and the ranking is not the one residents assume. Meanwhile the powers a
municipality unambiguously does hold — what it writes into a contract, what conditions it
attaches to a licence, what it instructs its inspectors to enforce, what it publishes — get
almost no attention in campaigns, because they are unglamorous and specific.

Two failures follow, and they are equally bad:

**The false promise.** Proposing something the municipality cannot do. It is the standard move
of municipal campaigning, and when the winner discovers the constraint in office, the failure is
attributed to the person rather than to the promise.

**The missed lever.** Concluding "that's the government's problem" about something the
municipality has been able to do by bylaw for thirty years and has not. This is the more common
error in practice, and finding one is the most valuable thing this project can produce.

## The rule

> **No proposal enters a policy paper without a named instrument and a named holder of it.**

Every lever is traced to the provision that creates it, and classified:

| Class | Meaning | What the paper must show |
|:-----:|---------|--------------------------|
| **A** | Municipality decides and funds | The instrument — bylaw section, tender clause, licensing condition, budget line, council decision, enforcement priority — the department that administers it, and **why it has not already been used** |
| **B** | Municipality decides, an external body must approve | The approving body, the statutory basis for its consent, and evidence of how it has decided comparable requests |
| **C** | Shared — delivery municipal, policy or funding national | The split, precisely: who sets policy, who employs the staff, who pays what share — and the leverage the municipality holds inside the arrangement |
| **D** | No municipal power | Said plainly, then either dropped or reclassified as an **advocacy** proposal with a named counterpart, a specific ask, and a realistic route |

Every recommendation in every paper carries its class letter. The
[program for the city](../platform/index.md) is sorted by class before it is sorted by theme,
because the reader's first question about a municipal platform is "which of this could you
actually do?" and the document should answer it before it argues anything.

## What this does and does not license

**Class D is not a reason to stop.** A municipality with no formal power over a problem almost
always still appears somewhere in someone else's process — as a statutory consultee, as the
owner of the land, as the issuer of a permit the project needs, as the body whose objection
triggers a hearing. Those points are leverage, they are citable, and finding them is what turns a
class-D problem into a real advocacy proposal rather than a complaint. What class D forbids is
presenting the outcome as something a mayor delivers.

**"Requires ministerial approval" is not a verdict.** Class B is a real constraint but a
soft one, and it becomes analysable the moment you know how that ministry has decided comparable
requests. A proposal that needs consent and shows the consent pattern is stronger than one that
needs nothing and does nothing.

**Political impossibility is not absence of power.** Coalition arithmetic on the council,
departmental resistance and Treasury pressure are real, they belong in the record research, and
they are recorded — but they are not the same thing as lacking the authority, and collapsing the
two is how a live lever gets written off. Where a power exists and is unused, the paper says
that, and then explains the politics separately.

**The mayor is not the municipality.** Mayoral powers, council powers, committee powers and
officials' delegated powers are different things. A proposal that needs a council majority needs
a council majority, and the platform counts the votes.

## The precedent test

The analysis has a shortcut that overrides theoretical reasoning, and it should be run early:
**if another Israeli municipality has already done it, it is class A or B by demonstration.**
Tel Aviv-Yafo, Haifa, Beersheba and the smaller councils operate under the same Municipalities
Ordinance, the same ministries, the same arnona rules and the same planning system. Where one of
them has acted, the feasibility question is settled and the surviving question is why Jerusalem
has not — which is a much better question, and one with an answer somewhere in the
[city-hall record](../pipeline.md).

## Where it is applied

The doctrine is executed by the `municipal-powers-analysis` skill and the `/map-powers` command
in the [plugin](./plugin.md), producing `02-jurisdiction.md` for each policy area before any
proposal is drafted. `/draft-paper` refuses to run on an area that has not been mapped.
