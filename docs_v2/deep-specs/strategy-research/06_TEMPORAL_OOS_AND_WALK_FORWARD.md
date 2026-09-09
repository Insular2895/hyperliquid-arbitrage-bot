# 06 — Temporal OOS and Walk-Forward

STATUS: FUTURE SPECIFIED / NOT ACTIVE

Temporal ordering is mandatory. Random row splits are insufficient for time-dependent market evidence.

The standard design has separate discovery/training, validation, and final untouched temporal holdout windows. The final holdout is evaluated once per declared decision family. If labels or features overlap through horizons, position lifetime, episodes or rolling windows, use purging and an evidence-justified embargo.

Walk-forward evaluation declares train/calibration/test windows, step, expanding or rolling policy, re-fit rules, warm-up, point-in-time feature availability and aggregation before results are observed. Each fold preserves Dataset, Run, model and report lineage. Missing or failed folds remain in the summary.

Minimum report: window boundaries; regimes and support; samples and effective independent units; leakage tests; calibration; economic, completion, tail and guardrail results; dispersion across folds; worst fold; parameter stability; OOD and missingness; unresolved coverage; comparison to the frozen baseline.

Selection cannot reuse the final holdout, tune on future folds or repair a losing fold without creating a new hypothesis/version and a new untouched evaluation period. Shadow and Micro-live remain later, distinct gates. Actual outcomes are sourced only from canonical Execution/Reconciliation evidence.
