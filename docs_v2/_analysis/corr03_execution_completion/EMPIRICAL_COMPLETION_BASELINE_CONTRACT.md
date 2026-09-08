# CORR-03 — Empirical Completion Baseline Contract

DOCUMENTATION STATUS: LEARNED/CALIBRATED ARTIFACT — NOT FORMULA AUTHORITY

The baseline answers: among comparable historical **real attempts**, using only information available before each attempt, how often did the intended strategy route fully complete?

Target `Y_full_route` is 1 only for `STRATEGY_ROUTE_COMPLETED`; it is 0 for authoritatively resolved non-completion classes; unresolved/invalid has no binary target. The raw resolved rate `n_full/n_resolved` is an analytical statistic, not a new QF.

## Baseline ladder

1. constant resolved completion rate within compatible strategy+mode scope;
2. transparent empirical conditional slices, initially separate `OWA+TT` and `Triangle+TTT`;
3. progressively broader fallback when a specific supported slice is sparse;
4. optional smoothing/shrinkage candidate to avoid 0/1 certainty from tiny samples;
5. complex models only as Challengers.

Initial focus is TT, then separately TTT. MT/MTT are excluded until maker evidence and horizon semantics exist. Output includes probability, full/resolved/unresolved counts, slice/fallback level, training interval, artifact/feature/label versions, scope/support/confidence and OOD/fallback reason. Exact support thresholds, hierarchy and smoothing are `CALIBRATED`.

No raw rate has Risk authority. The artifact first serves as Simulator calibration baseline/challenger/input candidate; Simulator remains owner of final `ExecutionForecast`.
