# 05 — Interactive Counterfactual and Market Response

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## World decomposition

`SimulationMode::InteractiveCounterfactual` uses:

```text
World_cf = HistoricalBaseline + Δour + Δresponse
```

`HistoricalBaseline` is the usable exogenous component. `Δour` is our necessary local mechanical intervention. `Δresponse` is the modeled conditional reaction of liquidity, flow, prices, queues, and linked markets. The decomposition is conceptual, not a new Formula Book equation.

## Initial response model

The first response Champion direction is a transparent **Conditional Empirical Model**. It compares historical events similar in market, side, trade size, size/depth, spread, depth, imbalance, OFI, microprice, realized volatility, recent intensity, regime, time, and cross-rate/route state. It estimates conditional distributions at supported horizons.

Expected outputs may cover `Δmid`, `Δmicroprice`, BBO/spread, depth loss/replenishment, cancels, new limit/market flow, and cross-market moves. Exact buckets, kernels, horizons, coefficients, and dependence representation are learned/calibrated, never hardcoded here.

## Forecast inputs

PASS 02 provides:

- `EdgeSurvivalForecast`: arrival survival, edge distribution, supported horizons/confidence;
- `LiquidityForecast`: arrival depth, depth quantiles/loss, replenishment, spread, confidence;
- `MakerForecast`: fill horizons/time, partial probability, adverse selection, confidence;
- `CrossMarketForecast`: sparse target responses and confidence.

Data Contracts owns their exact fields. The Simulator validates version/as-of/support/OOD, then draws or applies these distributions. It must not recompute a conflicting Participant model.

## Aggregate participants

Other traders are initially conditional event flow (`LIMIT_ADD`, `CANCEL`, `MARKET_BUY/SELL`) rather than invented Bot A/B identities. This captures observable aggregate effects without claiming actor identity or strategy.

## Challengers

Queue-Reactive models, Hawkes/point processes, nonlinear ML, and explicit agents may challenge the empirical Champion only with point-in-time temporal OOS calibration, distribution coverage, economic lift, runtime safety, Shadow/Micro-live evidence, and conservative fallback. Explicit agents remain F4 Research even when stylized statistics look realistic.

## Failure and OOD

Unsupported shock/size/regime/neighbour/horizon, low sample support, high dispersion, stale forecasts, or disagreement degrades confidence or rejects model-dependent response. No random noise fills a missing model. When no response is validated, Exogenous/F1 output may retain more authority than uncalibrated F3.
