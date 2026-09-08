# The Checker — nine gates + verdict

Run the candidate KPI through these gates. For each, state **pass/fail** and, on a fail, the **failure signature** so the founder sees *why*. Gates 1 and 3–9 are screened in conversation; **gate 2 must be proven with data** (see `retention-proof.md`) — until then it is "plausible," not "passed."

## The nine gates

1. **Value-exchange, not activity.**
   Does the event mean the customer *got what they came for*? Finish the sentence: "more of this is good *for the customer*." 
   *Fails on:* plumbing — logins, sessions, DAU-without-value, page views, clicks.

2. **Predicts retention.** *(empirical — prove via `retention-proof.md`)*
   The more it happens, the longer they stay — demonstrated in the data, not asserted.
   *Fails if:* the retention curves for high- vs low-usage cohorts don't separate.

3. **Leading, not lagging.**
   Moves *before* revenue/renewal, so there's still time to act.
   *Fails on:* revenue, MRR, LTV, GMV, ARPU, NRR used as the primary KPI.

4. **Grows within existing customers (GTM-independent).**
   Can rise *without adding new logos* — a depth / frequency / expansion metric.
   *Fails if:* the only way to grow it is to acquire more customers (an acquisition metric in disguise).

5. **A unit, not a goal (Goodhart-safe).**
   If it 10x'd by any available means, are customers better off? Is it a rate/count, not a cumulative vanity total?
   *Fails if:* you can hit the number while making the customer worse off, or by shrinking a denominator.

6. **Controllable / actionable.**
   Can *this team, through product, this quarter* move it?
   *Fails if:* it's a scoreboard nobody can influence.

7. **Cohort-measurable at cadence.**
   Computable per-user, per-cohort, weekly, cheaply and reliably.
   *Fails if:* you can't cut it by cohort — then gate 2 can never be proven.

8. **Has headroom.**
   Room for the average customer to do much more of it?
   *Fails if:* the best cohorts are already saturated, so steering by it changes nothing.

9. **Right unit of measurement.**
   Headline it as a **count or a per-active-account average**, not a percentage — so you can add it up and take clean week-over-week deltas. Use rates only as *derived* diagnostics, always shown with their numerator and denominator. **Never make a percentage the thing you difference** (a percentage-of-a-percentage is uninterpretable; state rate changes in percentage *points*, with the Ns).
   *Exception:* retention itself stays a curve — the denominator is the point.
   *Fails on:* conversion %, MoM % headlined and differenced week over week.

## Verdict logic

Do **not** compute a weighted score — a score becomes a gameable goal (fails gate 5). Use gates:

- **Hard gates** (must all pass): 1, 3, 4, 5, 6, 7, and 9 as the unit fix.
- **Empirical gate:** the retention proof (`retention-proof.md`).

**Verdict:**
- **Validated** — passes all hard gates *and* the empirical test with temporal ordering (ideally a real experiment).
- **Plausible** — passes the screen, but the retention test isn't run yet or is observational only. Say so, and name exactly what to instrument.
- **Rejected** — fails any hard gate, or the retention curves don't separate. Name which gate failed and offer a better candidate.

Most named KPIs land at "Plausible" or "Rejected" on first pass. That's the normal, useful outcome — the coaching is in what to fix or measure next, not in a pass stamp.
