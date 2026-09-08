# CORR-01 — Optimization Economic Value Contract

DOCUMENTATION STATUS: EVIDENCE GATE — NO OPTIMIZATION AUTHORIZED

## Required chain

```text
MEASURE -> ATTRIBUTE -> CHANGE -> REMEASURE
        -> FUNNEL EFFECT -> ACTUAL ECONOMIC EFFECT
        -> COST / UNCERTAINTY -> PROMOTE, REJECT OR ROLLBACK
```

An optimization is not valuable merely because a microbenchmark, mean latency or host score improves.

## Evidence layers

| Layer | Required evidence | Insufficient substitute |
|---|---|---|
| measurement validity | explicit `T_*` endpoints, clock domain, population, tails, invalid/missing counts and instrumentation overhead | label such as “tick-to-trade” alone |
| attribution | non-overlapping stage change, controlled workload/config, competing explanations and uncertainty | before/after on unrelated periods |
| technical effect | repeatable distributional improvement without regression in correctness, loss, jitter or safety | best/minimum sample |
| funnel effect | same-population change at specified funnel boundary, including unresolved/partials | opportunity anecdotes |
| economic effect | comparable actual PnL, QF-086–QF-093 as applicable, costs and lower-confidence evidence | estimated edge only |
| operational effect | failure modes, Recorder/telemetry health, recovery/reconciliation and rollback evidence | clean happy-path benchmark |

## Trial identity

Every candidate comparison binds `OptimizationTrialId`, baseline/candidate build and configuration, infrastructure instance, workload/dataset/seed, run mode, population definition, funnel/timing/metric versions, warm-up, sample count, cost horizon and predeclared acceptance/rollback rules.

## Decision rules

- A technical improvement may be kept as research evidence without production promotion.
- Promotion requires no safety/replay/correctness regression and the existing Validation/Capability gates.
- Infrastructure changes additionally use QF-084–QF-093 exactly as frozen; CORR-01 does not invent a new formula.
- If funnel or economic evidence is unavailable, disposition is `TECHNICALLY_PROMISING_NOT_ECONOMICALLY_VALIDATED`.
- Negative or null results are retained to prevent repeated unproductive optimization.
- A future hard decision threshold involving `p_full` remains `CALIBRATED` and Risk-owned; CORR-01 creates no new gate.

## Harjus comparative lesson

Harjus reported a lower average benchmark latency in release 4 alongside zero successful full triangular executions in the reported production run. This is not causal proof; it demonstrates why technical, funnel and economic evidence must remain separate. The external environment and implementation are not imported.
