# Event and Command Ownership Matrix

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Command/intent | Accepting owner | Requested effect | Authoritative return event | State owner that commits |
|---|---|---|---|---|
| Subscribe/refresh feed | Feed/Metadata Adapter | external WS/API subscription | payload/connection/gap observation | Normalizer then Book/Metadata reducers |
| `TimerCommand` | Ordered Coordinator/Clock | schedule logical deadline | `TimerEvent` | owning state machine reducer |
| Rebuild graph/routes | Graph/Route owner | none or worker computation | versioned build result | Graph/Route single writer after version check |
| Evaluate opportunity | Opportunity Engine | bounded worker computation | Opportunity/RejectEpisode | L4/Recorder; no economic-state mutation |
| Infer forecast | Participant owner | bounded inference | ModelForecast/OOD result | forecast/feature owner after version check |
| Simulate plan candidate | Simulator | bounded scenarios | `ExecutionForecast` | Simulator result store; no account mutation |
| Size/allocate | Sizer/Allocator | bounded optimization | size/allocation proposal | decision record; Risk remains permission owner |
| Assess/revalidate | Risk Engine | none | `RiskDecision`/kill event | Risk state writer |
| Reserve/release | Reservation Engine | atomic internal resource claim | Reservation event | Reservation state writer |
| Start/continue plan | Execution Coordinator | create `OrderIntent` | route/order transition | Execution state writer |
| Submit/query/cancel order | Effect Executor/Transport | signed exchange I/O | accepted/rejected/status/fill/timeout event | Execution/Account/Fill reducers in order |
| Cancel request | Execution Coordinator | cancel effect | cancel confirmed/rejected or racing fill | OrderState writer; reservation retained until terminal truth |
| Begin/replan Recovery | Recovery Engine | route search and later order effects via Execution | recovery transition/fill/failure | Recovery + Execution owners, ordered commits |
| Reconcile account | Reconciliation Engine | query orders→fills→balances | observed truth/mismatch/consistent event | Reconciliation then Account/Inventory/Execution owners |
| Record/rotate/archive | Recorder | disk/compression/archive I/O | recorder quality/backpressure result | Recorder state writer |
| Run Replay | Replay Engine | historical event source | Core events and `DecisionTrace` | same domain reducers in isolated Replay context |
| Promote/demote model | Model/Validation owner | artifact stage/verify | promotion/demotion decision | Model Artifact Manager |
| Promote/demote capability | Validation/Capability owner | sign/publish manifest | capability event | Capability Manager |
| Update/rollback/start/stop | Deployment owner | artifact/process lifecycle | deployment/readiness observations | Deployment + Engine/Reconciliation state owners |
| Refresh license | Licensing boundary | cold network request | signed license state | License state owner; Risk consumes scope |

An effect result always returns through the event boundary. No transport callback mutates economic state directly. `SubmitOrder != OrderAccepted != Fill`; `CancelRequested != Canceled`; timeout after possible transmission becomes `UNKNOWN`.
