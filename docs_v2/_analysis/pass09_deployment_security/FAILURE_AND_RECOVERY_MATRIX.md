# Failure and Recovery Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

In every row, unknown or unsafe state forbids new risk. Existing exposure is observed and handled through cancel, reconciliation and bounded Recovery whenever the required authority remains available.

| Failure | New risk / exposure action | Recovery, rollback and reconciliation | Escalation / evidence |
|---|---|---|---|
| Image verification failure | Block / leave current owner unchanged | Delete/re-download candidate; no activation | Release/integrity incident retained |
| Config invalid | Block / no new effects | Correct, revalidate and restart startup cycle | Validation errors + sanitized config hash |
| Secret missing | Block / query if possible | Provision locally then authenticate/reconcile | No secret values in evidence |
| Secret revoked | Block / cancel if alternate authority permits | Rotate, validate, reconcile; revoke old after safe migration | Security incident and account audit |
| License unreachable | Cached-policy envelope / safe actions continue | Retry off hot path | Outage and cache state retained |
| License invalid/expired/revoked | Block / cancel-reconcile-Recovery allowed | Repair entitlement only restores eligibility after full checks | License reason and signature metadata |
| Registry unavailable | Current version continues / unchanged | Retry download later | Registry status; no forced replacement |
| Network unavailable | Block / track uncertainty | Reconnect, resync and reconcile | Timings/reason codes retained |
| Exchange unavailable | Block / exposure unknown | Recovery after reconnect and reconciliation | Incident window retained |
| Clock unhealthy | Block / safe observation/cancel | Restore host clock health; re-evaluate freshness | Offset/uncertainty evidence |
| State incompatible | Block | Explicit migration or reconstruct from journal/exchange | Compatibility report; rollback only if safe |
| Checkpoint corrupt | Block | Preserve corrupt artifact; earlier checkpoint/journal then reconcile | Checksums and recovery trace |
| Journal corrupt | Block affected scope | Preserve, isolate, rebuild from other truth sources; manual review | Corruption range/checksums retained |
| Disk full/critical | Block before unsafe exhaustion / prioritize economic truth | Shed lower-priority data, expand/recover storage, reconcile | Watermarks and deletion audit |
| Container crash | Block after restart | `BOOTING→SYNCING→RECONCILING`; no automatic trading | Crash evidence; loop leads `HALTED` |
| Host reboot | Block | Full preflight, sync and reconcile | Boot/runtime/clock evidence |
| Update failure | Remain/return no-risk | Continue old owner if never stopped; otherwise known rollback path | Update transaction log |
| Rollback failure | Block / Recovery if possible | Forward repair or manual recovery; reconcile | Preserve both artifacts/migration markers |
| Old process active | Block all contenders | Fence/isolate/revoke as needed; account reconciliation | Split-brain incident |
| Diagnostic failure | Block promotion if required evidence absent | Repair diagnostics; lower modes may remain | Failed check and tool version |
| Schema migration failure | Block | Restore coherent backup if compatible or forward repair | Migration journal/checksums |

No failure path may discard evidence solely to regain READY. Manual escalation is mandatory when ownership, exchange truth, schema compatibility or safe signer authority cannot be established.
