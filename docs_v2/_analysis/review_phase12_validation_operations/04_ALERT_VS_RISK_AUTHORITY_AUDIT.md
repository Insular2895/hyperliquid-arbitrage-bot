# Alert versus Risk Authority Audit

| Condition | Canonical owner | Permission consequence | Alert/runbook |
|---|---|---|---|
| `UNKNOWN_ORDER` | Execution/Reconciliation/Risk | lock affected capital; no new risk | notify; unknown-order runbook |
| `BOOK_STALE` | Feed/Book/Risk | affected new risk off | notify; rebuild book |
| `CLOCK_UNHEALTHY` | Infrastructure/Risk | latency-sensitive new risk off | notify; resync |
| `INFRA_UNSAFE` | Infrastructure/Risk | scoped/global no-new-risk | notify; contain |
| `RECOVERY_FAILED` | Recovery/Risk | stop new risk; preserve exposure | urgent escalation |
| `SECRET_COMPROMISE` | Deployment/Security/Risk | fence signer/owner | P0 incident response |
| `DISK_CRITICAL` | Recorder/Infrastructure/Risk | protect evidence; contract permission | storage runbook |

The state transition does not depend on pager availability. Repeated notifications correlate to one incident/economic action and never execute it twice.
