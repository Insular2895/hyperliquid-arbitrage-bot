# Route Fanout Decision-Policy Contract

`DOCUMENTATION STATUS: CALIBRATED — AWAITING FINAL HUMAN REVIEW`

## Common invariants

For one committed market-state change, `pair_to_routes` produces a deterministic relevant route set under one Graph/index generation. Evaluation may be inline or use bounded C2 jobs, but:

- every result binds the complete canonical input tuple;
- missing/late/stale results have explicit disposition;
- completion order is never route priority;
- shared book/capital capacity is committed once in C0;
- final Risk and Reservation use current state;
- distinct ordered source states are not silently coalesced.

## Policy A — `BATCH_SELECT`

Evaluate the declared relevant candidate set, wait only until all required results arrive or the bounded decision deadline closes, apply the specified fallback/missing-result rule, then optimize and commit with deterministic ordering/tie-breaks.

Benefits: fuller within-cycle comparison and compatibility with joint allocation. Costs: slowest required work influences decision latency and state age. “Batch” does not authorize an unbounded decision window.

## Policy B — `EARLY_COMMIT`

Candidates are considered in a predeclared deterministic economic priority, not worker arrival order. A candidate may close the decision only when all evidence required by the policy is present/current and its admissibility rule proves waiting is unnecessary for the declared objective. C0 then revalidates shared capacity, final Risk and Reservation.

Benefits: lower decision latency may preserve edge. Costs: a better later result may be missed. Evidence must quantify opportunity cost, fairness/starvation and capture/economics.

## Current disposition

The repository requires deterministic allocation and ordered commit but does not mandate whether a decision cycle waits for all affected-route computations. Therefore:

| Item | Status |
|---|---|
| current canonical winner | `NONE` |
| `BATCH_SELECT` | safe candidate; `CALIBRATED / REPLAY + SHADOW REQUIRED` |
| deterministic `EARLY_COMMIT` | safe candidate; `CALIBRATED / REPLAY + SHADOW REQUIRED` |
| first worker wins | `FORBIDDEN` |
| adaptive switching | `RESEARCH` only; separate semantic/promotion review |

The initial mostly-inline Core evaluates in deterministic order, minimizing scheduler ambiguity while both parallel policies remain inactive candidates.

## Required comparison

Same Dataset, events/order, Graph/routes, formulas, models, q domain, Risk, capacity, config and resource profile. Report EventToDecision/Send tails, state age, queue wait, stale/deadline rates, evaluated/missed/selected candidates, fairness, reservations/conflicts, DecisionTrace differences, funnel outcomes and robust economics. Shadow precedes any capital-bearing consideration.
