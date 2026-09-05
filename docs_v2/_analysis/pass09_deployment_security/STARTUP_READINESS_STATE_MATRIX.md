# Startup / Readiness State Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Automatic restart is process supervision, not authorization to trade. Every boot starts without new-risk permission.

| State | Required evidence | New risk | Safe actions | Exit condition |
|---|---|---:|---|---|
| `BOOTING` | Verified artifact; single-owner lock; writable-volume check | No | Diagnose, stop | Runtime and schemas load |
| `CONFIGURING` | Config parsed, normalized, schema-compatible; `config_hash` emitted | No | Diagnose, correct config | Valid ResolvedConfig |
| `CLOCK_CHECK` | Host clock health and uncertainty within supported envelope | No | Observe, stop | Clock evidence accepted |
| `CONNECTING` | Required feed/API/account connections authenticated | No | Reconnect, diagnose | Sources reachable |
| `SYNCING` | Metadata, books, account, orders and fills reach coherent snapshots | No | Read/query/cancel if safe | Current state available |
| `RECONCILING` | Orders → fills → balances/inventory compared to journal/checkpoint | No | Cancel, reduce, Recovery | No unresolved material discrepancy |
| `RISK_CHECK` | Risk health, reservations, limits, capability and license evaluated | No | Risk reduction | Risk says eligible |
| `READY` | All required evidence fresh and compatible | Risk-gated | All licensed/validated actions | Material invalidation |
| `DEGRADED` | Process healthy but one or more new-risk gates unavailable | No by default | Cancel/reconcile/reduce | Evidence restored and full recheck |
| `RECOVERY_ONLY` | Exposure exists while ordinary capability unavailable | No | Cancel, reconcile, bounded Recovery | Exposure resolved and full startup cycle |
| `HALTED` | Unsafe/unknown state, crash loop or operator halt | No | Diagnose; explicitly safe reads/actions | Human-cleared cause plus full cycle |

## Health separation

- **Liveness:** the process can make progress; it is not a trading permission.
- **Readiness:** the engine can accept new-risk consideration; Risk still authorizes each action.
- **Trading health:** `READY`, `DEGRADED`, `RECOVERY_ONLY` or `HALTED` describes the safe action envelope.

A container health probe must not restart a process that is usefully reconciling or reducing exposure. Invalid config, incompatible state, missing signer, unhealthy clock, ambiguous ownership, unresolved reconciliation or unsupported capability blocks `READY` with a stable reason code.
