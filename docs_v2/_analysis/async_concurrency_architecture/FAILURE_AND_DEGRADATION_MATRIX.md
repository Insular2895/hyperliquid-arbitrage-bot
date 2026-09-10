# Failure and Degradation Matrix

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

“Existing exposure” allows only current-policy cancel, Recovery, reconciliation and safe shutdown; it never authorizes new risk.

| Failure | Detection/evidence | New risk | Safe response | Canonical-state effect |
|---|---|---|---|---|
| worker panic | join/panic result, job identity, health counter | unaffected scope only if fallback valid; otherwise off | discard generation, fallback/restart bounded worker, alert | none directly |
| worker-request queue full | enqueue outcome/backlog | optional candidate rejected/fallback | inline/simple path, supersede eligible derived job | none |
| worker-result queue full | explicit handoff failure | no commit from lost proposal | retry bounded handoff or discard/fallback | none |
| worker timeout | deadline disposition | no stale authorization | fallback/shrink/reject | none |
| stale/late worker | version/deadline comparison | off for that proposal | discard/revalidate only if exact contract permits | none |
| I/O disconnect | connection event/timer | affected scope off | reconnect/resync/query/reconcile | ordered health/gap event |
| market feed gap | sequence/Book invariant | affected markets off | invalidate Book, resync, cancel/recover if safe | C0 invalidates state |
| account feed gap | connection/sequence/missing evidence | account new risk off | query orders→fills→balances, retain resources | C0 reconciliation/health |
| effect timeout | effect identity/timer | no blind retry | `UNKNOWN`, query/reconcile | ordered ESM transition |
| ACK delayed | send/ACK timers | no extra send | remain pending/UNKNOWN by policy; continue event loop | ordered evidence only |
| fill during cancel | FillId plus cancel events | no assumption of canceled | apply fill once, update exposure, revalidate/Recovery | ordered reducers |
| reconciliation query slow/fails | effect deadline/error | account new risk off | remain NON-READY/UNKNOWN, retry bounded/escalate | no false consistency |
| Recorder P0 backlog/loss threat | priority queue/disk health | off before silent critical loss | preserve P0, shed lower priority, safe stop | ordered Recorder/health event |
| Recorder P2/P3 backlog | queue counters | unchanged | sample/coarsen/drop declared detail | economic truth unchanged |
| archive unavailable | upload/backoff/verification | unchanged | keep local/pending, alert/capacity action | none economic |
| disk full/slow | filesystem/queue/disk state | off if P0 integrity threatened | shed optional, rotate only safely, safe stop | health event |
| metrics/export failure | queue/export result | unchanged unless it hides required safety evidence | shed optional telemetry, local alert | none economic |
| model unavailable/OOD | load/inference/support state | fallback scope only | simple validated model, shrink or reject | capability/health event by owner |
| optional Atlas stale | freshness/version | dependent scope shrinks/off | last valid within rule or UNKNOWN | owner publishes status |
| two-vCPU oversubscription | scheduler/I/O-delay/tail metrics | shrink/off if safety SLO breached | reduce optional work/workers, prioritize safety | policy event only |
| shutdown during execution | lifecycle + active ESM | new risk off | keep fills/cancel/Recovery/reconcile, bounded P0 drain | ordered shutdown states |
| restart during `UNKNOWN` | journal/checkpoint/exchange evidence | off | fence, orders→fills→balances, reconcile | ordered recovery only |
| remote license/release service unavailable | background effect result | commercial new risk per cached policy | safety actions remain; no auto update | typed control event |

Background failure remains scoped by criticality and dependency. A healthy background restart does not automatically restore capability; current state consistency and explicit readiness evidence are required.
