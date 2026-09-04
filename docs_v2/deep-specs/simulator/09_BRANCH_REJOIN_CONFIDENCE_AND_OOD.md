# 09 — Branch/Rejoin, Confidence, and OOD

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## Branch-and-rejoin

Interactive simulation branches at intervention, keeps baseline and counterfactual deltas separate, and evolves only while the intervention remains material. It may rejoin history only through an explicit `CounterfactualRejoinEvent`; it must not silently replace branch state with baseline.

The rejoin condition is a calibrated compatibility rule informed by residual mechanical/response impact, QF-043 resilience, book/price/queue compatibility, multi-market divergence, model support, and confidence. The exact threshold is `CALIBRATED`, not architecture-locked.

## Variable horizon

Horizon depends on market, order size, depth/volume participation, ticks consumed, volatility, replenishment, response decay, queue exposure, and cross-market complexity. Tiny deep-market interventions may rejoin quickly. Large multi-tick or high-participation branches may require long horizons.

## Non-rejoin

If compatibility cannot be established within supported horizon, the Simulator does not force rejoin. It records residual state, reason, horizon, and confidence; returns conservative terminal/range semantics; and may label `LONG_HORIZON_COUNTERFACTUAL_UNRELIABLE`, `OOD`, or `REJECT`. Downstream Risk cannot interpret a non-rejoined branch as a validated long-run future.

## `SimulationConfidence`

QF-104 uses explicit gates rather than a fake fixed weighted score:

- Data fidelity and freshness;
- sample/model support and calibration health;
- OOD;
- model agreement;
- latency uncertainty;
- queue observability;
- response dispersion and cross-market complexity;
- intervention participation/support.

`ConfidenceState` explains why a result is `HIGH`, `MEDIUM`, `LOW`, or `REJECT`. Fidelity does not equal confidence; uncalibrated F3/F4 may have less authority than supported F1.

## OOD, disagreement, and drift

Size, participation, market, route, volatility/regime, queue state, shock, neighbour, or horizon outside training/validation support triggers OOD. Stale forecasts, schema/version mismatch, invalid data, model disagreement, and calibration drift also degrade confidence. Fallback is more conservative: reduce size, omit unsupported response with explicit lower fidelity, or reject.

## Capital and validation

Confidence participates in QF-076 gates but does not itself authorize capital. PASS 05 sets Risk action; PASS 07 chooses size. Rejoin calibration is assessed by post-trade residuals, branch/baseline compatibility, interval coverage, and false-rejoin/non-rejoin behaviour using Replay, Shadow where observable, and Micro-live.
