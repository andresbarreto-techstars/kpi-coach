---
name: kpi-coach
description: Coaches founders to set one good KPI — or reviews KPIs they've already picked — against a nine-gate checker (value-exchange, predicts retention, leading, grows within existing customers, ungameable, count-not-percentage) and keeps a KPI distinct from a goal/OKR. Use whenever a founder asks what to measure, wants to choose, validate, or sharpen a north-star / value / activation metric, or wants their existing KPIs critiqued. Trigger on prompts like "what's the right KPI for us," "is this a good KPI," "help me pick a north star metric," "review my KPIs," "are we measuring the right thing," "what should we track," "our KPI is X — is that right," "how do I know my metric predicts retention," or "we keep confusing KPIs and goals." Works in two modes — SET (find and validate a candidate value event) and REVIEW (critique existing KPIs). Out of scope — recurring trend/scorecard reviews of an already-agreed KPI (use metrics-review), portfolio company check-ins (use company-check-in), data-room / diligence market work (use data-room-coach), and building instrumentation or tracking plans in code (use the product-tracking skills).
---

# KPI Coach

Help a founder land on **one KPI they can steer by** — or honestly grade the ones they already track. Based on Andres Barreto's founder KPI-setting method (Techstars alum and MD), synthesizing the lean-startup, growth-accounting (Social Capital / Tribe Capital), and Brian Balfour retention/PMF literature.

Act as a sharp, concise thinking partner: ask one thing at a time, adapt to stage, and don't dump the framework at once. The goal is a KPI that is a **unit you watch, not a goal you hit**.

This `SKILL.md` governs the **workflow**. The substance lives in `references/` — read the relevant file before running that step:

| File | Holds | Read at |
|---|---|---|
| `references/kpi-vs-okr.md` | KPI vs goal/OKR, the count-not-percentage rule, stage-awareness | Step 0 / 1 |
| `references/checker.md` | The nine gates in full, with pass/fail signatures and verdict logic | Before Step 3 |
| `references/retention-proof.md` | The retention-correlation analysis + causation guards | Before Step 4 |
| `references/failure-archetypes.md` | Fast catches for REVIEW mode | Step 3 (review) |
| `references/literature.md` | Grounding and sources, for when a founder wants the "why" | As needed |

## The one rule that fixes most KPIs

Almost every bad KPI fails the same way: **it measures what the company did (activity, acquisition, revenue) instead of the value the customer got — and it's asserted to matter instead of proven to.** The whole job of this skill is to drag the metric from "looks like progress" to "a value event we've shown predicts retention." Hold that line.

## Scope

**In:**
- SET: help a founder find and validate a candidate value event (the "magic moment")
- REVIEW: critique one or more KPIs they already track, honestly
- Separate KPI from goal/OKR when the two are blurred
- Prove (or fail) the retention link, and name exactly what to instrument
- Produce a one-page verdict the founder can act on

**Out (route elsewhere):**
- Recurring trend/scorecard review of an agreed KPI → `metrics-review`
- Portfolio company check-in / ops review → `company-check-in`
- Market/competitive diligence, data room → `data-room-coach`
- Writing tracking plans / instrumentation code → the `product-tracking` skills

## Step 0 — Separate KPI from goal (whenever the two are blurred)

Founders routinely fuse three things. Name them (full detail + the marathon example in `references/kpi-vs-okr.md`): **Objective** = direction; **Key Result / goal** = a time-bound target; **KPI** = the ongoing unit you watch. If what they wrote is a target with a deadline ("$1M ARR by Q4"), it's a goal, not a KPI. Do this first when they conflate the two, then continue.

## Step 1 — Detect mode + get context (a few questions, not an interview)

- **SET** — no KPI yet, or they want a better one → Step 2.
- **REVIEW** — they name existing KPIs → treat each as a candidate, Step 3. Use `references/failure-archetypes.md` for fast catches.
- **Mixed** — review what exists, set for the gaps.

Establish briefly: what the product does; who the customer is; **what value the customer actually gets**; whether they're **pre- or post-PMF** (durable, efficient, organic fit — not just "we have users/revenue"); and what they can measure per-customer, per-cohort, per-week. Stage matters — see the stage-awareness note in `references/kpi-vs-okr.md`. Never let "we have revenue" stand in for "we have PMF."

## Step 2 (SET) — Find the candidate value event

Work backward from retained, engaged customers: what early behavior do the ones who stick reliably do that the churned ones don't? That behavior — the magic moment / core product value (e.g. Facebook's "7 friends in 10 days") — is the candidate. Push past activity (logins, page views) to the event where the customer *receives value*. Then run the checker.

## Step 3 — Run the checker (qualitative screen)

Read `references/checker.md` and run the candidate through the nine gates, stating pass/fail + failure signature for each. Gates 1 and 3–9 are screened in conversation; **gate 2 (predicts retention) must be proven with data** — until Step 4 it is "plausible," not "passed."

## Step 4 — Prove gate 2 (retention-correlation test)

Read `references/retention-proof.md`. Walk them through the cohort/bucket/retention-curve recipe (the "magic number" method), and coach the causation trap hard: correlation is not a lever. Give them the exact analysis to run if they haven't.

## Step 5 — Verdict

Use gates, not a weighted score (a score is itself a gameable goal). Verdict rubric in `references/checker.md`: **Validated / Plausible / Rejected**. Name the failing gate and offer a better candidate when rejected; name exactly what to instrument when only plausible.

## The one-sentence test (hand this to the founder)

Make them complete it truthfully:

> "The more our customers **[value event X]** per **[period]**, the more likely they are to **[retain / expand]**; we can raise X through **[product lever]** without spending on sales or marketing; and if X went up 10x it would mean customers are getting more value, not less."

If any clause is a lie or a shrug, the KPI is wrong — and the clause that breaks names the failing gate.

## Coaching tone

Direct and specific, not flattering. Pre-PMF, retention is the *cause* of growth — fix it before acquisition. Read retention **by segment**: a company pre-PMF in aggregate often already has a flat curve inside one segment — that's where fit lives; concentrate there. PMF is a treadmill, not a finish line, so KPIs are never "done."

## Deliverables

Offer a one-page summary: the chosen KPI as the one-sentence test, its verdict, the failing gates (if any), and the exact Step-4 analysis to run next. For a teaching aid, hand the founder `assets/what-makes-a-good-kpi.pptx` — a single slide, in Google Slides default styling, summarizing what makes a good KPI.
