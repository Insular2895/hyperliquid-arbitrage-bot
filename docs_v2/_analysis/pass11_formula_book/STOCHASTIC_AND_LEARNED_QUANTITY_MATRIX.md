# Stochastic and Learned Quantity Matrix

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

| QF | Quantity | Status | Target / estimator boundary | Required provenance | Calibration/validation |
|---|---|---|---|---|---|
| 029 | level weights | calibrated prose component | formula fixed, weights versioned | config/evidence/window | OOS stability and parity |
| 033 | MLOFI weights | calibrated within locked structure | linear aggregation fixed | config/feature schema | incremental/batch parity |
| 039 | scale horizon/threshold | calibrated | score structure fixed | config/dataset | false-positive/stability evidence |
| 044 | survival object | locked target, modeled value | `P(T>t∣X)` | model/features/event/horizon | censor-aware calibration |
| 045 | discrete hazard | LEARNED | conditional bin hazard | artifact/training/features/bins | discrimination/calibration/OOD |
| 048 | latency expectation | locked functional over measured distribution | no invented parametric latency | infra profile/data window | empirical distribution/golden |
| 049 | arrival edge | LEARNED DISTRIBUTION | conditional expectation | artifact/features/latency/horizon | OOS error/economic value |
| 050 | above-threshold probability | LEARNED | same future-edge distribution | artifact/threshold/version | Brier/log/calibration |
| 051 | fill survival | LEARNED | conditional time-to-fill | order context/artifact/features | censor-aware fill calibration |
| 053 | expected fill time | locked functional over learned survival | integration/tail policy versioned | QF-051 artifact/support | horizon sensitivity |
| 054–055 | adverse-selection realized/expected inputs | locked realized measure; predictive use learned | side-specific future move | fill/event/horizon/model | sign/golden + OOS error |
| 056–058 | scenario probabilities/outcomes | locked EV structures, learned components | exclusive outcome distribution | simulator/model/seed/state | mass, Replay, calibration |
| 059–062 | distribution diagnostics/tail | locked functional; empirical estimator open | sample PnL/Loss | dataset/seed/estimator version | coverage/tail stability |
| 063/065/069 | penalties | calibrated structures/components | objective, not realized cost | config/evidence/scope | sensitivity and Risk approval |
| 071–072 | future cycle/destination/stay EV | modeled estimates inside locked identities | comparable horizon/state | model/config/data | realized economic validation |
| 075–078 | optimization | locked objective/gates; search/solver config | evaluate exact candidate outputs | algorithm/config/seed | feasibility/golden/stress |
| 081 | response distribution | LEARNED | target-market conditional change | markets/shock/artifact/features | OOS causal limits/calibration |
| 083 | competition hazard | LEARNED | global edge death first | artifact/event/time/features | censoring/OOD |
| 085–086/091 | captured/gross uplift distribution and LCB | locked comparisons, calibrated estimator | like-for-like infra experiment | profile/cohort/config | uncertainty/holdout |
| 094 | observed survival | locked ratio, censor estimator open | eligible cohort | cohort/horizon/censor policy | cohort sufficiency |
| 095–099 | scoring/calibration | locked metrics; bins/epsilon calibrated | same events/predictions/outcomes | dataset/model/horizon | bounds, calibration diagrams |
| 101 | model value | locked definition over experiment estimates | OOS net contribution | experiment/artifact/infra/cost | robust positive LCB |
| 102 | disagreement | locked feature over model outputs | population SD over aligned p | artifact set/event/horizon | stability/utility |
| 103 | OOD | MODEL DEPENDENT | only nonnegative/higher-worse contract fixed | estimator/support/artifact | in/out support tests |
| 104 | confidence | gated categorical rules | no fixed weighted scalar | six gate versions/results | truth table and promotion evidence |
| 105 | opportunity rate | CALIBRATED | empirical foregone opportunities | dataset/horizon/capital scope | sensitivity/realization |

Learned predictions are not facts. Historical actual, historical model-as-of-time, and later-model counterfactual outputs must remain separate in RunManifest and datasets.
