# Command, Event and Effect Audit

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Requested operation | Command/intent owner | Effect boundary | Authoritative return event | Commit owner | Result |
|---|---|---|---|---|---|
| feed subscribe/resync | Adapter/Feed control | WS/API | payload, connection or gap observation | Normalizer then owning reducer | PASS |
| graph rebuild | Graph owner | bounded worker if used | version-tagged build result | Graph/Route writer | PASS |
| forecast inference | Model owner | bounded compute | forecast/OOD result | forecast snapshot owner | PASS |
| simulate candidate | Simulator | bounded scenario compute | `ExecutionForecast` | Simulator store only | PASS |
| size/allocate | Sizer/Allocator | bounded optimization | proposal | decision evidence; no Risk mutation | PASS |
| assess/revalidate | Risk | none | `RiskDecision`/kill event | Risk writer | PASS |
| reserve/release | Reservation Engine | atomic internal effect | Reservation event | Reservation writer | PASS |
| submit order | Execution creates `OrderIntent` | signed transport | ACK/reject/status/fill/timeout observation | Execution/Account reducers | PASS |
| cancel order | Execution | transport cancel | canceled/rejected/racing fill | OrderState writer | PASS |
| query/reconcile | Reconciliation | ordered external queries | order→fill→balance observations | Reconciliation then domain writers | PASS |
| Recovery replan | Recovery proposes | Risk then new Execution plan/effect | fills/failures/state | Recovery + Execution in ordered commits | PASS |
| persist/record | Reducer/producer requests | Recorder/storage | quality/backpressure/durability result | Recorder writer | PASS |
| Replay run | Replay Engine | historical source + simulated transport | same typed events | isolated same reducers | PASS |
| promote model/capability | Validation/manager | artifact verify/publish | promotion/demotion event | manager writer | PASS |
| deploy/update/rollback | Deployment | process/artifact lifecycle | lifecycle/readiness observations | Deployment/Engine/Reconciliation owners | PASS |
| license refresh | License boundary | cold network call | signed license state | License state owner | PASS |

`SubmitOrder != OrderAccepted != Fill`; `CancelRequested != Canceled`; timeout after possible transmission becomes `UNKNOWN`. No transport callback, adapter, Recorder, model or operator command mutates economic truth directly.
