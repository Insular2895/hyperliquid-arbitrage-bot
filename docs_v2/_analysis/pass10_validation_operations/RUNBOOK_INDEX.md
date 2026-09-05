# Runbook Index

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Every runbook begins with safety posture and evidence capture, identifies automated versus human steps, and ends with explicit reconciliation/revalidation. Commands are conceptual until the implementation/API pass freezes them.

| Runbook | Trigger | First action | Resume proof |
|---|---|---|---|
| RB-01 Feed/Book Desync | stale/gap/crossed/version mismatch | stop affected new risk; preserve feed evidence | valid snapshot, ordered catch-up, book and dependent state rebuilt |
| RB-02 Account Unreconciled | balance/order/fill mismatch | lock scope; query exchange truth | orders→fills→balances→reservations consistent |
| RB-03 Unknown Order | lost/ambiguous submit/ACK | no resend; query CLOID/OID/fills/account | unique final effect or continued safe lock |
| RB-04 Cancel/Fill Race | fill near cancel | apply fill idempotently; resolve remainder | terminal order plus reconciled exposure |
| RB-05 Recovery Failure | bounded exit fails | no new risk; escalate incident | exposure resolved or explicit controlled hold |
| RB-06 Crash/Reboot | forced exit/restart | start non-ready | journal/checkpoint/exchange reconstruction and readiness gates |
| RB-07 Disk Pressure | disk low/full/fsync/backlog | protect pinned evidence; apply recorder policy | storage stable, quality accounted, persistence safe |
| RB-08 Clock Unhealthy | offset/uncertainty/step | disable latency-sensitive decisions | sustained sync health and affected state refresh |
| RB-09 Model Drift/OOD | calibration/support alarm | fallback/reduce/disable dependents | reviewed evidence and explicit re-promotion |
| RB-10 Infrastructure Degraded | latency/jitter/network/resource | scope-degrade through Risk | sustained health plus reconciliation if connectivity changed |
| RB-11 Update/Rollback Failure | interrupted/incompatible release | keep/restore verified safe digest; no new risk | owner, migration, integrity and exchange state proven |
| RB-12 License Outage | invalid/unreachable license | block new risk only | valid entitlement and normal readiness; exits never trapped |
| RB-13 Secret Compromise | credential exposure/suspicion | fence/revoke/rotate; risk-off | clean artifact/config, owner, account audit and reconciliation |
| RB-14 Split Brain | ambiguous active owner | fence all ambiguous writers | exactly one owner with current account truth |
| RB-15 Exchange Rule Change | reject/metadata behavior change | suspend affected market/mode | official fact revalidated and dependent tests rerun |

P0/P1 runbooks create or attach an IncidentId and pin the incident evidence window.
