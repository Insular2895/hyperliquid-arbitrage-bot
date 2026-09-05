# 08 — Update, Rollback, Migration and Host Move

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Transactional update

An update first checks/downloads without disturbing the owner. It verifies digest/signature/channel/provenance, validates config and schema compatibility, disables new risk, resolves/drains active executions, produces a coherent backup/checkpoint, stops and proves release of the old owner, starts the new digest non-ready, applies declared migration, reconciles exchange truth, checks health/capability and only then reaches READY.

Each phase is restartable/idempotent or has an explicit compensating transition. State records candidate/current/previous digest, owner, migration marker, backup ID, exposure condition and last completed step.

## Failure semantics

- Before old-owner stop: reject candidate and retain the current safe owner.
- After stop but before compatible start: activate known previous digest if safe.
- After migration: use the declared rollback path; if reverse reading is unsafe, perform forward repair.
- After exchange state changed: never restore stale economic truth; reconcile.
- At any ambiguity: no new risk and manual escalation.

Rollback is not a database rewind. It is code/artifact replacement followed by current-state reconciliation. Backward-compatible storage is preferred; destructive migration requires backup, marker and tested recovery.

## Safe stop and reboot

`SIGTERM`/`stop --safe` disables new risk, cancels/resolves, persists and releases ownership. Forced exit/reboot is recorded and causes full startup reconciliation. A crash restart never resumes READY from a persisted boolean.

## Host move

Old host risk-off → resolve → backup/persist → stop/fence → new host preflight → non-ready start → sync/reconcile → evidence/capability → READY. There is no dual-active window. If old-host status is unknown, its authority is revoked/fenced before new risk. Cold recovery is baseline; hot standby is future work.
