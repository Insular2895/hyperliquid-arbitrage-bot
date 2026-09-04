# 01 — Objective, Scope and Fidelity Ladder

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Production objective

Predict calibrated distributions of collective effects that matter to execution: remaining edge lifetime, correction, book response, fill, adverse selection and response across connected markets. The output is useful only if it improves net economic decisions under latency, uncertainty and risk.

## Explicit non-goals

- no psychological reconstruction of every trader;
- no invented bot population presented as observed truth;
- no real-world identity claim from a wallet address;
- no exact claim about an unobserved alternate future;
- no model complexity promoted for realism or novelty alone.

The terms `ParticipantAddress`, `BehaviourSignature`, `BehaviourCluster`, `CollectiveResponse` and `ParticipantModelConfidence` preserve the observable/model boundary.

## Why collective response comes first

For execution the useful questions are time- and outcome-based: when does the opportunity die; will it clear the execution threshold at our arrival; will depth cancel or replenish; will a maker fill before the edge dies; and which route leg or neighbouring market corrects? These outcomes can be labelled and falsified without knowing a competitor's identity or strategy.

Historical tape is already a sample of real participant activity. An empirical model built from it is a stronger initial production basis than a detailed synthetic population with unidentifiable behavioural parameters.

## P0–P5

| Level | Included capability | Boundary |
|---|---|---|
| `P0 Historical Participants` | Recorded books/trades/opportunity paths; real historical aggregate activity. | No counterfactual participant response. |
| `P1 Edge Survival` | Opportunity episodes, empirical survival, hazard, capture and arrival-edge forecasts. | First model layer; supported horizons only. |
| `P2 Aggregate Response` | OFI, additions, cancellations, aggression, replenishment and future-depth distributions. | Aggregate effects, not identities. |
| `P3 Cross Market` | Sparse response neighbours, event studies, lead/lag candidates and conditional responses. | Predictive association; no unsupported causal claim. |
| `P4 Participant Signatures` | Optional pseudonymous address/cluster behaviour features. | Requires incremental stable OOS lift; no identity inference. |
| `P5 Interactive Research` | Queue-Reactive, Hawkes, synthetic order flow and ABIDES-like agents. | Laboratory/stress scenarios, not initial production truth. |

The source order is P0, P1, P2, P3, P4, P5. The architecture exposes compatible interfaces early, but activation is progressive. P0 data collection precedes P1 calibration. P1 precedes P2 response, maker fill/adverse selection, P3, P4 and finally P5 research. Initial production must not depend on P4/P5.

## Initial Champion and promotion rule

The source names an empirical/simple/interpretable/fast survival model as the initial Champion direction. In practice it is stratified empirical survival, with a naive constant-survival baseline retained for validation. A discrete-hazard model is production-capable but learned. GBDT, deep survival, Queue-Reactive and Hawkes are challengers of increasing complexity.

A challenger earns promotion only with all of:

- temporal out-of-sample statistical improvement;
- improved or non-degraded probability calibration;
- positive EconomicLift and ModelValue after added latency/operational cost;
- acceptable runtime, stability, OOD and fallback behaviour;
- versioned artifact, features and validation evidence;
- explicit approval through the later validation/governance process.

An architecture-level target may be `LOCKED` while estimator choice, coefficients, horizons and thresholds remain `LEARNED`, `CALIBRATED`, `RESEARCH` or `FUTURE`.

## Relation to Simulator fidelity

P0–P5 describes participant-model capability. Simulator F0–F4 describes counterfactual simulation fidelity. They are independent axes and must be recorded separately. P5 does not make a simulator truthful; explicit agents remain scenarios unless calibrated and validated as forecast inputs.

## Sources

SRC-007 lines 328–420, 4716–4800 and 5300–5380; SRC-008 lines 1–34 and 1785–1821; SRC-005 model-safety requirements; SRC-006 validation gates.
