# 07 — Cross-Market and Multi-Market Branches

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## Mechanical locality

Every market owns a separate baseline, `Shadow Book`, `Δour`, and `Δresponse`. If Leg 1 trades `A/X`, only `A/X` is mechanically mutated. The books for `X/B` and `B/A` are not mechanically changed by conservation or triangle membership. Their later change is historical or a sampled Cross-Market Response.

## Sparse response propagation

For a shock in source market `i`, PASS 02 provides QF-081-like response distributions for supported targets `j` and horizons `h`. The logical `pair_to_response_neighborhood` is sparse and economically linked; an unlisted/unsupported neighbour means unknown or omitted by declared fidelity, not proven zero. PASS 08 owns graph construction.

Each branch records source shock, target market, horizon, direction/magnitude distribution, response delay, confidence, OOD, model version, and common-state lineage. Mechanical consumption is never counted again as local response.

## Route and leg evolution

At each leg arrival, the Simulator recomputes its book, fees/precision, remaining edge, survival, completion/recovery alternatives, and confidence. QF-082 measures correction of route edge. `Dominant Decay Leg` is consumed when supplied as evidence about where correction occurs; it does not justify causal attribution by itself.

Multi-market response can represent repricing, cancellation, replenishment, following aggressive flow, and arbitrage correction. All are scenario distributions conditioned on state/regime, never fixed deterministic propagation.

## Dependence and uncertainty

Shared factors and linked responses should be sampled jointly only when calibrated evidence supports the dependence. Otherwise the run declares its approximation. Clock skew, stale neighbour state, unsupported horizon, graph drift, and regime shift degrade `SimulationConfidence`.

## Validation

Use clock-aligned event studies, temporal OOS tests, sparse-neighbour stability, common-factor controls, with/without cross-market ablation, distribution coverage, and Micro-live response after real interventions. An F1 mechanical result may be valid without cross-market response; an F3 claim is not.
