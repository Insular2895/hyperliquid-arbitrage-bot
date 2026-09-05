# Onboarding and Capability Pipeline

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

```text
INSTALL -> PREFLIGHT -> DIAGNOSTIC -> SYNC -> RECONCILE
        -> SHADOW -> MICRO-LIVE -> LIVE
```

| Stage | Permitted effects | Required evidence | Promotion gate |
|---|---|---|---|
| `INSTALL` | Filesystem/runtime setup only | Supported host, verified digest/signature, isolated mounts | Installation DoD |
| `PREFLIGHT` | Read-only local/exchange checks | Config/schema, secrets/signer scope, clock, disk, network, single owner | All mandatory checks pass |
| `DIAGNOSTIC` | Benchmarks and sanitized checks | CPU/scheduler/memory/disk/clock/feed/API RTT and Docker overhead | Supported envelope or explicit lower-mode restriction |
| `SYNC` | Read-only state acquisition | Metadata/books/account/orders/fills freshness | Coherent snapshots |
| `RECONCILE` | Cancel/recovery only if needed | Journal/checkpoint versus exchange truth | No unresolved discrepancy |
| `SHADOW` | No live order effects | Same artifact/core, deterministic evidence, current schemas | PASS10 Shadow capability |
| `MICRO-LIVE` | Strictly bounded live effects | Risk limits, release channel, license, signer and capability manifest | Explicit human promotion |
| `LIVE` | Validated scope/size/mode only | Stable evidence and all runtime gates | Per-decision Risk authorization |

## Separate axes

`RunMode`, compiled support, configured enablement, license entitlement, release channel and `CapabilityManifest` validation are independent. The effective capability is their intersection plus current Risk/readiness. Therefore: license does not imply validated; enabled does not imply validated; compiled does not imply validated.

Unsupported infrastructure may remain eligible for Replay/Shadow while Micro-live/Live stays blocked. The installer never generates or uploads a private key, silently changes host security, or starts Live trading. Promotion is explicit and auditable; demotion is automatic when evidence becomes invalid.
