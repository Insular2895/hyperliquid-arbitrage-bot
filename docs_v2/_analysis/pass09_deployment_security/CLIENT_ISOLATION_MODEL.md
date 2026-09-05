# Client Isolation Model

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Boundary | Required isolation | Failure containment | Evidence |
|---|---|---|---|
| Installation | Unique `installation_id` and DeploymentManifest | Incident/revocation targets one installation | Manifest plus license audit |
| Runtime | One active trading process/container initially | Crash/restart is local to client | Process identity and local owner lock |
| Exchange | One API wallet/signer per live process | Revocation does not expose other clients | Account/signer preflight |
| Capital | Client-owned balances and reservations | No pooled funds | Reconciliation against client account |
| Configuration | Per-installation external read-only config | Invalid config blocks only that installation | ResolvedConfig hash |
| Persistence | Per-installation state/journal/recorder/log volumes | Replaceable image cannot erase another client | Mount inventory and backup proof |
| License | Signed entitlement bound to installation, not private key | Vendor/license outage yields safe local degradation | Cached verification and failure matrix |
| Telemetry | Minimal and opt-in | No cross-client raw data aggregation by default | Consent and payload audit |
| Support | Client-created, redacted bundle | No automatic export | Explicit confirmation event |

## Active owner

At most one process may own Live trading authority for an account/signer/installation tuple. A local process lock is the initial control; update, rollback and host migration additionally require old-owner shutdown and exchange reconciliation. A future standby requires an explicit fencing/lease design before activation. If ownership is ambiguous, new risk is forbidden while cancel, reconciliation and bounded Recovery remain permitted.

## Trust boundaries

The vendor public verification key may be embedded in the artifact. Client private signing material may not enter the image, registry, vendor license service, logs, metrics, support bundle or crash dump. Vendor support access is client-controlled, temporary and auditable.
