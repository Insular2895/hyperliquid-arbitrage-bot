# 04 — Liquidity Response, Replenishment and Resilience

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Model boundary

`LiquidityResponseEngine` estimates a distribution of book changes conditional on current state, observed flow and an optional intervention:

```text
P(Book_{t+h} | Book_t, Flow_t, OurShock)
```

It predicts participant response. It does not reproduce exchange mechanics, walk our order through the book, allocate exact maker queue cancellations or claim one deterministic future.

## Targets

At supported horizons the target distribution may include:

- changes in mid, microprice, best bid/ask and spread;
- future depth by side/band and probability of depth loss;
- limit adds, cancellations and aggressive buys/sells;
- replenishment amount, probability and time;
- uncertainty/quantiles and model confidence.

Targets are conditional on market/route, side, state, shock size relative to depth/volume, OFI, spread, volatility, regime, feed fidelity and relevant cross-market context.

## Mechanical impact versus response

If our taker order consumes a known visible level, that immediate quantity removal is deterministic mechanical impact owned by the Exchange Emulator/Simulator. A maker replacing liquidity, another participant cancelling, following flow or a neighbour market correcting is probabilistic participant response.

Training labels and simulation composition must exclude the mechanical delta from the learned residual response. Otherwise impact is double-counted. Other route books are never mechanically changed by an order on the source book.

## Replenishment and resilience

Let `D_0` be depth before a defined shock, `D_s` depth immediately after it, and `D_t` depth at horizon `t`. QF-043 defines:

```text
Resilience(t) = (D_t - D_s) / (D_0 - D_s)
```

The structure is locked. Shock definition, price band, side, horizon and aggregation are calibrated. `D_0 = D_s` is invalid. Display may clamp to `[0,1]`, while raw values may retain over-replenishment above one. A negative raw value can express further deterioration and must not be silently normalized away in model training.

Replenishment is not assumed guaranteed. A shock can be followed by recovery, further withdrawal or migration of liquidity to another level.

## Cancellation and toxicity

The model may estimate `P(CancelSoon | X)` when OFI, flow, cross-market fair value, spread or volatility indicate toxicity. This matters to taker arrival because currently visible depth can vanish, and to maker orders because counterparties may selectively trade against stale quotes.

Cancellation propensity is learned. A named regime such as `TOXIC` is a monitoring label, not a substitute for quantitative features or a universal threshold.

## Future Depth

The required object is:

```text
P(Depth(t_arrival) | X, optional OurShock)
```

not `Depth(now)` copied to arrival. Outputs may include expected depth, quantiles, `p_depth_loss`, spread forecast and replenishment forecast. The distribution must respect non-negative depth and declared market units. Support outside observed sizes, horizons or regimes is OOD.

Public L2 supports only coarse depth evolution. Exact add/cancel order, queue movement and sub-snapshot response require event-level capability and new calibration. Horizons must follow observable fidelity, market, size, volatility and replenishment rather than a universal constant.

## Slicing and maker/taker use

Slicing weighs potential replenishment against opportunity survival, correction, competition, inventory exposure and operational cost. Fast replenishment is worthless if the edge usually dies before the next child order. The Simulator/Sizing passes own the optimizer; this domain supplies calibrated distributions.

Taker forecasts assess depth likely to remain at arrival. Maker forecasts use cancellation/replenishment context for fill and adverse-selection estimates. Neither consumer may turn expected depth into a guaranteed fill.

## Output contract boundary

The logical `LiquidityForecast` includes expected arrival depth, depth quantiles, depth-loss probability, expected replenishment, spread forecast and confidence. The exact field schema and units remain owned by the Data Contracts pass. Every forecast needs model/version, as-of time, supported horizon/size/regime and input lineage.

## Validation

- define shocks without future information and separate exogenous from self-induced episodes;
- compare predicted versus observed depth/spread/add/cancel/replenishment distributions;
- temporal/walk-forward OOS by market, side, regime, size/depth and horizon;
- calibration/coverage and tail error, not mean error alone;
- ablate OFI, volatility, shock and cross-market features;
- test no-response/simple empirical baseline;
- reject impossible negative depths and double-impact composition;
- shadow and micro-live calibration before participant response changes real sizing/execution;
- validate EconomicLift and ModelValue after runtime cost.

Fallback is conservative current/empirical capacity with widened uncertainty or rejection, as allowed by Risk; never optimistic replenishment.

## Sources

SRC-004 QF-043; SRC-005 `LiquidityForecast`; SRC-006 Simulator F3 and temporal slicing; SRC-007 Liquidity Response/Future Depth; SRC-008 counterfactual response and resiliency.
