# Configuration and Schema Compatibility Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Surface | Compatibility declaration | Migration | Rollback impact | Startup action / owner |
|---|---|---|---|---|
| Application ↔ config schema | Supported range embedded in release | Explicit config migration; never silent semantic reinterpretation | Old app must accept restored schema or use backed-up config | Parse/normalize/hash; invalid blocks READY — Deployment/Data |
| Application ↔ checkpoint schema | Exact readable range and writer version | Copy-on-write/backup-protected | Old reader may be incompatible | Refuse unsafe load; reconstruct/reconcile — Data/Execution |
| Application ↔ journal schema | Append/read compatibility and event version | Versioned transformation only | Cannot discard unique events | Halt new risk, retain evidence, replay/reconcile — Data |
| Application ↔ model schema | ModelManifest version/support | Rebuild or explicit adapter | Select known compatible model/fallback | Disable model-dependent capability — Participants/Deployment |
| Model ↔ feature schema | Exact feature definition/version hash | Retrain/re-export, not guess | Previous pair must remain available | Reject model activation — Participants/Data |
| Application ↔ formula version | Formula IDs/semantic version pinned | PASS11-governed migration | Decision comparability may break | Capability blocked until compatible — Formula/Data |
| Application ↔ event schema | Reader/writer compatibility window | Versioned event migration | Replay/readback must remain supported | Block affected mode, preserve raw data — Data |
| DeploymentManifest ↔ RunManifest | Link by IDs/digests; do not merge meanings | Additive governed evolution | Historical manifests immutable | Emit both compatible identities — Deployment/Data |

`ResolvedConfig` contains effective normalized values and a `config_hash`; source files remain outside the image and read-only at runtime. Client overrides may tighten risk constraints but cannot disable constitutional floors. Every incompatible or unknown relation fails closed for new risk with a stable reason; migrations are explicit, auditable and preceded by backup where state changes.
