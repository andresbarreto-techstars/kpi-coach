# KPI vs goal/OKR, stage-awareness, and the unit rule

## The three objects founders confuse

Founders routinely fuse three different things. Name them:

- **Objective** — direction / vision. *"Become the default tool for X."*
- **Key Result / goal** — a time-bound target. *"$1M ARR by Q4."*
- **KPI** — the ongoing *unit you watch* to know if you're on track — not tied to any single target.

**Marathon test:**
- Objective = run faster than 99% of people.
- Goal / KR = finish a marathon in 2:30 (a target you hit or miss).
- **KPI = average pace** (the unit you steer by continuously).

If what the founder wrote is a target with a deadline, it's a **goal**, not a KPI. A KPI is a unit; a goal is a number you hit. OKRs are the vision and the milestones; KPIs are the measurement along the way.

## Stage-awareness (pre- vs post-PMF)

The primary/secondary hierarchy flips by stage:

- **Pre-PMF** — the **leading value driver is the primary KPI**; financials (revenue, LTV, margin) are lagging outcomes you only monitor. Steering by revenue here hides a leaky bucket and invites premature scaling.
- **Post-PMF (executing a known model)** — financial KPIs can legitimately move to primary; the value driver becomes a secondary/health metric.

"Pre-PMF" is about the *quality and durability of fit*, not the funding stage. A launched company doing real revenue and growing fast can still be pre-PMF if the growth is bought, retention decays, and there's no organic pull. Never accept "we have revenue/users" as proof of PMF.

## The unit-of-measurement rule (gate 9, expanded)

The founder's instinct to prefer **counts over percentages** is mostly right, for real reasons:

- **Counts are additive and decomposable.** You can sum them across segments, cohorts, and weeks and break them back down. Percentages don't add without re-weighting by their bases.
- **The delta of a count is a count** — same unit, unambiguous. The delta of a percentage is a minefield: 10% → 12% is *+2 percentage points* or *+20 percent*, and people conflate them. Week-over-week % change of a % is an index of an index nobody reads correctly.
- **Rates are gameable via the denominator** — "churn rate" improves if you stop acquiring marginal customers. A count of value delivered is harder to fake.

Where the instinct misleads — two cases genuinely need a denominator:

- **Retention** is inherently a curve of percentages; the normalization *is* the signal. Keep it a rate.
- **"Growth within existing customers"** (gate 4) is often best seen as a **per-active-account average** (events per account per week) — a ratio — precisely to strip out the acquisition effect a gross count would smuggle in.

**The operating rule:** store and difference the **counts**; treat every rate as a *derived read-out*, never the thing you difference — and never show a rate without its numerator and denominator beside it. On a dashboard: headline the value KPI as a count (or per-active-account average), keep retention as a curve, keep a *small* set of efficiency ratios (Quick Ratio, NDR, DAU/MAU) as diagnostics computed from the stored counts.
