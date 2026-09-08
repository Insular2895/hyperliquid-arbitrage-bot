# CORR-03 — Per-Leg Fill Calibration Contract

DOCUMENTATION STATUS: DIAGNOSTIC TARGETS — ROUTE TARGET REMAINS PRIMARY

For leg k, permitted diagnostics include `P(any fill | leg k actually attempted)`, `P(full order fill | leg k actually attempted)`, continuous `q_filled/q_requested`, and censored time-to-first/full-fill. Denominators include only executions that reached and attempted that leg, with unresolved/invalid counts adjacent.

Raw per-leg probabilities must never be multiplied to obtain route completion. Legs are sequential, share market/regime/latency factors, and later-leg q/state exist only after actual earlier fills. A future decomposition would require calibrated conditional distributions such as `P(L2 outcome | actual L1 outcome, new state)`, not independence. CORR-03 adds no formula.

Per-leg diagnostics explain route failures; direct route-level `Y_full_route` remains the primary completion target. TT, TTT, MT and MTT keep separate mechanics and support.
