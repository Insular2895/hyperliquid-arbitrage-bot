# State Ownership Matrix

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Canonical state | Logical writer | Readers | Version/snapshot | Persistence | Replay reconstruction |
|---|---|---|---|---|---|
| `BookState` | Book Engine reducer | Graph, Features, Opportunity, Simulator, Risk, Execution | BookVersion/immutable BookSnapshot | RAW + compatible checkpoint | Market events through same reducer |
| `MetadataState` | Metadata Engine | Graph, Formula, Precision, Execution, Replay | MetadataVersion | point-in-time metadata + RAW | metadata events at replay cutoff |
| `FeeState` | Fee Engine | Formula, Opportunity, Risk, Accounting | FeeVersion | point-in-time rules | fee events/artifact available at T |
| `PrecisionState` | Precision Engine | Formula, Sizer, Execution, Recovery | Precision/Metadata version | point-in-time rules | rule events at T |
| `GraphState` | Global Market Graph | Routes, Watcher, Atlas, Capital, Recovery | GraphVersion | topology artifact/checkpoint | metadata events + deterministic build |
| Route/index state | Route Engine/Graph commit | Opportunity, Execution, Replay | RouteDefinitionVersion | versioned definitions | deterministic from GraphState |
| `MarketAtlasState` | Atlas reducer/aggregator | HWC, Capital, Risk, research | AtlasVersion immutable snapshot | derived point-in-time store | recompute from eligible evidence/artifact at T |
| `FeatureState` | Feature Engine reducer | Opportunity, Participants, Simulator, Risk | FeatureVersion/Snapshot | L3 derived records | deterministic ordered events/formula versions |
| `AccountState` | Account reducer under Reconciliation/Coordinator | Inventory, Reservations, Risk, Execution | AccountVersion/Snapshot | P0 journal/checkpoint | account events then exchange reconciliation |
| `InventoryState` | Inventory reducer | Capital, Sizer, Portfolio, Risk, Execution, Accounting | InventoryVersion | fill ledger/journal/checkpoint | unique fills + balances/reservations |
| `ReservationState` | Reservation Engine | Capital, Risk, Execution, Reconciliation | ReservationVersion | execution journal/checkpoint | plan/reserve/release/UNKNOWN events |
| Risk state / `RiskSnapshot` | Risk Engine | Sizer, Allocator, Execution, Recovery, Operations | RiskSnapshot/config/TTL versions | decisions/config/evidence | same inputs and decision reducer |
| `ExecutionState` | Execution Coordinator | Risk, Recovery, Reconciliation, Accounting, Ops | separate Engine/Route/Order versions | execution journal/checkpoint | intents + observed order/fill events |
| `RecoveryState` | Recovery Engine reducer | Execution, Risk, Ops, Accounting | RecoveryVersion | journal | actual exposure + recovery events |
| `ReconciliationState` | Reconciliation Engine reducer | Engine readiness, Risk, Inventory, Ops | ReconciliationVersion | journal/report | orders→fills→balances observations |
| Capability state | Capability Manager | Risk, Execution, Deployment, Operations | signed `CapabilityManifest` | immutable manifest/evidence | load exact historical manifest |
| `RecorderState` | Recorder coordinator | Operations, Validation | recorder seq/chunk/quality versions | recorder metadata/chunks | reconstructed from recorder control records |
| Model artifact state | Model Artifact Manager | Participants, Simulator, Risk, Replay | ModelArtifactId/manifest | immutable artifact registry/local cache | exact point-in-time artifact from RunManifest |
| Infrastructure health state | Infrastructure Monitor | Risk, Execution, Operations, Validation | InfraInstanceId + observation/policy version | metrics/incident evidence | recorded health events or declared counterfactual |

Unowned canonical state: **0**. Duplicate logical ownership: **0**. Components may hold immutable read caches but cannot treat them as independently mutable truth.
