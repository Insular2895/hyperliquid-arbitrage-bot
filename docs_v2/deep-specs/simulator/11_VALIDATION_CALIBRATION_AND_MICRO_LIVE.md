# 11 — Validation, Calibration, and Micro-live

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## Evidence progression

M0 Specified → M1 Unit → M2 Replay → M3 Shadow → M4 Micro-live → M5 Live. A capability cannot exceed its critical dependency. No evidence means no validation; fidelity availability does not imply capital authority.

## Offline Replay

Validate deterministic ordering, no look-ahead, RAW→normalized roundtrip, historical fees/rules, arrival reconstruction, exact mechanics fixtures, partial/failure/recovery paths, queue bounds, seeded scenario repeatability, and invalid-data rejection. Use temporal/walk-forward OOS for learned response. Compare F0/F1/F2/F3 only with fidelity labels.

## Shadow

Shadow runs the same core on current live feed through `NullShadowTransport`. Compare opportunity evolution, edge survival, forecast arrival state, would-execute/would-size decisions, latency, observed liquidity and cross-market continuation, stability, and drift. Because no real order exists, Shadow cannot validate our causal impact or actual queue fill.

## Micro-live

Small real orders under strict calibrated Risk limits produce intervention evidence: send/ack/first/last fill, actual fill/partial/cancel, execution price/slippage/fees, recovery, PnL, and post-trade book/response. Historic `€40–50` is an example of a calibration probe, not a fixed production rule.

## Predicted versus Actual

| Capability | Comparison |
|---|---|
| Latency/arrival | predicted latency/arrival book versus measured trace/state |
| Fill/partial | probability buckets and quantities versus outcomes; QF-099 |
| Time-to-fill | predicted survival/CDF/quantiles versus realized times |
| Slippage | `ActualSlippage - PredictedSlippage`, mean and quantiles |
| Adverse selection | QF-054/QF-055 horizon outcomes |
| Response/resilience | depth/spread/price/replenishment/cross-market distributions |
| Recovery | predicted path/loss versus actual QF-080 outcome |
| PnL distribution | mean, median, quantiles, P+, partial/recovery rates, VaR/CVaR coverage |

A repeated 95% interval should cover approximately 95% of comparable outcomes under valid assumptions. Exact estimators, sample minima, and tolerances remain calibrated.

## Champion / Challenger

New response/queue/simulator versions run on the same point-in-time data and costs as the Champion. Promotion requires temporal OOS prediction, distribution calibration, execution/economic lift, performance, failure/OOD/fallback tests, Shadow, and Micro-live where decision-affecting. Challenger output cannot alter Live decisions before promotion.

## Drift, precedence, and kill switch

Monitor calibration error, PnL bias, distribution coverage, model disagreement, OOD frequency, and support drift by slice. `Backtest Cannot Override Live Evidence`: persistent statistically supported live contradiction wins. Risk consumes model/version/confidence/drift and owns the `Simulator Calibration Kill Switch`: reduce size, fall back conservatively, or disable dependent strategies. Three isolated trades are not automatically persistent drift.
