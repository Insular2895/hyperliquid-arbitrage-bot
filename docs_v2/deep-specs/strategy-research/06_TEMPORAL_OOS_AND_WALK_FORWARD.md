# 06 — Temporal OOS and Walk-Forward

`DOCUMENTATION STATUS: F2 PART 2 / INTERMEDIATE DOCUMENTARY WORK / AWAITING HUMAN REVIEW`

`CAPABILITY STATUS: FUTURE SPECIFIED / NOT ACTIVE`

Temporal ordering is mandatory. Random row splits are insufficient for time-dependent market evidence.

The standard design has separate discovery/training, validation, and final untouched temporal holdout windows. The final holdout is evaluated once per declared decision family. If labels or features overlap through horizons, position lifetime, episodes or rolling windows, use purging and an evidence-justified embargo.

Walk-forward evaluation declares train/calibration/test windows, step, expanding or rolling policy, re-fit rules, warm-up, point-in-time feature availability and aggregation before results are observed. Each fold preserves Dataset, Run, model and report lineage. Missing or failed folds remain in the summary.

Minimum report: window boundaries; regimes and support; samples and effective independent units; leakage tests; calibration; economic, completion, tail and guardrail results; dispersion across folds; worst fold; parameter stability; OOD and missingness; unresolved coverage; comparison to the frozen baseline.

Selection cannot reuse the final holdout, tune on future folds or repair a losing fold without creating a new hypothesis/version and a new untouched evaluation period. Shadow and Micro-live remain later, distinct gates. Actual outcomes are sourced only from canonical Execution/Reconciliation evidence.

For Prompt-1 Falsifier work, the protocol—including splits, selection/region rules, T2 plan and
final-holdout policy—is frozen before every data-dependent T0 cell. T1 Discovery precedes
independent temporal Validation and walk-forward; T2 precedes the one-time final untouched
holdout. A later material `StrategyVersion` begins new lineage and states whether any earlier
window can legitimately transfer; it cannot inherit OOS status merely because it shares a parent.

Fee, metadata, feed capability, Formula, feature and Simulator versions are bound to each temporal
window. An external fee/feed/rule change creates a new fact/version boundary and drift/revalidation
question; historical results remain historical evidence rather than being recomputed as if the
new rule had always applied. Missing point-in-time truth yields limited/invalid evidence, not
backfilled certainty.
