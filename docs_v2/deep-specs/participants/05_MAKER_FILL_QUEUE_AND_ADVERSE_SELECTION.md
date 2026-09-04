# 05 — Maker Fill, Queue and Adverse Selection

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Predictive boundary

The participant-side maker model estimates when and how much a resting order may fill and what adverse market move may follow. Exchange/Simulator owns order acceptance, price-time mechanics, deterministic matching, queue-state representation and counterfactual cancellation allocation. PASS 02 does not specify Pessimistic/Optimistic/Probabilistic Queue mechanics; PASS 03 owns them.

## Required forecasts

A maker forecast can include:

- `P(fill before h)` at supported horizons;
- probability and expected quantity of partial fill;
- time to first fill and time to full fill;
- expected fill time under an explicit horizon convention;
- edge/second-leg survival while resting and at fill;
- post-fill adverse selection by side and horizon;
- expected cleanup/recovery cost;
- confidence, OOD and provenance.

The source's example `p_fill_10/50/100` fields are conceptual; actual horizons must match data fidelity and calibration.

## Fill survival and CDF

For fill time `T_f` conditional on state `X`:

```text
S_f(t|X) = P(T_f > t | X)                                 QF-051, LEARNED
F_f(t|X) = P(T_f <= t | X) = 1 - S_f(t|X)                 QF-052, LOCKED
E[T_f] = integral_0^infinity S_f(t) dt                    QF-053, LOCKED
```

Discrete evaluation may sum survival over bins. If fills beyond the model horizon are not observable/supported, report the conditioning convention, such as expected time conditional on fill within horizon, rather than creating an artificial finite unconditional mean.

Fill curves must be coherent: survival in `[0,1]` and non-increasing, CDF non-decreasing, and partial/full-fill definitions explicit.

## Queue observability

Public L2 can estimate initial visible quantity but cannot establish exact future cancellation position or individual order lifecycle. The forecast must declare whether queue inputs are exact, bounded or probabilistic and which feed produced them. L2 cannot silently claim L4 queue fidelity.

Gap/reorder, reconnect, crossed/stale book, unknown own-order state or unsupported size invalidate affected maker forecasts. More granular node/event data remains future/external-dependent.

## Edge survival while resting

A maker order can remain unfilled while its economic rationale decays. The model therefore joins fill-time distribution with edge/second-leg viability at possible fill times. Maker expiry/cancel decisions are calibrated and remain owned by Execution/Risk.

For MT (`Maker A→X`, then `Taker X→B`), QF-058 expresses the locked structure:

```text
EV_MT = integral f_fill(t|X) EV_leg2(t) dt
        - C_adverse - C_recovery
```

The Formula/Execution domains own exact use. PASS 02 provides fill and post-fill distributions only.

## Adverse selection

Positive adverse selection means movement against the maker position. With fill price `P_f`, fill time `t_f` and later mid:

```text
AS_BUY(h)  = (P_f - Mid_{t_f+h}) / P_f                   QF-054
AS_SELL(h) = (Mid_{t_f+h} - P_f) / P_f                   QF-055
```

Multiply by `10^4` for bps where the consumer contract specifies bps. Horizons, conditioning, missing-mid rules and aggregation are calibrated. Predict `E[AS(h) | fill, X]` at multiple supported horizons, not an unconditional price move.

## Why maker fee advantage is insufficient

A fill may occur because informed/aggressive flow is moving through the quote. The second-leg edge may disappear, liquidity may be withdrawn, partial exposure may require recovery, and cancellation can lose a race. Maker selection must therefore include fill timing, adverse selection, survival, recovery and queue uncertainty—not current maker price plus current taker price.

## Maker toxicity and Risk

OFI, microprice/dislocation, volatility, signed flow, cross-market state and cancellation response may feed a learned toxicity estimate. On every actual fill, Risk/Execution immediately reassesses inventory, remaining edge, second-leg liquidity and recovery. Participant forecasts can tighten or block a maker capability but cannot override exposure, age or recovery limits.

## Validation and activation

- temporal/walk-forward evaluation with exact point-in-time book/own-order state;
- predicted fill buckets versus observed fill rate using QF-099;
- time-to-first/full-fill and partial-quantity calibration;
- adverse-selection error by side, horizon, market, regime and size;
- queue-observability/OOD, reconnect and cancellation-race tests;
- ablation against naive empirical fill and no-adverse-selection baselines;
- simulated-versus-live fill/adverse-selection calibration;
- second-leg and recovery testing in the Simulator;
- EconomicLift/ModelValue after latency and operational cost.

MT is not activated merely because the interface exists. SRC-006 requires calibrated fill and adverse selection plus tested leg-two recovery. Higher-risk TM/MM modes remain later execution decisions; MM is initially disabled in the source direction.

## Sources

SRC-004 QF-051..055 and reference-only QF-058; SRC-005 maker Risk; SRC-006 maker validation/activation; SRC-007 maker model; SRC-008 queue/counterfactual and MT boundaries.
