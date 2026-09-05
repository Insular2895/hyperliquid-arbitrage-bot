# Update and Rollback State Machine

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Update

```text
CHECK -> DOWNLOAD -> VERIFY -> COMPATIBILITY -> RISK_OFF
      -> RESOLVE/DRAIN -> BACKUP/CHECKPOINT -> STOP_OLD
      -> START_NEW_NO_RISK -> MIGRATE_IF_REQUIRED -> RECONCILE
      -> HEALTH/CAPABILITY -> READY or ROLLBACK
```

| Phase | Invariant | Failure transition |
|---|---|---|
| Check/download | No change to active owner | Keep current verified version |
| Verify | Digest, signature, provenance and expected channel match | Reject candidate |
| Compatibility | Config/state/journal/model/event schemas have explicit path | Reject or require planned migration |
| Risk-off | New risk disabled before ownership change | Halt update if not provable |
| Resolve/drain | Active executions canceled/resolved or explicitly handed to Recovery | Remain old owner in safe mode |
| Backup/checkpoint | Coherent, attributable, restore-tested artifact | Do not stop old owner |
| Stop old | Ownership lock released; no active old process | Block new owner |
| Start new | Starts non-ready with the intended digest | Stop candidate on failure |
| Migrate | Explicit, logged, bounded, backup-protected | Roll back only through declared compatibility path |
| Reconcile | Exchange truth supersedes local snapshot | `RECOVERY_ONLY`/manual escalation |
| Promote | Full health and capability checks | Keep no-new-risk |

No silent automatic update is allowed.

## Rollback

Rollback selects a known previous digest and compatibility declaration, disables new risk, stops the failed owner, starts the previous image without trading authority, and reconciles against current exchange truth. It never blindly restores old economic state. Destructive migrations require a pre-migration backup, migration marker and tested reverse/forward recovery plan; otherwise rollback may mean forward repair with new risk disabled.

## Safe shutdown and host migration

On `SIGTERM` or `stop --safe`: disable new risk, cancel/resolve in-flight work, persist/journal/checkpoint, release ownership and exit. Forced kill or host reboot triggers full sync/reconciliation on restart. Host migration uses the same invariant: old host risk-off → resolve → stop/release → new host start without risk → reconcile → validate → READY; overlap is forbidden.
