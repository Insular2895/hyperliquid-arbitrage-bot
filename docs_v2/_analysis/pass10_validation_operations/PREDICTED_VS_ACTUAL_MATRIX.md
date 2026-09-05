# Predicted-versus-Actual Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Object | Prediction | Actual | Comparison/slices |
|---|---|---|---|
| arrival | latency distribution and arrival book/edge | stage timestamps and observed book/edge | bias/quantiles/coverage by infra, market, regime |
| fill | probability, quantity and time distribution | zero/partial/full, quantity, first/last fill time | reliability/calibration by probability, size/depth, mode |
| slippage | distribution/quantiles | actual execution versus decision reference | signed error, mean and quantiles by spread/volatility |
| fees | predicted fee schedule/amount | exchange-accounted fee | exact difference by fee/version/tier |
| edge survival | survival curve/horizon probability | censored/observed end | Brier, LogLoss, integrated Brier, calibration |
| response | depth/spread/price/replenishment distribution | observed post-intervention path | coverage, sharpness and distribution distance |
| Recovery | selected path, probability, cost/loss/timing | actual child intents/fills/loss/duration | path/error/tail by failure class |
| PnL | full distribution after costs | realized route/Recovery/inventory/global PnL | bias, coverage, quantiles, P+, drawdown/tails |
| infrastructure | predicted capture/lost PnL | measured latency/outage and attributable outcome | comparable treatment and uncertainty |

Each row joins by stable attempt/execution/forecast IDs and exact input/version scope. Means alone are insufficient; reports include counts, missing joins, invalid intervals, tails, uncertainty and negative outcomes. New results append to evidence and never overwrite the original forecast.
