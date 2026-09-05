# Split-Brain and Active-Owner Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Scenario | Detection | Process allowed to trade | New-risk block | Reconciliation / intervention |
|---|---|---|---|---|
| Normal update | Local owner lock, process identity, manifest | Old until safely stopped; new only after reconcile | Update state disables before handoff | New process reconciles; manual if old cannot be proven stopped |
| Rollback | Digest/process/lock transition | No process during swap; previous only after checks | Rollback state | Reconcile current exchange truth; escalate incompatibility |
| Host migration | Explicit migration token/runbook plus account observations | Old until stopped; then new after proof | Both configured risk-off during handoff | New host full sync/reconcile; operator confirms old host off |
| Unexpected old process alive | Duplicate identity, exchange activity, lock/heartbeat anomaly | Neither gains new-risk authority | Global/account kill | Cancel/reconcile; revoke old signer or isolate host |
| Restart storm | Supervisor count/backoff and repeated startup state | None | Crash-loop `HALTED` | Preserve evidence; manual root-cause clearance |
| Future standby | Lease/fencing design not yet validated | Fenced active owner only | Standby has no Live credentials/permission until ownership proof | Future architecture and validation required |
| Manual duplicate start | Exclusive local lock and PID/process check | Existing healthy owner only | Second start fails | Operator resolves stale lock only after process/account checks |

Initial local locking reduces accidental duplicates but is not a distributed fence. A second host or hot standby is `FUTURE` until account-level ownership, fencing, lease expiry, partitions and recovery are specified and validated. Ambiguity always removes new risk; it never elects two winners.
