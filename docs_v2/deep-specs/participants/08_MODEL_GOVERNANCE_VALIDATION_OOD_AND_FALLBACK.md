# 08 — Model Governance, Validation, OOD and Fallback

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Status model

`LOCKED` applies to required mathematical objects, interfaces, safety properties and governance. `LEARNED` applies to fitted relationships and coefficients. `CALIBRATED` applies to windows, horizons, thresholds and operational budgets. `CHALLENGER`, `RESEARCH`, `FUTURE` and `EXTERNAL_DEPENDENT` do not authorize production use.

## Model portfolio

| Capability | Classification | Production condition |
|---|---|---|
| Naive constant survival | Validation baseline | Always retained for comparison, not preferred by assumption. |
| Stratified empirical survival | Initial Champion direction and conservative fallback | Sufficient support, censor-aware temporal calibration and safe runtime. |
| Discrete hazard | Production-capable learned challenger/Champion candidate | Validated coefficients, calibration, economics, runtime and fallback. |
| Liquidity response | Locked interface, not yet calibrated | F3 use after distribution calibration and simulated/live comparison. |
| Maker fill/adverse selection | Locked interfaces, not yet calibrated | Required before dependent maker activation. |
| Sparse cross-market response | Locked architecture, learned model | OOS predictive improvement, ablation, clock validity and safe OOD. |
| Address behaviour | P4 Research/Future, external-dependent | Stable incremental lift and privacy/data approval. |
| Survival GBDT | Challenger | Beats simple Champion robustly after all costs. |
| Deep survival | Research/Future | Only if added calibration/economic value, robustness and runtime justify it. |
| Queue-Reactive | P5 Challenger/Research | Event fidelity and measurable gain over simpler hazard/response models. |
| Hawkes | P5 Challenger/Research | Self-/cross-excitation adds robust value with acceptable complexity. |
| Explicit agents | P5 Research/stress only | Never production truth merely because stylized facts look realistic. |

## Offline lifecycle

```text
record immutable point-in-time data
  -> label episodes/censoring
  -> train in Python
  -> temporal validation and calibration
  -> export versioned compact artifact
  -> shadow Challenger on identical live features
  -> micro-live comparison where required
  -> explicit promotion decision
  -> bounded Rust inference
```

The live bot collects outcomes but does not mutate weights every second. Online self-learning is initially forbidden because it creates feedback loops, corruption, instability and unauditable regime adaptation.

## Artifact and feature provenance

Every model artifact includes:

- `model_id`, semantic/model version and artifact checksum/signature;
- training dataset ID and start/end times;
- feature schema and formula versions;
- source code Git commit and hyperparameters;
- supported markets, sizes, regimes, feed modes and horizons;
- calibration/statistical/economic metrics and validation manifest;
- runtime budget, fallback ID and approval state.

Inference rejects missing, stale, mismatched or non-finite inputs/outputs.

## Temporal validation

Random row splits are forbidden. Use ordered train/validation/test intervals and walk-forward windows. Evaluate later regimes, new assets, high volatility, low liquidity, size/depth buckets, feed modes and censored episodes separately. All features and neighbourhoods are reconstructed as known at decision time.

The initial Champion must beat a naive constant-survival baseline out of sample. Cross-market and address features require with/without ablation. Maker models require fill and adverse-selection calibration plus second-leg/recovery testing.

## Statistical calibration

For binary horizon outcomes:

```text
Brier = (1/N) sum_i (p_i-y_i)^2                          QF-095
LogLoss = -(1/N) sum_i [y_i ln p_i +(1-y_i)ln(1-p_i)]    QF-096
```

Probabilities are numerically clipped for Log Loss as specified by Formula authority. Survival models additionally use integrated Brier, calibration curves and ranking/concordance where supported. A predicted 0.8 bucket should observe roughly 80% outcomes within statistical uncertainty; PASS 02 invents no tolerance.

Maker fill calibration uses:

```text
CalibrationError_B = ObservedFillRate_B - MeanPredictedFill_B   QF-099
```

Metrics are sliced by horizon, market, regime, size, fidelity and support. Aggregate scores must not hide unsafe tails or slices.

## Economic and latency value

```text
EconomicLift = NetPnL_model - NetPnL_baseline             QF-100
```

Both arms use the same dataset, capital, fees and risk budget. Also compare drawdown, CVaR, partial fills, recovery loss and capital utilization.

```text
ModelValue = PnL_with - PnL_without
             - PnLLostDueToAddedLatency - OperationalCost QF-101
```

A statistically superior model is not promoted if added latency or operations destroy value. Promotion requires robust positive value out of sample, not one favourable run.

## OOD

QF-103 locks only the contract: `OODScore >= 0`, with larger values farther outside validated support. The method is model-dependent—feature-range, Mahalanobis, density, tree support or neighbour distance—and must be versioned and validated. Size, regime, route, market, feed fidelity, feature age and latency horizon all contribute to support.

An order representing far more depth than training data is OOD; the model must not return high-confidence extrapolation. OOD lowers confidence, reduces size or rejects the dependent capability according to Risk.

## Disagreement

For `M` comparable probabilistic predictions:

```text
p_bar = (1/M) sum_m p_m
Disagreement = sqrt[(1/M) sum_m (p_m-p_bar)^2]             QF-102
```

Disagreement may feed model uncertainty; its penalty mapping is calibrated. It is informative even when one model is a shadow Challenger. It never becomes permission to average away a hard safety failure.

## Drift

Monitor feature distributions, probability calibration, outcome error, model support and economic results over FAST/RECENT/MEDIUM/LONG windows. Regime labels are monitoring aids. Drift thresholds and remediation are calibrated and versioned.

Material drift can trigger `MODEL_KILL` for dependent strategies while leaving unrelated safe capabilities active. Recalibration happens offline and follows the full promotion process.

## Fallback and fault tests

For unavailable/corrupt models, NaN, schema mismatch, stale inputs, OOD, large disagreement or drift:

1. invalidate the forecast and expose a reason;
2. use conservative empirical survival only inside its support;
3. increase uncertainty/risk buffer and reduce size where Risk permits;
4. reject model-dependent routes or disable the affected strategy if no safe fallback exists.

Test model corruption, feature omission, stale forecasts, unsupported size/regime, disagreement, drift, feed degradation and fallback itself. Complexity must fail safe.

## Promotion decision record

No model is promoted automatically by this document. A later validation/governance decision records evidence, artifact, target capabilities, rollback/fallback and approver. Until then, architecture is specified but the model remains observe-only, Challenger or Research as classified.

## Sources

SRC-004 QF-094..103; SRC-005 Risk Constitution; SRC-006 Validation Matrix; SRC-007 model governance; SRC-008 confidence and participant simulation boundaries.
