# Network Exposure Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Flow/interface | Direction | Default binding | Allowed data | Rule |
|---|---|---|---|---|
| Hyperliquid market/API | Egress | N/A | Market, account, order/cancel traffic | Required; authenticated scope minimal |
| DNS/NTP/host updates | Egress | Host-managed | Infrastructure operations | Constrained and monitored |
| OCI registry | Egress, update time | N/A | Image/auth metadata | Read-only credential; not hot path |
| License validation | Egress, cold/control path | N/A | Minimal signed entitlement request | Cached; never hot path; no signer/private key |
| Metrics | Inbound local/private | Loopback or private admin plane | Aggregated health | No public unauthenticated binding |
| Health/readiness | Inbound local | Loopback/container-local | Non-secret status | Must not expose account secrets |
| Admin/`botctl` | Local socket/CLI | Local-only | Authenticated control | No public `0.0.0.0` default |
| Telemetry | Optional egress | Disabled unless opted in | Version, health, crash/benchmark summary | No raw orders, full balances/history or credentials |
| Support access | Temporary inbound if client enables | Client-controlled restricted channel | Incident-scoped | Audited and removed after use |
| Future dashboard | Prefer outbound initiated | None initially | Sanitized telemetry | Separate design/validation required |

Container bridge versus host networking remains an empirical performance and threat-model choice. Any inbound port must be enumerated, justified, bound narrowly, authenticated where relevant and tested. Vendor infrastructure is not required for order execution.
