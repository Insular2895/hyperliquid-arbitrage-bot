# CORR-03 — Completion Calibration Contract

DOCUMENTATION STATUS: VALIDATION CONTRACT — NO DECISION AUTHORITY

Evaluate the exact frozen decision-time `p_full` against authoritatively resolved `Y_full_route` using chronological/walk-forward OOS data. Never regenerate the forecast from final books. Report total attempts, exact joins, resolved, full, non-full, unresolved/censored/invalid, time interval, label/model/artifact versions and population scope beside every score.

Use QF-095 Brier and QF-096 Log Loss exactly as Formula Book defines them; QF-096 epsilon remains the existing versioned/calibrated numerical parameter. Reliability tables/curves compare predicted groups with observed resolved frequency and show support/uncertainty/unresolved counts. Global calibration is insufficient: inspect TT vs TTT, q/depth, latency, route/market family, volatility/regime, infrastructure and model version where support permits.

AUC/accuracy may be diagnostic but cannot prove probability quality. A complex Challenger must beat constant and empirical baselines on calibration, stability, OOD/fallback/runtime and, before decision influence, comparable QF-100 economic lift with no safety regression. Drift in base rate, calibration, partial/Recovery/UNKNOWN rate, latency or population support can demote authority.

No CORR-03 result sets a hard `p_full` threshold.
