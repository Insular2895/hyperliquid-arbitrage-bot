# Cross-domain Invariant Catalog

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Invariant | Status | Primary owner | Violation response |
|---|---|---|---|
| No stale/invalid Book for new risk | LOCKED | Book + Risk | disable affected market/routes; resync |
| No unknown fees, precision or minimum rules | LOCKED | Fee/Precision + Risk | reject affected economics/order |
| No double spending of balance/book/Risk capacity | LOCKED | Reservation | atomic claim; contain invariant breach |
| Reserve before order effect | LOCKED | Reservation + Execution | no submit without current reservation |
| No blind retry after possible transmission | LOCKED | Execution/Reconciliation | UNKNOWN + stable CLOID query/reconcile |
| Actual unique fills only alter economic state | LOCKED | Account/Inventory | reject planned/duplicate fill mutation |
| Cancel requested is not cancel confirmed | LOCKED | OrderState | retain order/resource exposure until observed terminal event |
| SENT may have executed | LOCKED | Execution | UNKNOWN semantics; never assume no fill |
| UNKNOWN locks reservations | LOCKED | Execution/Reservation | block affected capacity until reconciliation |
| Reconcile before new risk when truth is uncertain | LOCKED | Reconciliation/Risk | non-ready/recovery-only |
| Recovery remains available where safely possible | LOCKED | Risk/Execution | license/config failure cannot remove risk reduction |
| No hard-Risk bypass by EV, optimizer or config | CONSTITUTIONAL | Risk | remove action from `A_safe` |
| No lookahead | LOCKED | Data/Replay/Validation | invalidate trace/report/capability evidence |
| Same Core contracts across RunModes | LOCKED | Data/Execution/Validation | reject divergent mode shortcut |
| No synchronous hot-path disk/database/control service | LOCKED | Architecture/Infra | isolate async or reject topology |
| No silent model/formula/config/capability version change | LOCKED | Data/Model/Capability | create new version; revalidate plan/scope |
| More capital does not increase `Q_validated` | LOCKED | Validation/Risk/Capital | q remains bounded by evidence intersection |
| Strategy ≠ Bridge ≠ Rebalance ≠ Recovery | LOCKED | Inventory/Accounting/Execution | classify separately; reject alpha mixing |
| Position Sizing ≠ Order Slicing | LOCKED | Capital/Execution | fixed total q before mechanical decomposition |
| Graph ≠ Atlas ≠ HWC | LOCKED | Graph/Atlas | topology, evidence and compute policy remain separate |
| Implemented ≠ configured ≠ validated | LOCKED | Validation | capability intersection fails closed |
| Licensed ≠ validated or Risk-permitted | LOCKED | Deployment/Validation/Risk | license only narrows commercial scope |
| Container running ≠ READY | LOCKED | Deployment/Execution | sync/reconcile/readiness checks required |
| Software rollback ≠ exchange rollback | LOCKED | Deployment/Reconciliation | current exchange truth wins |
| No dual active economic owner | LOCKED | Deployment/Execution | fence/halt/reconcile account context |
| No private competing mutable economic truth | LOCKED | Architecture/Data | consume owner snapshot; remove duplicate writer |
| Higher profit cannot outrank state/exposure safety | CONSTITUTIONAL | Risk | apply master priority order |

Exact domain semantics are owned by the linked masters. Calibrated thresholds do not weaken these directions.
