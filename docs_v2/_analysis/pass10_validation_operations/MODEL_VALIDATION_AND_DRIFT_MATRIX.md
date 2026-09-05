# Model Validation and Drift Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Gate | Required evidence | Failure response |
|---|---|---|
| point-in-time data | immutable DatasetId, `training_end < validation_start`, availability audit | reject contaminated run |
| temporal generalization | ordered train/validation/test and walk-forward OOS | remain Challenger/Research |
| baseline | initial model beats naive constant survival on comparable OOS data | simpler baseline remains Champion |
| probability calibration | Brier, LogLoss, integrated Brier where applicable, reliability curves | recalibrate or disable dependent use |
| economic value | `EconomicLift > 0` after same costs/capital/Risk; drawdown/CVaR/recovery/capital use | no promotion |
| ablation | with/without advanced feature on same evidence | remove feature without robust incremental lift |
| support/OOD | validated markets, sizes, regimes, horizons, feed modes and OOD behavior | reduce size/fallback/reject |
| runtime/stability | latency budget, finite outputs, corruption/unavailable fallback | conservative fallback or strategy disable |
| Shadow/Micro-live | identical live features; predicted/actual calibration where decision-affecting | remain observe-only |
| continuous drift | feature/support, calibration, outcome error, OOD frequency, economics by slice | alert, demote, retrain offline |

Champion output alone may affect decisions; Challenger output is recorded only. A new version does not inherit Champion maturity. Live collection does not mutate weights or promote automatically. A persistent supported contradiction from Micro-live/Live outranks a favorable backtest; isolated trades do not alone prove persistent drift.
