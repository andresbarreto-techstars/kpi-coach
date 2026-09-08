# Proving gate 2 — the retention-correlation test

This is what separates a real KPI from a plausible story. It is the same method Facebook used to find "7 friends in 10 days" and that Social Capital / Tribe Capital formalized as growth accounting. Walk the founder through it; if they haven't run it, hand them this as the exact analysis to do.

## The recipe

1. Take a **past cohort** of customers (enough history that retention has had time to play out).
2. Measure the **candidate event count** in an early, fixed window — first 7 / 14 / 30 days (pick the window that matches the product's natural cadence).
3. **Bucket** customers by that count: 0, 1–2, 3–5, 6+ … (adjust ranges to the data).
4. Plot each bucket's **retention curve** over the following weeks/months.
5. Read three things off the curves:
   - **Dose-response** — more of the event → visibly higher retention; the bucket curves are *separated*, not stacked on top of each other.
   - **Plateau** — the high-event buckets *flatten* to a non-zero floor. A flattening curve is the fingerprint of fit; a curve that decays to zero is not.
   - **Elbow** — the threshold where retention jumps. That's the **magic number** — the activation target to drive new users toward.

**Passes only if** higher usage tracks materially higher retention **and** the top cohorts flatten. If every bucket's curve looks the same, or all decay to zero, the event is not the value driver — reject it and find a better candidate.

## Read retention by segment

A company that looks pre-PMF in aggregate often already has a **flat curve inside one segment / use-case**. Always cut the curves by segment before concluding there's no fit — the segment where the curve flattens is where fit actually lives, and it's where the founder should concentrate. A blended average hides this.

## The causation trap (coach this hard)

"Users who do X retain better" is usually **correlation, not a lever** — X may just be a *symptom* of already-committed users. Driving X up for indifferent users then does nothing. Two guards:

1. **Temporal ordering** — measure X in an *early* window and retention *later*, so X precedes the outcome. Never measure both over the same period.
2. **Experiment / natural experiment** — the real proof is: when you *deliberately* drive X up for a matched or randomized set of accounts, does *their* retention improve? A product change, an onboarding nudge, or a natural before/after all count.

Until an experiment exists, the honest verdict is **"strong leading indicator," not "proven driver."** Say exactly that — it tells the founder the metric is worth steering by *and* what would upgrade it to Validated.

## Growth-accounting cross-check (optional, if they have the data)

Decompose each period's active customers (and, separately, revenue) into **new, retained, resurrected, churned**. Then:
- **Net new = new + resurrected − churned.**
- **Quick Ratio = (new + resurrected) / churned** — growth *efficiency*; > 1 means growing, and early-stage healthy is well above 1.

A company adding lots of *new* while churning lots is pre-PMF no matter what the top line says. This is the quantitative version of "retention is truth," and it keeps the primitives as counts (see gate 9).
