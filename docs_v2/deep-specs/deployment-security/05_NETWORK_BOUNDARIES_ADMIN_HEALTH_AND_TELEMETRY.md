# 05 — Network Boundaries, Admin, Health and Telemetry

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Flows

The sole required trading path is client host ↔ Hyperliquid feed/API. Registry and license service are update/control-plane egress, never synchronous decision-path dependencies. DNS, clock synchronization and host package operations are host concerns with explicit policy.

Metrics, health and admin are local-only or on a client-controlled private authenticated plane. No public unauthenticated admin listener is permitted. Every inbound port and bind address appears in the DeploymentManifest/diagnostic inventory and an installation scan.

Bridge versus host network mode remains a combined latency benchmark and threat-model decision. Neither is declared universally superior.

## Health surfaces

Liveness reports progress/deadlock state. Readiness reports whether all prerequisites for considering new risk are met. Trading health reports `READY`, `DEGRADED`, `RECOVERY_ONLY` or `HALTED`. Health output contains version, state and reason codes without private keys, API tokens, raw orders or full account state.

Supervision may restart a dead process but must not restart a healthy reconciler merely because it is not READY. Every restart begins non-ready.

## Telemetry and support

Telemetry is minimal, opt-in and independently consented. Candidate fields include version, coarse health, crash class, benchmark summary and anonymous performance aggregates. It excludes credentials, raw orders, full balances, full history and arbitrary files.

A support bundle is generated locally, allowlisted, redacted, scanned and reviewed by the client before explicit transfer. Temporary support access is client-enabled, least-privilege, time-bounded and audited. Future remote dashboard work should prefer outbound client-initiated data flow and requires its own threat model/validation.
