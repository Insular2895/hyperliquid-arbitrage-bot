# Domain Interface Catalog

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Interface | Producer | Consumers | Required semantic boundary / versioning |
|---|---|---|---|
| `RawEvent` | Feed/account adapters + Recorder | Normalizer, Replay, audit | immutable payload, source/connection, timestamps, `recorder_seq`, schema |
| Normalized `MarketEvent` / `AccountEvent` / `EngineInputEvent` | Normalizer | ordered reducers | typed, raw lineage, receive order; invalid never mutates state |
| `BookSnapshot` | Book Engine | Graph/Routes, Features, Opportunity, Simulator, Risk | coherent BookVersion, freshness/gap validity |
| Metadata/Fee/Precision snapshots | owning engines | Graph, Formula, Sizer, Execution | point-in-time effective version; unknown fails closed |
| `RouteDefinition` / route dependency index | Graph/Route Engine | Opportunity, Execution, Replay | fixed ordered legs, dependencies, topology version |
| `RouteEconomics` | Route/Formula Core | Opportunity, Sizer, Risk, Accounting | exact size-dependent `NetConvert`, units/rule/formula versions |
| `FeatureSnapshot` | Feature Engine | Participants, Simulator, Risk, Atlas | event/state version, window/support/fidelity |
| `OpportunityEpisode` / RejectEpisode | Opportunity | Recorder, Participants, Simulator, Validation | economic birth/death/reason, censoring and point-in-time versions |
| `EdgeSurvivalForecast` | Participant Engine | Opportunity, Simulator, Risk, Sizer, Infra | horizon distribution, support, confidence/OOD, artifact version |
| `LiquidityForecast` / `CrossMarketForecast` / maker forecast | Participants | Simulator, Execution, Risk, Atlas | distribution; no mechanical-impact double count; scope/version |
| `ExecutionForecast` | Simulator | Sizer, Risk, Execution evidence | full/partial/recovery/failure distribution, fidelity, confidence, seed/model |
| `MarketAtlasSnapshot` | Atlas | HWC, Capital, Risk, research | market/route/asset/location/horizon evidence + AtlasVersion |
| `AccountSnapshot` | Account/Reconciliation reducer | Inventory, Reservation, Risk, Execution | observed orders/fills/balances consistency and AccountVersion |
| `InventoryState` | Inventory Engine | Terminal, Sizer, Portfolio, Risk, Accounting | actual-fill-derived exposure, class/bands/location/version |
| Reachability/Terminal result | Capital/Terminal engines | Sizer, Portfolio, Risk | available after reservations, exit/stranded/future state |
| Size curve / allocation proposal | Sizer/Allocator | Risk, Reservation, DecisionTrace | deterministic q candidates, `Q_validated`, shared constraints |
| `RiskSnapshot` / `RiskDecision` | Risk Engine | Reservation, Execution, Recovery, Data/Ops | structured action/reasons/limits/TTL and all dependency versions |
| `ReservationState` | Reservation Engine | Risk, Execution, Capital, Reconciliation | balance/book/risk claims, owner, lifecycle, UNKNOWN lock |
| `ExecutionPlan` | Decision/Execution boundary | Execution Coordinator, Replay, Recorder | immutable legs/protection/versions/authorization |
| `OrderIntent` / effect request | Execution Coordinator | Transport | stable CLOID, quantity/price/protection, plan/order versions |
| order/fill/cancel observations | Transport/adapters | ordered Execution/Account reducers | unique external identity, actual quantity/fee/status/provenance |
| FillLedger | Account/Execution reducer | Inventory, Recovery, Accounting, Replay | unique/idempotent actual fills only |
| Recovery plan/state | Recovery Engine | Risk, Execution, Accounting, Ops | current exposure, bounded actions, no route loyalty/sunk-cost widening |
| Reconciliation report/state | Reconciliation Engine | readiness, Risk, Inventory, Ops | orders→fills→balances proof, mismatch/consistency version |
| Accounting record | Accounting | Ops, Validation, research | disjoint action/PnL classification, actual units/fees |
| `RunManifest` | Data/Replay/Deployment | Replay, Validation, research | build/config/models/formulas/schemas/mode/dataset/seed identities |
| `DecisionTrace` | ordered Core | Replay, Validation, incidents | ordered decisions/intents/transitions/Risk decisions + hashes |
| `ModelArtifact` / manifest | Model Artifact Manager | Participants, Simulator, Risk, Replay | training range, features, support, metrics, fallback, approval |
| `CapabilityManifest` | Validation/Capability Manager | Deployment, Risk, Execution, Operations | exact market/mode/q/model/infra/version maturity scope |
| Infrastructure/health snapshot | Infrastructure/Ops | Risk, Execution, Validation | instance, clock/feed/resource validity, policy version |
| `EvidenceId` / ValidationReport / IncidentRecord | Validation/Ops | Capability, Release, operator | immutable evidence inputs, results, scope and provenance |

Exact serialized fields remain governed by Data schemas. PASS 13 fixes producers, consumers and semantics, not an alternate wire format.
