# Capability Promotion Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| From → to | Mandatory proof | Decision record |
|---|---|---|
| untracked → M0 | complete specification and ownership | scope, dependencies, planned evidence |
| M0 → M1 | unit/property/golden as applicable; failure cases; performance budget measured | immutable test run and deviations |
| M1 → M2 | deterministic Replay, no lookahead, realistic failures, exact versions | RunManifest, DatasetId, trace hashes |
| M2 → M3 | same production core with no-effect transport; live feature/support/stability evidence | Shadow report and invalid intervals |
| M3 → M4 | current Risk/readiness; strict caps; incident/safe-stop/recovery readiness | Micro-live plan, predeclared gates and approver |
| M4 → M5 | sustained real calibration, economic value after costs, acceptable tail risk and operations | signed/scoped promotion decision and rollback |
| size/market/mode expansion | all prior evidence plus evidence specific to the new band/scope | new manifest entry; never mutate old evidence |

Models additionally require temporal OOS improvement, calibration, `EconomicLift > 0`, runtime and safe OOD/fallback. Release promotion requires critical unit/integration/golden Replay, security/Risk regression and performance evidence; trading-logic changes also require Shadow and Micro-live. A docs-only change does not inherit or demand capital evidence.

No promotion is automatic. Unknown/missing evidence is failure to promote, not a soft pass.
