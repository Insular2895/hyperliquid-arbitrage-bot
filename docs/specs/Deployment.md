# Deployment

## Purpose

Installer et exploiter une instance client isolée, reproductible et rollbackable.
## Responsibilities

Image/config/secrets/volumes/service/update/rollback/readiness lifecycle.
## Non-responsibilities

Ne mutualise pas le hot path et n'auto-active pas live.
## Inputs

Signed image digest, config, secrets, entitlement and host baseline.
## Outputs

One non-root process/container with deployment manifest.
## Dependencies

Signer secret provider, Recorder storage, InfrastructureMonitor, CapabilityRegistry.
## State

Installed/current/previous digest, schema/config and service state.
## Algorithms / formulas

Preflight→sync→reconcile→ready; safe update/rollback flow.
## Invariants

No latest/privileged/socket; one writer/account; licence never blocks recovery.
## Failure modes

Bad image/config/migration, disk/secret/licence/network, interrupted update.
## Risk interactions

Any uncertainty starts risk-off; rollback always reconciles.
## Performance requirements

Container overhead benchmarked; no control-plane hot dependency.
## Metrics

Starts/restarts/readiness/update/rollback/resource/security scan.
## Persistence

State/journal/data/models/config outside replaceable container.
## Configuration

Host/network/resources/retention with validated defaults or OPEN.
## Tests

Fresh install/update/rollback/reboot/SIGKILL/migration/licence/security.
## Maturity requirement

M2 container replay; M3 canary; M4 live rollback drill.
## Open calibrated parameters

Host/bridge, resources, distro/runtime versions, licensing provider.
