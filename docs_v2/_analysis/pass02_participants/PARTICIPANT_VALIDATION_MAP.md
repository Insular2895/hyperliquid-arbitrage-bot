# PASS 02 — Participant Validation Map

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 02 REVIEW COMPLETE`

No numerical threshold below is invented. “Positive” and “acceptable” require a later versioned validation decision with uncertainty.

| Capability | Required data | Baseline | Statistical metric | Economic metric | Temporal/OOD/fallback | Ablation / micro-live | Maturity / activation | Authority |
|---|---|---|---|---|---|---|---|---|
| Edge Survival | Point-in-time OpportunityEpisodes, full edge paths, censoring, books/features, latency | Naive constant survival; stratified empirical | QF-094 observed survival, QF-095 Brier, QF-096 Log Loss, integrated Brier, calibration/concordance | QF-100 EconomicLift; QF-101 ModelValue | Walk-forward by horizon/route/size/regime; censored data; unsupported horizon/size OOD; empirical/reject fallback | Ablate features/model; predicted-vs-actual in shadow and micro-live | M2 replay, M3 observe; production use only after calibrated OOS gain | SRC-004/005/006 |
| Liquidity Response | Shock-labelled books/trades, mechanical delta separated, future depth/spread/add/cancel paths | No-response / simple empirical buckets | Distribution calibration, coverage, depth/spread/replenishment error and tails | EconomicLift/ModelValue through Simulator | Temporal by market/side/size/regime/fidelity; negative-depth/double-impact tests; conservative capacity/reject | Ablate OFI, shock, vol, cross-market; simulated-vs-live response | F3 only after calibrated distributions; no initial dependency | SRC-005/006/007/008 |
| Cross-Market | Clock-aligned source shocks and neighbour outcomes, point-in-time graph/state | No validated response; sparse empirical event study | Target/horizon calibration/error, neighbourhood stability | EconomicLift/ModelValue | Later-time/new-regime/asset; common-factor and clock-skew tests; omit/reject unsupported neighbours | Mandatory with/without cross-market ablation; micro-live before scaling | OOS predictive improvement >0 and safe runtime/OOD before production | SRC-004 QF-081/082; SRC-006 |
| Maker Fill | Own order/book state, queue-fidelity label, fills/partials/cancels, time-to-fill | Empirical fill by support bucket | QF-099 fill calibration, survival/CDF coherence, timing/quantity error | MT EconomicLift/ModelValue after recovery | Temporal by side/market/size/regime/feed; queue visibility OOD; conservative/reject fallback | Ablate queue/OFI features; shadow then micro-live fills | Required calibration before dependent maker strategy activation | SRC-004/005/006 |
| Adverse Selection | Maker fills and later mids at supported horizons, side, state, second-leg/recovery | Zero/simple empirical adverse cost (comparison only, never optimistic fallback) | Signed QF-054/055 error/calibration by horizon and slice | Net maker/MT lift incl. recovery and tails | Temporal/OOD for unsupported horizons/state; conservative adverse buffer/reject | With/without adverse model; live post-fill comparison | Must be calibrated with fill and recovery before MT activation | SRC-004/005/006 |
| Address Behaviour | Revalidated passive counterparty fields, trades, opportunity events, privacy-safe lineage | Aggregate model without address features | Incremental Brier/LogLoss/calibration, cluster stability | Incremental EconomicLift/ModelValue | Later-window/new-address/sparse support; missing fields fallback to aggregate | Mandatory address-feature ablation; shadow first; micro-live only if justified | P4 Research/Future; no initial production dependency | SRC-007; EXT-005 |
| Advanced Challenger | Same point-in-time data as Champion plus event-level data where required | Current approved simple Champion | Calibration/statistical improvement, robustness and runtime | EconomicLift and ModelValue robustly positive | Temporal regime stress, OOD, corruption/NaN/drift and rollback | Same-feature Champion/Challenger, component ablation; micro-live if decision-affecting | GBDT/Deep/Queue-Reactive/Hawkes require evidence; agents remain P5 stress | SRC-005/006/007/008 |

## Common validation invariants

1. Random row split is not accepted.
2. Training, validation and test periods are ordered; walk-forward measures decay.
3. Feature and graph construction are point-in-time and schema-versioned.
4. Probability calibration is evaluated by horizon and support slice, not aggregate only.
5. Statistical improvement alone is insufficient.
6. Same dataset, capital, fees and risk budget are used for EconomicLift comparison.
7. Added inference latency and operations enter ModelValue.
8. OOD, stale/schema mismatch, model corruption, disagreement, drift and fallback are tested explicitly.
9. Production weight changes require offline validation, artifact approval and rollback/fallback.
