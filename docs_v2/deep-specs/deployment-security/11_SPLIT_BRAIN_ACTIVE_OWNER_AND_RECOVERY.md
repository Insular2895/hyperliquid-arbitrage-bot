# 11 — Split Brain, Active Owner and Recovery

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Invariant

At most one process may take new risk for an installation/account/signer authority at a time. A local exclusive process lock is the initial mechanism; it prevents duplicate starts on one host but is not a distributed fencing proof.

Ownership is acquired only after artifact/config prerequisites and before effects, and Live authority arrives only after sync/reconciliation/readiness. It is released after risk-off, active-work resolution and persistence. A stale lock can be removed only after checking process identity and exchange/account activity.

## Ambiguity rule

If two processes, hosts or manifests might be active, all contenders lose new-risk permission. Safe actions remain cancel, reconcile, reduce/Recovery and stop. Operators isolate the old host or revoke/fence its signer, establish exchange truth and then perform a full startup cycle. There is no optimistic winner election.

## Scenarios

Normal update and rollback prove old-owner stop before new activation. Host migration has no overlap. Unexpected old-process activity is a security/ownership incident. Restart storms transition to `HALTED` with backoff and evidence preservation. Manual duplicate start fails idempotently without disturbing a healthy owner.

## Future standby

Hot standby, multi-host failover or centralized fleet controls are `FUTURE`. They require a specified lease/fencing source, partitions and clock semantics, signer ownership, stale-owner revocation, account-level detection, recovery actions and tests. Until then the supported resilience strategy is reproducible cold recovery.

## Reconciliation

After any crash, forced kill, reboot, rollback, migration or ownership anomaly, orders → fills → balances/inventory are reconciled. Local checkpoint/journal helps reconstruct intent and evidence but cannot override exchange truth. Unknown economic truth keeps affected capability out of READY.
