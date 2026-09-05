# License Failure Permission Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

The license mechanism is outside the hot path. A locally cached, signed entitlement is verified with an embedded public key. It may identify `license_id`, `installation_id`, features, validity/expiration and signature. It never receives the client's exchange private key.

| License state | New risk | Cancel | Reconcile | Reduce/Recovery | Read/export own data | Required transition |
|---|---:|---:|---:|---:|---:|---|
| Valid and capability-supported | Risk-gated | Yes | Yes | Yes | Yes | Normal checks |
| Service temporarily unreachable, cached entitlement valid | Risk-gated within policy | Yes | Yes | Yes | Yes | Record outage; refresh later |
| Grace period | Conservative policy; may be disabled | Yes | Yes | Yes | Yes | Warn, audit, seek renewal |
| Expired | No | Yes | Yes | Yes | Yes | `NO_NEW_RISK`/`RECOVERY_ONLY` |
| Revoked | No | Yes | Yes | Yes | Yes | Immediate `NO_NEW_RISK`; audit incident |
| Invalid signature/binding | No | Yes | Yes | Yes | Yes | Treat as invalid; investigate |
| Missing/corrupt cache at startup | No | Yes if authenticated state available | Yes | Yes | Yes | Fetch/repair; never assume entitlement |

Commercial enforcement cannot strand exposure, suppress reconciliation, hide client data or disable a safe shutdown. Exact grace duration, offline renewal cadence, hardware binding and revocation distribution are `COMMERCIAL_POLICY`/`OPEN_ITEM` and require human approval plus failure tests. Binding must not be so brittle that routine host recovery becomes unsafe.
