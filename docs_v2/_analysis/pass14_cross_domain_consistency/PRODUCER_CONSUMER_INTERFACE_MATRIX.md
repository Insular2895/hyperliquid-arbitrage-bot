# Producer–Consumer Interface Matrix

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Contract | Producer | Consumers | Cross-domain guarantee |
|---|---|---|---|
| Raw/normalized event | Adapter/Recorder/Normalizer | Core, Replay, audit | bytes/order/lineage retained; invalid cannot mutate |
| Book/rule snapshots | Book/Metadata/Fee/Precision | Formula, Graph, Risk, Execution | coherent versions, freshness and current rule identity |
| route definition/index | Graph/Route | Opportunity, Replay, Execution | ordered legs and all dependencies, comparator included |
| route economics | Formula/Route | Opportunity, Sizer, Risk, Accounting | size-dependent units and no cost duplication |
| feature snapshot | Feature Engine | Participants, Simulator, Risk, Atlas | point-in-time schema/support/fidelity |
| opportunity/reject episode | Opportunity | Recorder, Models, Simulator, Validation | candidate/reject/censoring and state versions |
| participant forecasts | Participants | Simulator, Risk, Execution, Atlas, Sizer | distributions, horizon, support/OOD and artifact identity |
| `ExecutionForecast` | Simulator | Sizer, Risk, Execution evidence | exclusive outcomes, tails, fidelity, confidence and seed |
| Atlas snapshot | Atlas | HWC, Capital, Risk, research | historical/learned context, never current book truth |
| account snapshot | Account/Reconciliation | Inventory, Reservation, Risk, Execution | orders/fills/balances consistency/version |
| inventory state | Inventory | Terminal, Sizer, Portfolio, Risk, Accounting | actual-fill-derived exposure/class/bands |
| terminal/reachability result | Capital/Terminal | Sizer, Portfolio, Risk | post-reservation, exit/stranded/future-state result |
| size/allocation proposal | Sizer/Allocator | Risk, Reservation, trace | deterministic feasible q candidates; not permission |
| `RiskDecision` | Risk | Reservation, Execution, Recovery, Ops | current scoped action, limits, reasons, expiry |
| reservation state | Reservation | Capital, Risk, Execution, Reconciliation | once-only claims and unknown lock |
| execution plan/intent | Execution | Signer/Transport, Replay, Recorder | immutable Risk-linked requested action |
| order/fill observations | Transport/Account adapter | ordered reducers | observed exchange evidence, unique identity |
| FillLedger | Account/Execution reducers | Inventory, Recovery, Accounting, Replay | idempotent actual fills only |
| Recovery state/plan | Recovery | Risk, Execution, Accounting, Ops | current exposure, bounded actions, no sunk-cost widening |
| reconciliation report | Reconciliation | readiness, Risk, Inventory, Ops | orders→fills→balances proof or explicit unresolved |
| accounting record | Accounting | Ops, Validation, research | disjoint action/PnL class, units, period and lineage |
| `RunManifest` / `DecisionTrace` | Data/ordered Core | Replay, Validation, Incident | reproducible resolved input and ordered outputs |
| ModelArtifact | Model Manager | Participants, Simulator, Risk, Replay | immutable hash, data/features/support/approval/fallback |
| Evidence/Validation report | domain producer + Validation | Capability, release, operator | immutable scoped claim and deviations |
| CapabilityManifest | Validation/Capability Manager | Deployment, Risk, Execution, Ops | exact promoted subset, not broad inference |
| Infrastructure health snapshot | Infrastructure | Risk, Execution, Validation, Ops | three-state health plus evidence/policy version |

Missing producers: **0**. Missing consumers for canonical runtime/evidence contracts: **0**. Orphan findings are detailed in `ORPHAN_AND_DEAD_CONTRACT_AUDIT.md`.
