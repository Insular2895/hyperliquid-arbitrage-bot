# 06 — Maker Queue and Fill Simulation

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## Why maker differs

A taker usually walks available arrival depth immediately. A maker rests, competes in price-time order, may never fill, may fill partially after its edge decays, may lose a cancellation race, and may be selected adversely. Fee advantage alone is not value.

## L2 and L4

At insertion, existing same-price aggregate L2 quantity is a defensible `queue_ahead` bound under the declared price-time rule. Later aggregate reduction does not reveal trade versus cancel or whether cancellation was ahead/behind. Exact L2 queue position is unknowable. Architecture accepts richer L4/order identity later, but current Hyperliquid L4/spot availability is `EXTERNAL_REVALIDATION`; initial spot capability cannot require it.

## Three L2 queue modes

| Mode | Cancellation rule | Interpretation |
|---|---|---|
| `PESSIMISTIC` | Cancellations never reduce `queue_ahead`; only observed trades do. | Lower-bound fill scenario. |
| `OPTIMISTIC` | All cancellations at the level are treated as favourable/ahead. | Upper-bound sensitivity; never production truth. |
| `PROBABILISTIC` | Calibrated `P(cancel ahead \| state)` and flow allocate advancement stochastically. | Expected/distributional scenario inside validated support. |

All three can be reported together as a robustness envelope. A strategy viable only under `OPTIMISTIC` is not robust.

## Required outputs

- `P(fill before h)` across supported horizons;
- time-to-first-fill and time-to-full-fill distributions;
- QF-051 fill survival, QF-052 fill CDF, QF-053 expected fill time;
- partial-fill probability and expected filled quantity;
- resting survival/edge viability, expiry/cancel outcome, and cancel/fill race;
- QF-054/QF-055 adverse selection by supported horizon;
- second-leg and recovery distributions for MT through QF-058;
- queue mode/observability, model version, support, OOD, and confidence.

## Participant contract

PASS 02 `MakerForecast` supplies calibrated fill/adverse distributions. The Simulator owns the queue counterfactual and path sampling; Exchange/Execution owns acceptance, matching, cancels, and states. Do not treat expected fill as guaranteed or create a second forecast schema.

## Calibration and activation

Evaluate survival/CDF coherence, QF-099 fill calibration, timing/quantity error, adverse-selection error, cancel races, and economic lift after second leg/recovery. Shadow observes would-rest viability but cannot validate our actual fill. Micro-live is required before maker-dependent activation. Unsupported queue visibility or persistent miscalibration triggers conservative mode, reduced size, or rejection via Risk.
