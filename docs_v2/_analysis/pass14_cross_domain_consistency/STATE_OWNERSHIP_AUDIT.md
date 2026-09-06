# State Ownership Audit

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Canonical mutable state | Single logical writer | Principal readers | Persistence/reconstruction | Duplicate owner? |
|---|---|---|---|---|
| `BookState` | Book reducer | Graph, Formula, Simulator, Risk, Execution | ordered market events + compatible checkpoint | NO |
| `MetadataState` | Metadata reducer | Graph, Precision, Formula, Execution | point-in-time metadata events | NO |
| `FeeState` | Fee reducer | Formula, Risk, Accounting | effective-time fee events/artifact | NO |
| `PrecisionState` | Precision/Metadata reducer | Formula, Sizer, Execution | point-in-time rules | NO |
| `GraphState` / routes | Graph/Route commit owner | Opportunity, Atlas, Capital, Replay | deterministic metadata build | NO |
| `MarketAtlasState` | Atlas aggregator | HWC, Capital, Risk, research | eligible point-in-time evidence | NO |
| `FeatureState` | Feature reducer | Participants, Simulator, Risk | ordered state + FormulaVersion | NO |
| `AccountState` | Account reducer under coordinator | Inventory, Reservation, Risk, Execution | account events + exchange reconciliation | NO |
| `InventoryState` | Inventory reducer | Capital, Sizer, Portfolio, Risk, Accounting | unique fills + balance/reconciliation evidence | NO |
| `ReservationState` | Reservation Engine | Risk, Capital, Execution, Reconciliation | plan/reserve/use/release/unknown events | NO |
| Risk state / `RiskSnapshot` | Risk Engine | Sizer, Execution, Recovery, Operations | decision/config evidence | NO |
| `ExecutionState` | Execution Coordinator | Risk, Recovery, Accounting, Operations | intent/order/fill journal | NO |
| `RecoveryState` | Recovery reducer | Risk, Execution, Accounting, Operations | actual exposure + recovery events | NO |
| `ReconciliationState` | Reconciliation reducer | readiness, Risk, Inventory, Operations | orders→fills→balances evidence | NO |
| capability state | Capability Manager | Deployment, Risk, Execution, Operations | signed immutable manifest/evidence | NO |
| `RecorderState` | Recorder coordinator | Operations, Validation | recorder control records/chunks | NO |
| model artifact state | Model Artifact Manager | Participants, Simulator, Risk, Replay | immutable artifacts | NO |
| infrastructure health state | Infrastructure Monitor | Risk, Execution, Operations | recorded health events | NO |
| accounting records | Accounting logical writer | Operations, Validation, research | unique fills + classified events/valuation | NO |

Coordinator commit authority is not duplicate domain ownership: it serializes owner-produced transitions. Read caches and persistence are not mutable truth. Unowned states: **0**. Duplicate logical owners: **0**. Position Sizing is an Inventory/Capital proposal owner, not a second Risk state owner.
