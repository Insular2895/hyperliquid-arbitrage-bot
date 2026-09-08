# CORR-01 — Predicted vs Actual Capture Calibration

DOCUMENTATION STATUS: VALIDATION CONTRACT — IMPLEMENTATION NOT AUTHORIZED

## Immutable prediction freeze

At `T_PLAN_COMMITTED`, and again only if a plan is legitimately versioned/replanned before possible send, preserve the exact `ExecutionForecast` and forecast bundle used by Risk/Execution. The frozen record includes probabilities, distributions, horizon, `ForecastLabelVersion`, candidate/size/route objective, support/confidence/OOD, model/data/formula/config/schema versions and issue/valid-until times.

A post-outcome recomputation is a `COUNTERFACTUAL_MODEL` prediction and cannot replace the decision-time forecast.

## Join

```text
FrozenForecast
  --(ExecutionPlanCandidateId, ExecutionId, ForecastLabelVersion)-->
ExecutionOutcomeLabel
```

The join preserves zero-fill, reject, `UNKNOWN`, Recovery and negative-PnL outcomes. Missing actual labels remain `UNRESOLVED`/censored; they are not removed. If an inferred repair join is used, it is reported separately and excluded from primary calibration.

## Comparable labels

| Forecast object | Primary actual label |
|---|---|
| `p_full` | for `ROUTE_OUTCOME_RESOLVED_V1`, eventual `CF-27 FULL_ROUTE_COMPLETED`, actual-fill proved, no Recovery |
| `p_partial` | eventual resolved non-completion with nonzero strategy fill and no Recovery entry |
| `p_recovery` | eventual resolved non-completion with `CF-28 RECOVERY_ENTERED`, regardless of recovery result/PnL |
| `p_failure` | residual eventual resolved zero-fill/no-Recovery non-completion; never `UNKNOWN` or negative PnL merely by itself |
| expected/quantile fill quantity | actual unique fill quantity by order/leg/route scope |
| expected fill time | actual local send-to-fill duration, with censoring |
| expected fees/slippage | reconciled actual components in identical units |
| expected PnL/quantiles/probability positive | economically complete attempt PnL at identical horizon/numeraire |

`ROUTE_OUTCOME_RESOLVED_V1` is mutually exclusive/exhaustive over eventual terminal classes; unresolved/censored/invalid outcomes at a cutoff remain unscored coverage. If another `ForecastLabelVersion` does not prove an exclusive/exhaustive partition, report separate binary forecasts; do not force a multinomial score or renormalize.

## Required diagnostics

- total forecasts, attempted joins, exact joins, inferred joins, unresolved outcomes and invalid label versions;
- calibration bins/reliability by probability target, Brier/log loss where QF definitions apply;
- observed rate and uncertainty per bin, expected calibration error only with declared weighting;
- interval coverage, sharpness and tail exceedances for continuous outcomes;
- signed and absolute error for fill, time, fees, slippage, Recovery and PnL;
- slices by mode, market/route family, size/depth, spread/volatility/regime, model/support/OOD, execution mode and infrastructure instance;
- censoring/maturity policy and observation-window cutoff.

## Bias controls

Primary analysis is attempt-cohort based. A separate opportunity-cohort analysis exposes selection into attempts. Training/calibration excludes look-ahead and binds point-in-time artifacts. Shadow predictions do not become actual execution labels. MicroLive/Live promotion evidence cannot pool different authority, capital or market populations without an explicit controlled design.

## Authority

Simulator emits forecasts; Execution/Recovery/Reconciliation/Accounting emit actuals; Data owns immutable lineage; Validation owns calibration judgments; Risk owns response to invalid calibration. The funnel projection cannot promote a model.
