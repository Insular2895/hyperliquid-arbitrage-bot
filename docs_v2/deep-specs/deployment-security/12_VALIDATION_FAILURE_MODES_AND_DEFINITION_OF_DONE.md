# 12 — Validation, Failure Modes and Definition of Done

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Evidence families

PASS09 requires future executable evidence for artifact provenance/digest/signature, runtime least privilege, read-only filesystem, secret absence, config/schema rejection, startup reconciliation, safe shutdown, update/rollback/migration, single-owner behavior, license failures, local network binding, diagnostic redaction, host migration and release promotion.

Evidence identifies installation, artifact/config/model/schema/capability versions, host/runtime profile, time, test vector, result and retained artifacts. A missing test is not a pass. Golden nominal paths alone are insufficient; fault injection must cover every state transition that can affect ownership, exposure or persistence.

## Failure classes

| Class | Examples | Required posture |
|---|---|---|
| Integrity | Wrong digest/signature, vulnerable/untrusted artifact | Reject before activation |
| Configuration | Invalid config or incompatible schema/model/formula/event | No READY; migrate/repair explicitly |
| Authority | Missing/revoked secret, ambiguous owner | No new risk; fence/reconcile |
| External | Registry/license/network/exchange outage | Preserve current safe state; degrade explicitly |
| Persistence | Disk full, corrupt checkpoint/journal, failed migration | Protect evidence; reconstruct/reconcile; manual if unknown |
| Lifecycle | Crash, reboot, update/rollback/start failure | Restart non-ready through sync/reconciliation |
| Privacy | Secret in log/bundle/telemetry | Fail export/promotion; rotate and respond |

## Definition of done

Installation DoD requires verified immutable artifact, supported platform, isolated/hardened runtime, explicit mounts, valid config/schema, safe signer and network/preflight evidence. Micro-live DoD adds deterministic/replay/Shadow evidence, reconciled account truth, bounded capital/size, Risk authority and tested safe stop/recovery. Live DoD adds promoted Stable/capability evidence and current local gates.

Upgrade DoD proves active and no-exposure cases, failures at each step and compatible migration. Rollback DoD proves current exchange truth wins even after state changes. Security DoD proves credentials absent from image, logs and exports; admin local; supply-chain verification; and client-controlled support.

## Ownership and limits

PASS10 will freeze CapabilityManifest/evidence promotion and final test ownership. Operations will turn failure behavior into runbooks. Current exchange, platform and vulnerability facts require external revalidation. Exact thresholds and products remain calibrated/open. This specification authorizes neither implementation nor Live activation.
