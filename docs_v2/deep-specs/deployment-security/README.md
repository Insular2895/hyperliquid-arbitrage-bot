# Deployment and Security Deep Specs

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

These specifications refine [the Deployment/Docker master](../../14_DEPLOYMENT_AND_DOCKER.md). They define contracts and evidence boundaries; they do not select unfrozen vendors/tools, implement deployment automation or authorize Live use.

1. [Commercial model, client isolation and ownership](01_COMMERCIAL_MODEL_CLIENT_ISOLATION_AND_OWNERSHIP.md)
2. [OCI image, build provenance and supply chain](02_OCI_IMAGE_BUILD_PROVENANCE_AND_SUPPLY_CHAIN.md)
3. [Container hardening and filesystem](03_CONTAINER_RUNTIME_HARDENING_AND_FILESYSTEM.md)
4. [Configuration, secrets, signer and credential lifecycle](04_CONFIGURATION_SECRETS_SIGNER_AND_CREDENTIAL_LIFECYCLE.md)
5. [Network boundaries, admin, health and telemetry](05_NETWORK_BOUNDARIES_ADMIN_HEALTH_AND_TELEMETRY.md)
6. [Startup, preflight, readiness and onboarding](06_STARTUP_PREFLIGHT_READINESS_AND_ONBOARDING.md)
7. [Release channels, capabilities and promotion](07_RELEASE_CHANNELS_CAPABILITIES_AND_PROMOTION.md)
8. [Update, rollback, migration and host move](08_UPDATE_ROLLBACK_MIGRATION_AND_HOST_MOVE.md)
9. [Licensing fail-safe and commercial enforcement](09_LICENSING_FAIL_SAFE_AND_COMMERCIAL_ENFORCEMENT.md)
10. [`botctl`, diagnostics, redaction and incident export](10_BOTCTL_DIAGNOSTICS_REDACTION_AND_INCIDENT_EXPORT.md)
11. [Split brain, active owner and recovery](11_SPLIT_BRAIN_ACTIVE_OWNER_AND_RECOVERY.md)
12. [Validation, failure modes and definition of done](12_VALIDATION_FAILURE_MODES_AND_DEFINITION_OF_DONE.md)

Cross-domain authority remains with Risk (permission), Execution (orders/recovery/reconciliation), Data/Recorder (truth/schemas/persistence), Infrastructure (host evidence), and future Validation/Operations passes.
