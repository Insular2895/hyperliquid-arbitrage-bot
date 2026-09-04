# 02 — Engine and Route execution state machines

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## `EngineState` inventory

| State | Meaning / entry action | Exit evidence | Prohibited |
|---|---|---|---|
| `BOOTING` | initialize services, load checkpoint/config, no risk | local bootstrap completes | orders/new risk |
| `SYNCING` | connect feeds; fetch metadata/account/order/fill/time state | required sources current enough to compare | new risk |
| `RECONCILING` | start canonical reconciliation | `CONSISTENT` or escalation | new risk; assumption-based release |
| `READY` | reconciled and health/Risk gates permit execution | health loss, recovery need, halt/shutdown | bypassing gates |
| `DEGRADED` | bounded impaired state | health restored + reconcile, or escalation | silent full capability |
| `RECOVERY_ONLY` | existing risk reduction only | exposures resolved + reconcile, or halt | new opportunities |
| `HALTED` | automated risk-taking stopped | explicit authorized restart/shutdown | risk-increasing effects |
| `SHUTTING_DOWN` | stop admission; cancel/settle/persist by policy | safe shutdown conditions | new risk |
| `STOPPED` | process execution terminal | new process boot only | all exchange effects |

### Engine transitions

| From | Event/guard | Action | To |
|---|---|---|---|
| `BOOTING` | bootstrap succeeds | begin feeds/account sync | `SYNCING` |
| `BOOTING` | critical bootstrap fails | record reason; forbid risk | `HALTED` |
| `SYNCING` | required snapshots/streams available | request comparison | `RECONCILING` |
| `SYNCING` | bounded dependency impaired | retain no/limited risk | `DEGRADED` |
| `RECONCILING` | reconciliation `CONSISTENT`; all health/Risk gates pass | publish current snapshots | `READY` |
| `RECONCILING` | exposure needs reduction | prioritize safety | `RECOVERY_ONLY` |
| `RECONCILING` | unresolved critical inconsistency | persist evidence/escalate | `HALTED` |
| `READY` | market/account/clock/infra becomes unsafe | disable new risk; cancel resting orders as policy | `DEGRADED` or `RECOVERY_ONLY` |
| `READY` | route enters recovery | prioritize exposure | `RECOVERY_ONLY` when global policy requires |
| `DEGRADED` | health restored | resync/reconcile before admission | `SYNCING` or `RECONCILING` |
| `DEGRADED` | critical failure/unresolved mismatch | stop risk | `HALTED` |
| `RECOVERY_ONLY` | recovery resolved | request full reconciliation | `RECONCILING` |
| `RECOVERY_ONLY` | recovery failed beyond policy | manual/hard-halt escalation | `HALTED` |
| any active | authorized shutdown | stop admission and perform safe close | `SHUTTING_DOWN` |
| `SHUTTING_DOWN` | safety/persistence criteria complete | stop effects | `STOPPED` |

No direct startup-to-`READY`, timeout-to-`READY`, or `UNKNOWN`-to-`READY` transition exists.

## `RouteExecutionState` inventory

| State | Entry work | Exit condition | Reservation/exposure meaning |
|---|---|---|---|
| `DETECTED` | correlate opportunity and current state | validation starts | none yet |
| `VALIDATING` | quantize, simulate, Risk/current-state checks | allow or known reject | no new order |
| `RESERVING` | atomically reserve balances/book/Risk | complete set or fail | capacity locked if success |
| `PLANNED` | freeze immutable `ExecutionPlan` | current pre-send validation | reservations locked |
| `EXECUTING` | create intents and reduce order/fill events | completion/recovery/ambiguity | actual fills become exposure |
| `COMPLETED` | finalize route actuals | terminal | only policy-permitted dust remains |
| `ABORTED` | known safe stop | terminal after release/reconcile | no unresolved exposure |
| `RECOVERY_REQUIRED` | stop same-capital new risk; start Recovery | recovery plan starts | actual exposure exists/may exist |
| `RECONCILING` | resolve ambiguous route/order/account state | consistent continuation/terminal or failure | reservations stay conservative |
| `FAILED_SAFE` | no safe automatic continuation; evidence retained | manual/new execution lifecycle | new risk blocked for affected scope |

### Route transitions

| From | Event/guard | Action | To |
|---|---|---|---|
| `DETECTED` | candidate accepted for current check | create validation context | `VALIDATING` |
| `VALIDATING` | current validation/Risk rejects; exposure zero | record structured reject | `ABORTED` |
| `VALIDATING` | all current gates pass | request three reservation classes | `RESERVING` |
| `RESERVING` | any reservation fails atomically | release acquired remainder; record reason | `ABORTED` |
| `RESERVING` | complete/versioned reservations held | materialize immutable plan | `PLANNED` |
| `PLANNED` | pre-send validity envelope still holds | create first intent | `EXECUTING` |
| `PLANNED` | state invalidates plan before possible send | release after proof; replan/new version or stop | `ABORTED` |
| `EXECUTING` | first IOC zero fill and terminal-known | no later leg; reconcile releases | `ABORTED` |
| `EXECUTING` | leg actual fill; continuation still best and permitted | resize/revalidate next leg | `EXECUTING` |
| `EXECUTING` | full route closure conditions hold | compute actuals; release remainder | `COMPLETED` |
| `EXECUTING` | partial/later failure/edge death leaves exposure | snapshot actual exposure | `RECOVERY_REQUIRED` |
| `EXECUTING` | send/order truth ambiguous | lock reservations; query truth | `RECONCILING` |
| `RECOVERY_REQUIRED` | Recovery machine starts | transfer current exposure context | `EXECUTING` remains suspended while Recovery owns action |
| `RECOVERY_REQUIRED` | truth itself ambiguous | query before unsafe recovery | `RECONCILING` |
| `RECONCILING` | truth consistent and original execution still valid | resume at proven state | `EXECUTING` |
| `RECONCILING` | truth consistent, zero exposure/known abort | release proven remainder | `ABORTED` |
| `RECONCILING` | truth consistent, exposure needs reduction | start/restart Recovery from actual state | `RECOVERY_REQUIRED` |
| `RECONCILING` | cannot resolve within policy | retain locks and escalate | `FAILED_SAFE` |
| `RECOVERY_REQUIRED` | Recovery `RECOVERED`, all route closure criteria pass | reconcile final actuals | `COMPLETED` |
| `RECOVERY_REQUIRED` | Recovery `RECOVERY_FAILED` | keep evidence/locks as required; escalate | `FAILED_SAFE` |

`ABORTED` means a known safe non-completion, not a synonym for network error. `FAILED_SAFE` is a fail-conservative route outcome, not proof of zero exposure.
