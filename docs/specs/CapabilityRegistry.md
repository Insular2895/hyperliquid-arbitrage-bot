# CapabilityRegistry

## Purpose

Empêcher l'activation au-delà de la maturité et des preuves approuvées.
## Responsibilities

Load/verify manifests, resolve dependencies/restrictions and runtime permissions.
## Non-responsibilities

Ne produit pas la preuve et ne remplace pas RiskEngine.
## Inputs

Signed CapabilityManifest, environment, module/model/config versions.
## Outputs

Enabled/observe/disabled capability map with reasons.
## Dependencies

Deployment, all module version registries, RiskEngine.
## State

Approved manifest/version and current environment mapping.
## Algorithms / formulas

Dependency closure and minimum maturity checks.
## Invariants

Code presence≠permission; unknown/mismatch fail closed; no environment escalation.
## Failure modes

Tampered/stale manifest, missing evidence/dependency, incompatible version.
## Risk interactions

Provides maximum permission envelope; RiskEngine may further restrict.
## Performance requirements

Precomputed lookup; verification off hot path.
## Metrics

Capabilities/status/rejections/manifest age and mismatches.
## Persistence

Manifest/signature/approvals/change audit.
## Configuration

Environment and trust roots; no self-promotion by live system.
## Tests

Dependency/maturity/version/tamper/environment downgrade cases.
## Maturity requirement

M1 before M3/M4 activation workflows.
## Open calibrated parameters

Approval/signing workflow and evidence retention.
