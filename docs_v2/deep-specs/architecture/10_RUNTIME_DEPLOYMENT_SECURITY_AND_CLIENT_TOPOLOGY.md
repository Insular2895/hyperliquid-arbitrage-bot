# 10 — Runtime, Deployment, Security and Client Topology

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

The baseline is one client VPS, one OCI trading container, one Rust process, one account/signer/capital context and one active economic owner. Config, secrets, mutable state, data and logs use explicit external mounts/boundaries; the immutable digest contains software only. Host clock synchronization and local `botctl`/diagnostics support the container.

Runtime hardening is non-root/read-only/minimal with dropped capabilities, explicit mounts, no privileged mode, Docker socket, host root/PID access or clock-setting. The API signer is least privilege and has no withdrawal authority. Registry and licensing are control-plane dependencies outside the trading path; loss of either cannot remove cancel/Recovery/Reconciliation/data access.

Startup is non-ready through BOOTING/SYNCING/RECONCILING; process liveness is not trading readiness. Shutdown first blocks new risk and resolves or contains outstanding economic state. Update, rollback and host move transfer single ownership, then boot and reconcile against current exchange truth.

Python research/archive is a separate offline environment. No Redis/Postgres/Kafka/Kubernetes/microservice mesh is a baseline hot-path dependency. A future node or standby creates new security, link, state synchronization and fencing obligations.

CORR-04 keeps Docker as baseline and treats bridge/host/native as security-preserving benchmark treatments. A node may be co-hosted or separated only as a studied topology; it has no signer secret by default. Host network, device/hugepage access and kernel bypass require explicit least-privilege/threat/rollback evidence and never justify privileged mode or Docker-socket access.
