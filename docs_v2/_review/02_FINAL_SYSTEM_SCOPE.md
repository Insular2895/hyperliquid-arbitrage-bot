# Final System Scope

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

Review 02 uses the single canonical `ScopeClass` taxonomy from Review 17: `FOUNDATION`, `LATER_V1`, `RESEARCH`, `FUTURE`, `REJECTED`. Product or activation distinctions belong to `Program role`; they are not alternative scope classes.

| Capability | Scope class | Program role | Earliest technical phase / evidence maturity | Initially capital-bearing? | Key dependencies / gate |
|---|---|---|---|---:|---|
| Strong domain types, units, IDs, versions, Clock/RNG/RunManifest | FOUNDATION | final-capable domain foundation | Technical Phase 1 / M1 | No | approved reviewed baseline |
| Hyperliquid adapters and immutable RAW Recorder | FOUNDATION | source-truth foundation | Technical Phases 2–3 / M1 | No | current wire semantics; recorder integrity |
| Book, metadata, fees, precision, Graph/routes, Formula Core | FOUNDATION | deterministic market/economic foundation | Technical Phases 4–7 / M1 | No | coherent feed; current rules; golden parity |
| Deterministic Replay and opportunity episodes | FOUNDATION | evidence and first-strategy support | Technical Phases 8–9 / M2 | No | same Core; no lookahead |
| Account, Inventory, Reservations, Risk, ESM, Recovery/Reconciliation | FOUNDATION | safety/execution foundation | Technical Phases 10–14 / M2 | No | actual-fill truth; conservative failure handling |
| fixed OWA TT hypothesis, fair comparator and first candidate baseline | FOUNDATION | first measurable/reconcilable strategy baseline | Technical Phases 5–20 as dependencies mature / M0, M1, M2, M3, then separately M4; M5 later | Probe only at separately authorized M4 | Falsifier/finite Sweep may support DRAFT; Replay, Shadow, Micro-live and capital gates remain separate |
| Economic Falsifier, narrow Bounded Sweep and Robustness Map | FOUNDATION | scientific validation method/contract | consumes Phases 5–18 as applicable; no new phase/stage | None | frozen finite protocol, canonical truth, temporal OOS, T2-before-holdout, non-authorizing disposition |
| Triangle TTT | LATER_V1 | first separately gated three-leg taker strategy | after TT; Evidence Stage 13 / scoped M4–M5 | Separate probe | three-leg tail/intermediate exposure/Recovery proof |
| Quant features, Atlas, Sizing, F0/F1 Simulator | FOUNDATION | evidence/model foundation support | Technical Phases 15–18 / M2 | No | point-in-time evidence and support |
| Collective Participant/Survival Champion | LATER_V1 | later model enrichment | Technical Phase 21 / M2–M3 | No direct grant | temporal OOS, calibration, OOD and EconomicLift |
| F2 queue / F3 response Simulator | LATER_V1 | later simulator fidelity | Technical Phase 22 / M2–M3 | No direct grant | supported data and calibration |
| MT / MTT | LATER_V1 | bounded maker-mode paths | Technical Phase 23 / scoped M4–M5 | Separate probes | actual maker fill/time/adverse/cancel/recovery evidence |
| Portfolio allocation | LATER_V1 | later shared-resource allocation | Technical Phase 24 | Bounded only after promotion | single-candidate validity; shared constraints; lift vs simple baseline |
| Bridge / Capital Relocation | LATER_V1 | later capital relocation | Technical Phase 25 | Separate probe/promotion | `STAY`, terminal, exit, relocation and persistence evidence |
| F4 interactive world, explicit agents, deep Hawkes/Queue-Reactive | RESEARCH | isolated advanced-model research | Research only | No | primary provenance and local OOS evidence |
| Cross-exchange, transfer edges, perp hedge | FUTURE | separate future product | no V1 phase | No | new venue/settlement/Risk/Data/Ops specification |
| Private node / higher-fidelity feed challenger | RESEARCH | observe-only infrastructure challenger | isolated observation/benchmark only | No direct grant | current capability facts and robust incremental economics; public feed remains independent |
| Hot standby/HA | FUTURE | separate future availability architecture | no V1 activation | No | separate fencing/failover architecture and evidence |
| Gossip/read and IOC/ALO priority optimization | RESEARCH | evidence-gated mechanism research | research after baseline gate | No automatic grant | current facts, typed policy, matched outcomes, cost-once, Risk/Validation approval |
| Reusable InfraProfile laboratory | RESEARCH | offline/observe-only infrastructure evidence | Recorder/Replay/Shadow evidence support | No | simultaneous calibration, freshness, provenance and counterfactual labels |
| TM/MM | FUTURE | separate future execution product | no current activation | No | separate product, safety, execution, Risk, evidence and authorization program |

Scope semantics are strict: implemented ≠ validated; licensed ≠ validated; running ≠ ready. A capability is active only at the intersection of declared scope, dependency maturity, evidence, operations readiness, `CapabilityManifest`, Risk and capital authorization.
