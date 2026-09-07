# Final System Scope

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Capability | Scope class | Earliest phase / maturity | Initially capital-bearing? | Key dependencies / gate |
|---|---|---|---:|---|
| Strong domain types, units, IDs, versions, Clock/RNG/RunManifest | A — foundation | Phase 1 / M1 | No | approved reviewed baseline |
| Hyperliquid adapters and immutable RAW Recorder | A — foundation | Phases 2–3 / M1 | No | current wire semantics; recorder integrity |
| Book, metadata, fees, precision, Graph/routes, Formula Core | A — foundation | Phases 4–7 / M1 | No | coherent feed; current rules; golden parity |
| Deterministic Replay and opportunity episodes | A — foundation | Phases 8–9 / M2 | No | same Core; no lookahead |
| Account, Inventory, Reservations, Risk, ESM, Recovery/Reconciliation | A — foundation | Phases 10–14 / M2 | No | actual-fill truth; conservative failure handling |
| OWA TT and direct conversion comparator | B — first strategy | Shadow 19; Micro-live 20; M5 later | Probe only at M4 | valid comparator; full critical chain; human authorization |
| Triangle TTT | B — first strategies, separately gated | after TT, stages 12 / scoped M4–M5 | Separate probe | three-leg tail/intermediate exposure/Recovery proof |
| Quant features, Atlas, Sizing, F0/F1 Simulator | A/B support | Phases 15–18 / M2 | No | point-in-time evidence and support |
| Collective Participant/Survival Champion | C — later V1 | Phase 21 / M2–M3 | No direct grant | temporal OOS, calibration, OOD and EconomicLift |
| F2 queue / F3 response Simulator | C — later V1 | Phase 22 / M2–M3 | No direct grant | supported data and calibration |
| MT / MTT | C — later V1 | Phase 23 / scoped M4–M5 | Separate probes | actual maker fill/time/adverse/cancel/recovery evidence |
| Portfolio allocation | C — later V1 | Phase 24 | Bounded only after promotion | single-candidate validity; shared constraints; lift vs simple baseline |
| Bridge / Capital Relocation | C — later V1 | Phase 25 | Separate probe/promotion | `STAY`, terminal, exit, relocation and persistence evidence |
| F4 interactive world, explicit agents, deep Hawkes/Queue-Reactive | D — Research | Research only | No | primary provenance and local OOS evidence |
| Cross-exchange, transfer edges, perp hedge | E — Future | no V1 phase | No | new venue/settlement/Risk/Data/Ops specification |
| Private node, hot standby/HA, high-end infrastructure | E — Future/evidence-gated | Phase 26 candidate | No direct grant | current capability facts and robust incremental economics |
| TM/MM | E — Future/type-supported | no initial activation | No | separate product decision and evidence program |

Scope semantics are strict: implemented ≠ validated; licensed ≠ validated; running ≠ ready. A capability is active only at the intersection of declared scope, dependency maturity, evidence, operations readiness, `CapabilityManifest`, Risk and capital authorization.
