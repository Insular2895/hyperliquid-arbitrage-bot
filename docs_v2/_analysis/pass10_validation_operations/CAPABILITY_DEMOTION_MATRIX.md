# Capability Demotion Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Trigger | Minimum response | Possible target | Resume condition |
|---|---|---|---|
| critical invariant or Risk violation | stop affected new risk; preserve evidence | Suspended / below M4 | root cause, fix, Replay + required live revalidation |
| unknown order/account/reconciliation | lock affected capital and reconcile | capability unavailable | exchange truth proven and reservations consistent |
| model drift/OOD/calibration failure | fallback, reduce size or disable dependents | Degraded/Disabled; M3 or lower | new artifact or restored support with full promotion evidence |
| Simulator underestimation | shrink Q_validated and confidence; disable dependent modes | lower validated size/fidelity | predicted/actual calibration restored |
| stale/gapped feed or unhealthy clock | no latency-sensitive new risk | degraded/no-new-risk | sustained health plus book/account reconciliation |
| critical security or secret compromise | fence signer/owner; risk-off | release/capability rejected | rotation, containment, integrity proof, clean restart |
| artifact/config/schema incompatibility | reject activation/rollback | previous compatible scope | verified artifact and migration/replay evidence |
| host move/material infra change | remove inherited profile authority | M3 maximum until proven | diagnostic/benchmark, Shadow and required Micro-live |
| exchange-rule change | block affected markets/modes | scoped suspension | external fact validation + regression/Replay/live evidence |
| incident invalidates M5 assumption | immediate scoped demotion | any lower safe level | postmortem actions and explicit re-promotion |

Demotion is monotone toward safety, can be automatic when a locked safety condition fails, and is always audited. Restoring health does not silently restore the previous maturity.
