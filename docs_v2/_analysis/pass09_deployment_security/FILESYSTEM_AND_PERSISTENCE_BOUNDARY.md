# Filesystem and Persistence Boundary

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Path/class | Mutable | Persistent | Backup | Loss policy |
|---|---:|---:|---:|---|
| Image/root filesystem | No | Re-pullable | No | Replace by verified digest |
| `/config` | No at runtime | Yes, host-owned | Yes | Invalid/missing blocks READY |
| `/run/secrets` | No at runtime | Secure host/secret store | Separate secure procedure | Never included in ordinary backup/export |
| `/data/state` | Yes | Yes | Atomic/coherent | Reconcile before authority after restore |
| `/data/journal` | Append/managed | Yes | Yes | Protect before lower-priority data |
| `/data/recorder` | Yes | Yes | According to PASS06 retention | Shed lower priority before economic truth |
| `/data/models` | Controlled | Yes when externally promoted | Yes with manifests | Hash/schema verification required |
| `/logs` | Yes | Operationally persistent | Optional/retention-governed | Logs are not economic truth; rotate |
| Temporary/cache | Yes | No requirement | No | Reconstructible only |

The root filesystem should be read-only. Only declared mounts are writable. No host root, Docker socket or unrelated client directory is mounted.

## Disk pressure

`NORMAL`, `LOW` and `CRITICAL` thresholds are calibrated. Cleanup respects PASS06 priority and evidence-retention policy: protect journal, unique fills, account truth, checkpoints and active trade/incident windows; shed or rotate lower-priority derived data first. Random deletion is forbidden. Before exhaustion threatens safe persistence, disable new risk and retain cancel/reconciliation/Recovery ability.

## Backup and restore

The minimum backup set is configuration, schema/version metadata, journal, coherent state/checkpoint and critical history. The image is recovered from its digest. Secrets use a distinct client-controlled backup/rotation procedure. Every restore starts in `SYNCING`/`RECONCILING`; an old checkpoint never overrides exchange truth.
