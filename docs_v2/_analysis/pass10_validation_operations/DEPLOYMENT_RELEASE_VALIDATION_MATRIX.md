# Deployment and Release Validation Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Surface | Required evidence | Blocking failure |
|---|---|---|
| artifact | immutable digest, provenance/signature policy, dependency locks/scans | wrong/untrusted/vulnerable artifact |
| runtime | non-root, least privilege, read-only root, explicit mounts, no socket/privileged mode | escape/secret/write boundary violation |
| configuration | schema/model/formula/event compatibility and fail-closed validation | incompatible or unknown critical field |
| secrets/signer | absent from image/log/export; scoped access; rotation/revocation test | leak, ambiguity or unauthorized signing |
| startup/readiness | preflight, clock/feed/book/account/open-order/fill reconciliation, owner proof | READY before consistency |
| safe stop/crash | no new risk, active/resting resolution, persistence, restart non-ready | stale automatic resume |
| update/migration | transactional steps, interruption at each phase, backup/markers | incomplete artifact/migration or dual owner |
| rollback | known prior digest plus current exchange reconciliation | stale database rewind |
| licensing | failure blocks new risk but preserves safe exit/reconcile/read | trapped exposure or remote trading control |
| diagnostics | local, allowlisted/redacted, canary-secret test, explicit export | secret/account overcollection |
| release | critical unit/integration/golden Replay/security/Risk/performance; Shadow/Micro-live on trading change | missing required evidence |

Development/Candidate/Stable describes release channel. It does not grant Live scope. New builds/config/models have separate identities; a material change revalidates affected dependencies only, without silent inheritance.
