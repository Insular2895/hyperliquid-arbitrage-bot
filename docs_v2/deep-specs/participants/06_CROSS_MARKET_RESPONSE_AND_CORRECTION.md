# 06 — Cross-Market Response and Correction

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Purpose and mechanical boundary

`CrossMarketResponseEngine` estimates how relevant markets may change after a source-market shock. An order on market `i` mechanically changes only market `i`. Movement on route neighbours is participant response or common-state evolution, never copied mechanical impact.

## Learned response object — QF-081

```text
R_{i->j}(h) = P(Delta Market_j(h) | Shock_i, X)
```

This is a target distribution, not a fixed coefficient. Outcomes can include mid, spread, depth, OFI, direction, response delay and quantiles at supported horizons. Model, neighbour graph, features, horizons and coefficients are learned/calibrated and versioned.

## Sparse response graph

Candidate targets are limited to:

- markets sharing an asset;
- direct route and triangle neighbours;
- strong empirically discovered lead/lag relationships.

`ResponseNeighborhood(i)` replaces an indiscriminate dense `AllMarkets` matrix. Sparsity bounds CPU/memory, reduces multiple-testing exposure and false correlations, and aligns inference with route relevance. Neighbour additions/removals are governed model changes.

## Discovery and event studies

Define `Shock_i` at `t0` without future information. For each candidate `j`, observe `DeltaMid_j(h)`, `DeltaSpread_j(h)`, `DeltaDepth_j(h)` and `OFI_j(h)` at fidelity-supported horizons, conditioning on direction, relative shock size, liquidity, volatility, regime and wider state.

Cross-correlation, lagged regression, lead/lag estimators and Granger-like methods are discovery tools only. Two markets can respond to a common factor; correlation or temporal precedence does not establish direct causal impact. Production requires later-window predictive improvement and with/without ablation.

Clock alignment and uncertainty are data validity requirements. A lead/lag smaller than timing uncertainty is inconclusive.

## Correction Velocity — QF-082

For initial edge `E_0` and edge at horizon `h`:

```text
Correction(h) = (E_0 - E_h) / E_0
```

`1` means disappearance; values above `1` represent crossing through zero. `E_0=0` is invalid. The conditional distribution `P(Correction(h)|X)` captures gradual decay that binary survival cannot.

## Dominant Decay Leg

Where episode attribution is sufficiently observable, `DominantDecayLeg` records the route leg most associated with economic death/correction. It may inform execution ordering, maker placement, size and recovery preference. It is a descriptive/predictive feature, not proof that one participant or market caused death.

## Route Competition Score

A `[0,1]` score built from hazard, half-life, correction speed, activity and optional fast-flow evidence may be exposed for monitoring. It is not a Formula Book risk gate. Risk consumes `p_survive`, arrival-edge distribution, response tails and confidence directly.

## Forecast and confidence

Logical output includes affected pairs, expected moves, move distributions, response-delay distributions and confidence per target. Exact `CrossMarketForecast` fields belong to Data Contracts.

Confidence reflects sample count, neighbourhood stability, clock quality, feed freshness/fidelity, shock/size/regime support and model dispersion. Unsupported targets/horizons are OOD and omitted or rejected; they are not returned as zero-response with high confidence.

## Risk and Simulator interfaces

- Simulator applies learned response to non-source books in interactive branches and preserves source-market mechanical separation.
- Risk checks route consistency and rejects stale-leg false arbitrage or insufficient cross-market confidence where the strategy depends on it.
- Execution may use probability of correction before later legs, never a claimed certain move.
- Market Atlas may store response strength and dominant decay summaries by window/version.

## Validation

- temporal and walk-forward splits across regimes/assets;
- null/common-factor and clock-perturbation tests;
- predictive calibration/error per target/horizon;
- sparse-neighbour stability and multiple-comparison controls;
- with/without cross-market ablation; SRC-006 requires OOS predictive improvement greater than zero before production use;
- replay economic lift and ModelValue after inference latency;
- OOD/fallback/fault tests and micro-live predicted-versus-observed response before scaling.

A safe fallback declares no validated response contribution plus conservative uncertainty or rejects the dependent route; it does not assert that other markets will remain static.

## Sources

SRC-004 QF-081/082; SRC-005 cross-market Risk/Data; SRC-006 validation and ablation; SRC-007 sparse response model; SRC-008 multi-market counterfactual boundary.
