# 14 — Deployment, Docker, Security and Client Distribution

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## 1. Purpose

This master defines how the bot is packaged, delivered, installed, started, operated, updated, recovered and supported on a client's infrastructure. Its safety objective is simple: packaging or commercial enforcement must never create unauthorized trading, dual ownership, lost economic truth, leaked credentials or stranded exposure.

## 2. Authority

SRC-006 Dossier 5 closure is the primary authority. PASS00 preserves all 426 Deployment/Security requirements and their locators. The Risk Constitution owns permission and safe degradation; Execution owns orders, fills, cancellation, Recovery and reconciliation; Data/Recorder owns schemas, journal, checkpoint, retention and economic truth; Infrastructure owns measured host suitability; future Validation and Operations passes own evidence promotion and operational runbooks.

Status vocabulary:

| Status | Meaning |
|---|---|
| `LOCKED` | Required architecture or behavior supported by closure authority |
| `CALIBRATED` | Mechanism required; value/profile selected from measured evidence |
| `OPEN` | Tool/provider/policy decision not yet frozen |
| `EXTERNAL_REVALIDATION` | Current external fact must be checked before use |
| `FUTURE` | Compatible direction with no current activation authority |

## 3. Commercial distribution model

The bot is distributed software, not a centralized multi-tenant execution SaaS. The normal path is client → own VPS/server → own OCI container/process → own Hyperliquid account → own signer/API wallet → own capital. Vendor infrastructure is not required to submit, cancel or recover a trade.

The deliverable includes a private immutable image, `botctl`, Compose and config templates, documentation, release metadata/channel, signed license entitlement and support. Source distribution is not required. Docker does not guarantee IP secrecy; intellectual-property protection relies on commercial, legal and access controls as well as reasonable artifact minimization.

## 4. Client ownership / isolation

The client owns the host, exchange account, capital, signer, configuration, persistent data, logs and decision to activate Live capability. The vendor owns release production, compatibility declarations, documentation and support tooling. Each installation has isolated credentials, volumes, config, license and `installation_id`.

There is no shared execution engine, pooled signer or pooled capital. A fleet of clients is a fleet of isolated deployments. Support access is temporary, client-controlled and audited; diagnostics remain local until the client explicitly exports them. There is no hidden backdoor.

## 5. OCI image

The portable artifact is an OCI image. Docker Engine with Compose is the initial supported runtime; orchestration remains provider-agnostic. V1 targets `linux/amd64`; other architectures require their own build and evidence.

The image is multi-stage and minimal: the runtime contains the executable and required runtime assets, not the Rust compiler, Cargo tooling or source tree. It is immutable and replaceable. Mutable config, secrets, state, recorder data and logs are external mounts. Stable models may ship with the image; separately promoted models are independently hash-addressed and schema-checked.

Production is pinned to an explicit semantic version and immutable digest. Tags are navigation only. No production `latest` is permitted.

## 6. Artifact provenance

Every release identity binds:

- semantic application version;
- Git revision;
- OCI digest and platform;
- build timestamp, toolchain and build configuration;
- dependency-lock identity;
- config, checkpoint, journal, event, model and feature-schema compatibility;
- SBOM, vulnerability result and signature/provenance evidence.

`DeploymentManifest` records at least `installation_id`, `image_digest`, version, `config_hash`, model versions and `started_at`. It links to but does not replace PASS06 `RunManifest`. A wrong digest, invalid signature, unsupported platform or incompatible schema blocks activation.

## 7. Runtime hardening

The process runs as a dedicated non-root user with a read-only root filesystem and only declared writable mounts. The runtime drops Linux capabilities by default and is neither privileged nor granted the Docker socket, host root, host PID namespace or `CAP_SYS_TIME`. Host time synchronization remains a host responsibility.

CPU, memory, PID, swap/OOM and optional affinity policies are explicit and benchmarked. Pressure thresholds must disable new risk before loss of safe persistence or recovery ability. Exact seccomp/AppArmor tooling, UID and limits remain implementation/calibration choices.

## 8. Filesystem/persistence boundary

| Class | Boundary |
|---|---|
| Image/root | Immutable and replaceable |
| `/config` | Client-owned, read-only at runtime |
| `/run/secrets` | Client-owned, read-only, never ordinary backup/export |
| `/data/state` | Persistent coherent state/checkpoints |
| `/data/journal` | Persistent execution/economic recovery evidence |
| `/data/recorder` | PASS06 priority, quality and retention rules |
| `/data/models` | Optional independent promoted artifacts with manifests |
| `/logs` | Bounded operational data; not economic truth |

Disk states `NORMAL`, `LOW` and `CRITICAL` are calibrated. Cleanup protects journal, unique fills, account truth, checkpoints and active trade/incident windows before lower-priority derived data. The minimum backup set is config/schema metadata, journal, coherent state/checkpoint and critical history; secrets have a separate secure procedure. Restore always reconciles against exchange truth.

## 9. Configuration

Configuration lives outside the image, is parsed and validated into an immutable normalized `ResolvedConfig`, and produces a `config_hash`. Config files carry a schema version. Missing, invalid, inconsistent or incompatible configuration blocks readiness with a stable reason.

Migrations are explicit and auditable; no release silently reinterprets a value. Client overrides may tighten Risk policy but cannot weaken constitutional floors. Application/config/checkpoint/journal/event/model/feature/formula compatibility is declared before update or rollback.

## 10. Secrets / signer

Private keys, API-wallet secrets, registry credentials and license credentials never enter an image, source bundle, ordinary config, CLI argument, environment dump, log, metric, diagnostic export or vendor system. A read-only secret file with strict host permissions is preferred. The exchange signer uses least privilege and no withdrawal permission.

Lifecycle: local provision → scope validation → read-only mount → restricted use → controlled rotation → old credential revocation after safe migration. Rotation runs risk-off, reconciles, replaces, restarts/reloads, revalidates and reconciles before READY. Memory zeroization is desirable where practical but does not replace the boundary.

## 11. Network exposure

The required hot path is the client VPS to Hyperliquid. Registry and license traffic are cold/control-plane egress. Health, metrics and admin surfaces bind to loopback or a private authenticated plane; no unauthenticated public `0.0.0.0` admin default exists.

Every inbound port is enumerated, justified and tested. Telemetry is minimal and opt-in and excludes secrets, raw orders, full balances and full trading history. Future remote dashboards should prefer outbound client-initiated transport. Docker bridge versus host networking is selected through benchmark and threat model, not assumption.

## 12. Supply-chain security

Source revision, dependency lock, builder/toolchain, image, SBOM, scan, signature, digest, registry transfer, local verification, activation and audit form one chain. Client registry credentials are read-only. Known critical vulnerabilities require explicit assessed acceptance before promotion; unassessed critical findings block it.

Exact registry, signature, SBOM and scanner products remain `OPEN`, but local fail-closed verification before owner replacement is locked. A staged download cannot alter the current active owner.

## 13. Startup / preflight / readiness

Every process starts without new-risk authority:

```text
BOOTING -> CONFIGURING -> CLOCK_CHECK -> CONNECTING
        -> SYNCING -> RECONCILING -> RISK_CHECK -> READY
```

Preflight verifies artifact identity, host/runtime profile, mounts, writable capacity, config/schema, secret presence and signer scope, network/exchange reachability, clock health and absence of another owner. Sync loads metadata, books, account, orders and fills. Reconciliation follows orders → fills → balances/inventory and resolves local-versus-exchange differences.

Invalid evidence leads to `DEGRADED`, `RECOVERY_ONLY` or `HALTED`, never optimistic READY. Automatic restart is not automatic trading.

## 14. Client onboarding

```text
INSTALL -> PREFLIGHT -> DIAGNOSTIC -> SYNC -> RECONCILE
        -> SHADOW -> MICRO-LIVE -> LIVE
```

The installer creates/checks explicit directories, templates and runtime prerequisites. It does not generate or upload private keys, silently alter host security or start Live. `botctl benchmark` measures CPU, scheduler, memory, disk, clock, feed/API RTT and Docker overhead. An unsupported host may retain Replay/Shadow while Micro-live/Live remains unavailable.

Each promotion requires evidence plus explicit client/operator intent. Failed evidence demotes capability conservatively.

## 15. RunMode / capability separation

Replay, Shadow, Micro-live and Live use the same core artifact and reducers; effects and provenance differ. Six axes remain separate:

1. compiled support;
2. configured enablement/RunMode;
3. license entitlement;
4. release channel;
5. validated scope in `CapabilityManifest`;
6. current readiness and per-action Risk decision.

Effective capability is their intersection. License does not imply validated, enabled does not imply validated, and compiled does not imply validated. A license can only remove commercial permission; it cannot add safety authority.

## 16. Licensing

Licensing is outside the trading hot path. A locally cached signed entitlement, verified by an embedded public key, may contain license/installation identity, features, expiration and signature. The service never needs a client exchange private key.

A temporary service outage may use a bounded grace policy. Expired, revoked, invalid or unbound entitlement forbids new risk and transitions to `NO_NEW_RISK` or `RECOVERY_ONLY`; cancel, reconciliation, exposure reduction, safe shutdown and access to client-owned data remain available. Exact grace, binding and revocation-delivery policy require commercial/security validation.

## 17. `botctl`

Source-exact commands are `status`, `health`, `benchmark`, `config validate`, `start`, `stop`, `reconcile`, `update check`, `update`, `rollback`, `support-bundle` and `emergency-stop`. The normalized public surface also covers `install`, `preflight`, `diagnose`, `logs`, `stop --safe`, `risk-off`, `export-incident` and `version`, either as stable commands or documented aliases once implementation freezes naming.

Read/write effects, confirmation, credential needs, HALTED/license availability, exit class, audit, idempotence and redaction are specified in the command contract. State-changing actions record actor/source, installation, correlation ID, before/after state and relevant digests/hashes—never secret values.

## 18. Health / readiness

Liveness proves only that a process can make progress. Readiness means the engine currently satisfies the prerequisites to consider new risk. Trading health—`READY`, `DEGRADED`, `RECOVERY_ONLY`, `HALTED`—defines the safe action envelope, while Risk still decides every action.

Container health checks must not kill a useful recovery/reconciliation process merely because new risk is unavailable. Health output is local/private and exposes stable reasons without credentials or sensitive trading detail.

## 19. Safe shutdown

On `SIGTERM` or `stop --safe`, the engine disables new risk, cancels/resolves active executions according to Execution/Risk, persists journal/checkpoint state, releases active ownership and exits. A timeout or force-kill is recorded; the next start performs full sync/reconciliation.

`risk-off`/`emergency-stop` emits the applicable global kill before cancel and Recovery policies. Repetition is idempotent and audited.

## 20. Update

Update is a transaction:

```text
check -> download -> verify -> compatibility -> risk-off
      -> resolve/drain -> backup/checkpoint -> stop old
      -> start new without risk -> migrate -> reconcile
      -> health/capability -> READY
```

No silent automatic update is allowed. Failure before owner replacement leaves the verified current release running safely. Failure after replacement enters declared rollback or forward-repair flow with new risk disabled. Software, configuration and model updates are separate operations.

## 21. Rollback

Rollback uses a known previous digest and declared schema compatibility. It stops the failed owner, starts the previous version without new-risk authority and reconciles against current exchange truth. It never blindly restores old orders, balances or exposure from a checkpoint.

Destructive migrations require coherent backup, migration marker and tested recovery path. If an old reader cannot safely interpret new data, the correct response is forward repair or manual recovery—not forced startup.

## 22. Split-brain prevention

At most one process owns Live authority for an installation/account/signer tuple. A local exclusive owner lock covers the initial single-host baseline. Update/rollback require positive old-process shutdown before new ownership. Unknown ownership blocks all new risk.

A future hot standby or distributed owner requires explicit lease/fencing and partition/recovery validation. It is not implied by Docker restart or an exchange API wallet.

## 23. Host migration

Host migration is ordered: old host risk-off → resolve/cancel → persist/backup → stop and prove release → new host install/preflight → start non-ready → sync/reconcile → capability/health → READY. There is no planned overlap. If the old host cannot be proven inactive, revoke/fence its trading authority and reconcile before enabling the new host.

Cold reproducible recovery is the initial resilience strategy. Hot standby remains future work.

## 24. Release channels

The exact channels are `DEVELOPMENT`, `CANDIDATE` and `STABLE`. Promotion follows Code → unit → integration → golden replay → benchmark → Shadow → Micro-live → Candidate → canary → Stable. The same artifact identity advances; it is not rebuilt between evidence gates.

An emergency release retains at least unit, integration, golden replay and Shadow evidence. Old versions affected by a breaking exchange change may be restricted to no-new-risk, but they must not abandon existing exposure.

## 25. Diagnostics / redaction

The local diagnostic/support bundle contains version/digest, schema/model versions, sanitized config and hash, infrastructure/health data, bounded logs and incident IDs. It automatically excludes keys, seeds, tokens, registry/license credentials, raw memory and unnecessary account/trading history.

Bundle construction uses an allowlist plus denylist/entropy/canary-secret scans and fails closed. It records an inclusion manifest and remains local until client confirmation. Core dumps are sensitive and excluded from ordinary support export.

## 26. Incident/security response

Security priority is: protect credentials; prevent unauthorized trading; preserve state/economic truth; retain risk-reduction ability; then protect IP and convenience. Suspected signer compromise triggers new-risk disablement, safe cancel/reconciliation, credential rotation/revocation and evidence preservation.

Crash loops lead to `HALTED` and backoff rather than repeated trading attempts. Release, update, ownership, license, diagnostic and command events carry correlation/incident identity. Operations owns the final response runbooks; this pass defines their safety invariants.

## 27. External revalidation

Before production use, revalidate current Hyperliquid API-wallet permissions, signer/nonce/authentication semantics, endpoints/rate limits and any breaking exchange behavior. Also revalidate supported Linux/Docker/Compose/platform versions, registry behavior, base-image support, vulnerability state and current provider/network claims.

These facts live in `_analysis/EXTERNAL_REVALIDATION_REGISTER.md`. No web research was used to convert them into current facts in PASS09.

## 28. Validation / DoD

Installation DoD: verified artifact, supported host, isolated mounts, hardening, config/schema, secret and network/preflight tests pass. Micro-live DoD: startup reconciliation, Risk envelope, bounded capital/size, diagnostic evidence and safe stop/recovery tests pass. Live DoD: promoted capability/channel, current entitlement, readiness and per-action Risk authority all hold.

Upgrade/rollback DoD includes wrong-digest rejection, active-exposure handling, migration compatibility, dual-active prevention and exchange-changed rollback. Security DoD includes no secret in image/log/diagnostics, least privilege, local admin binding and incident export redaction. PASS10 owns final executable evidence mapping.

## 29. Deep-spec links

- [Commercial model, isolation and ownership](deep-specs/deployment-security/01_COMMERCIAL_MODEL_CLIENT_ISOLATION_AND_OWNERSHIP.md)
- [OCI build, provenance and supply chain](deep-specs/deployment-security/02_OCI_IMAGE_BUILD_PROVENANCE_AND_SUPPLY_CHAIN.md)
- [Runtime hardening and filesystem](deep-specs/deployment-security/03_CONTAINER_RUNTIME_HARDENING_AND_FILESYSTEM.md)
- [Configuration, secrets and signer lifecycle](deep-specs/deployment-security/04_CONFIGURATION_SECRETS_SIGNER_AND_CREDENTIAL_LIFECYCLE.md)
- [Network, admin, health and telemetry](deep-specs/deployment-security/05_NETWORK_BOUNDARIES_ADMIN_HEALTH_AND_TELEMETRY.md)
- [Startup, readiness and onboarding](deep-specs/deployment-security/06_STARTUP_PREFLIGHT_READINESS_AND_ONBOARDING.md)
- [Channels, capabilities and promotion](deep-specs/deployment-security/07_RELEASE_CHANNELS_CAPABILITIES_AND_PROMOTION.md)
- [Update, rollback, migration and host move](deep-specs/deployment-security/08_UPDATE_ROLLBACK_MIGRATION_AND_HOST_MOVE.md)
- [Licensing fail-safe behavior](deep-specs/deployment-security/09_LICENSING_FAIL_SAFE_AND_COMMERCIAL_ENFORCEMENT.md)
- [`botctl`, diagnostics and incident export](deep-specs/deployment-security/10_BOTCTL_DIAGNOSTICS_REDACTION_AND_INCIDENT_EXPORT.md)
- [Active owner and recovery](deep-specs/deployment-security/11_SPLIT_BRAIN_ACTIVE_OWNER_AND_RECOVERY.md)
- [Validation and failure modes](deep-specs/deployment-security/12_VALIDATION_FAILURE_MODES_AND_DEFINITION_OF_DONE.md)

Human validation is still required before any runtime, release, migration, license or Live-trading implementation decision is applied.
