# Data, Learning and Experiment Dependencies

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

## Target-before-model rule

Before a predictive model exists, its target must be observable, defined, labelable, recordable and validatable. Knowing a mathematical target does not mean the dataset contains it.

| Target family | Earliest source | Required label discipline | Safe initial baseline |
|---|---|---|---|
| Opportunity/Edge(q) | Valid book + Graph + NetConvert | Point-in-time versions, rejected and accepted candidates | Deterministic formula engine |
| Survival/correction/capture | Opportunity episodes and future valid market state | Birth/death/censor/cause/horizon/support | Constant or simple empirical survival |
| Maker fill/time/adverse | Maker rest/queue proxy/trade/cancel/fill episodes | Right censoring, queue visibility, fill-conditioned outcome | Pessimistic/simple empirical model |
| Liquidity/cross-market response | Synchronized point-in-time shock/response episodes | Sparse neighborhood, no future leakage, confounding disclosed | Local empirical response/no-response fallback |
| Recovery loss | Recovery-start state through terminal actual outcome | Sunk-cost boundary, failed outcomes retained | Deterministic bounded recovery scenarios |
| Q_validated | Full q curve plus every safety/evidence gate | Exact market/mode/model/regime/infra/version scope | Conservative minimum of known gates |
| Bridge utility | Atlas history plus capital/exit/utilization outcomes | STAY comparator and future horizon declared | STAY |
| Infra economics | Same-event host evidence plus survival/capture | Clock uncertainty and selection bias explicit | Current validated host |

## Experimental protocol

Every major experiment declares hypothesis, target, primary/guardrail metrics, dataset/time split, support, formulas/models/config/build, validity/exclusion rules, stop/go criteria and consumer. Its output is an immutable `ModelReport`, `ReplayReport`, `ValidationReport` or `InfraBenchmark`; negative results stay archived.

## Point-in-time law

At decision time T, the run may consume only data, metadata, fees, models, Atlas fields, configs and formula/schema artifacts available by T. A modern model on old data is a labeled research counterfactual, never Historical Truth. Random row splits are forbidden for time series; temporal OOS/walk-forward applies.

## Prediction-to-actual law

A prediction is immutable before intervention and linked by stable IDs to actual arrival, ACK, fills, fees, slippage, Recovery, account and PnL. Reports include missing joins, count, support slices, bias, calibration, quantiles, coverage and tails. Post-hoc bucketing cannot define success.

The row-level map is [EXPERIMENT_AND_DATA_REQUIREMENT_MAP.md](../../_analysis/pass12_build_validate_scale/EXPERIMENT_AND_DATA_REQUIREMENT_MAP.md).
