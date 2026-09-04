# PASS 02 — Participant Legacy Comparison

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 02 REVIEW COMPLETE`

Comparison was performed only after the V2 master/deep specs were drafted. Legacy remained reference-only and never overrode original sources.

## Files reviewed

- `docs/06_MARKET_PARTICIPANTS.md`
- `docs/05_MARKET_MICROSTRUCTURE.md`
- `docs/07_COUNTERFACTUAL_SIMULATOR.md`
- `docs/09_RISK_CONSTITUTION.md`
- `docs/16_VALIDATION_MATRIX.md`
- relevant `docs/specs/ParticipantEngine.md`, `EdgeSurvivalEngine.md`, `LiquidityResponseEngine.md`, `CrossMarketResponseEngine.md`, `OFIEngine.md`
- `docs/decisions/ADR-012-statistical-participants.md` and extracted participant notes.

## Disposition

| Legacy subject | Classification | PASS 02 result |
|---|---|---|
| Collective statistical response before agents | `RECOVERED` | Elevated to the master purpose/non-goals and P0–P5 deep spec. |
| OpportunityEpisode, censoring and selection-bias prevention | `OVER_COMPRESSED` | Full economic death, episode, non-opportunity and right-censor contract recovered. |
| Empirical/Discrete Hazard/GBDT progression | `OVER_COMPRESSED` | Statuses separated into baseline, production-capable learned model and Challenger. |
| P0–P5 ladder | `RECOVERED` | Exact P5 contents and independence from F0–F4 made explicit. |
| Survival/hazard/capture formulas | `OVER_COMPRESSED` | Exact QF-044..050/083/085 and `E[S(L)]` tail rationale recovered. |
| QI/OFI/MLOFI/microprice | `OVER_COMPRESSED` | Event-level formulas, snapshot proxy boundary, provenance and no-lookahead added. |
| Liquidity response/future depth | `OVER_COMPRESSED` | Mechanical separation, QF-043 raw/clamp semantics, cancellation and distribution targets added. |
| Maker model | `OVER_COMPRESSED` | QF-051..055, horizon conditioning, toxicity, MT reference and strategy activation recovered. |
| Sparse cross-market model | `OVER_COMPRESSED` | Event studies, causal caution, correction, dominant leg, score boundary and ablation added. |
| Address signatures | `OVER_COMPRESSED` | Passive features, ReactionDelay/FastCorrection, privacy and no deanonymization added. |
| OOD/disagreement/drift/fallback | `OVER_COMPRESSED` | QF-102/103, model kill, offline promotion and fault tests recovered. |
| Statistical/economic validation | `OVER_COMPRESSED` | QF-094..101, temporal walk-forward, same-budget comparison and ModelValue recovered. |
| Heavy Monte Carlo/runtime boundary | `MISSING` in participant master | Explicitly routed to Simulator and bounded participant inference. |
| Data forecast schemas | `ROUTED_TO_OTHER_PASS` | Semantic interfaces referenced; exact fields/types remain PASS 06. |
| Queue counterfactual mechanics | `ROUTED_TO_OTHER_PASS` | Kept out of PASS 02; PASS 03 owns detailed queue branches. |
| Risk thresholds and execution state transitions | `ROUTED_TO_OTHER_PASS` | Participant output can tighten/block only; Risk/Execution own decisions. |
| Legacy formula ranges `QF-044..058,081..104` | `SUPERSEDED` as a vague citation | Replaced with exact per-formula crosscheck and ownership boundaries. |

## Legacy omissions recovered

- economic opportunity death and entry/exit hysteresis boundary;
- full latency distribution and why `S(E[L]) != E[S(L)]`;
- expected arrival edge and probability above execution threshold;
- true OFI versus Snapshot OFI proxy;
- raw over-replenishment and future-depth uncertainty;
- side-correct adverse selection and expected-fill-time horizon convention;
- correlation versus causality, Dominant Decay Leg and monitoring-only competition score;
- exact P5: Queue-Reactive, Hawkes and ABIDES-like agents;
- no live self-modifying model and full artifact provenance;
- Brier, Log Loss, fill calibration, EconomicLift and ModelValue formulas;
- model disagreement, OOD, drift and strategy-scoped fail-safe behaviour;
- forecast freshness/schema/fidelity contract and all cross-domain consumers.

## Legacy-only untraced material

**0 imported.** No legacy-only claim was promoted without original-source support. The legacy `RunManifest declares both P/F levels` detail is compatible with source architecture and retained as a cross-domain contract proposal; exact schema remains Data/Simulator-owned.

## Contradicted/superseded legacy readings

No legacy file directly contradicted final source authority. Any reading that synthetic agents are production truth, L2 gives an exact queue, a dense cross-market matrix is desirable, or a more complex model is automatically better is explicitly superseded by SRC-007/008 and closure validation rules.
