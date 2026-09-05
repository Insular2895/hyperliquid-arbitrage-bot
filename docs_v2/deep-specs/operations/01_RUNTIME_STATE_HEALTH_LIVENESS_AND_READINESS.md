# 01 — Runtime State, Health, Liveness and Readiness

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Liveness reports whether the process/control loop can respond and progress. Readiness answers whether a named action is currently permitted in a named scope. Therefore `live=true, ready=false` is normal during boot, sync, reconciliation, degraded operation, update and incident hold.

Readiness consumes artifact/config/owner/license state; clock/feed/book/account/order/fill health; reconciliation; model/simulator support; InfraState; CapabilityManifest; active exposure; and RiskDecision. It emits boolean/action scope plus machine-readable blockers and evidence versions.

Health is scoped and three-valued or richer: healthy, degraded, unsafe/unknown. Missing is not healthy. A local market/model can be suspended while unrelated capabilities remain. Shared account/owner/authority uncertainty generally blocks broader new risk.

Safe actions remain distinct: new risk, risk reduction/Recovery, cancel, reconciliation, persistence and read-only diagnostics. Removing new-risk permission must not trap exposure or suppress evidence.
