# `botctl` Command Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

The source-exact baseline commands are `status`, `health`, `benchmark`, `config validate`, `start`, `stop`, `reconcile`, `update check`, `update`, `rollback`, `support-bundle` and `emergency-stop`. The broader public vocabulary below normalizes mission-required aliases/workflows without claiming that every spelling was already frozen in SRC-006.

| Command | Purpose / effects | Confirmation / credentials | HALTED / no license | Audit, idempotence and redaction |
|---|---|---|---|---|
| `install` | Create/check directories, templates and runtime prerequisites; no Live start | Confirm host mutations; no Live key required | Yes / yes | Re-run converges; log paths/versions only |
| `preflight` | Read-only config, schema, secret-presence, host, clock, network and owner checks | No; validates but does not print secrets | Yes / yes | Stable reason codes; secret values omitted |
| `config validate` | Parse/normalize config and emit hash | No; no Live credentials unless exchange-scoped validation requested | Yes / yes | Idempotent; sanitized errors |
| `benchmark` / `diagnose` | CPU/scheduler/memory/disk/clock/feed/API/Docker diagnostics | Network tests may need explicit consent; trading key not required | Yes / yes | Versioned report; sensitive host fields redacted |
| `start` | Start process in non-ready startup sequence | Confirm Live intent separately; signer needed only for authenticated stages | After fault clearance / entitlement required only for new risk | Repeated start detects owner; never creates dual active |
| `stop --safe` / `stop` | Disable new risk, resolve/cancel, persist and stop | Confirm if exposure cannot be resolved | Yes / yes | Repeated stop is success; actions audited |
| `status` / `health` / `version` | Read state, readiness reasons, manifest/version | No; no Live credentials | Yes / yes | Read-only; client identifiers redacted in export |
| `logs` | View bounded local logs | Confirm broad/time-range export | Yes / yes | Never reveal secrets; read-only |
| `reconcile` | Compare orders, fills, balances and local state; may apply safe recovery | Confirm any material action | Yes / yes | Idempotent reducers and incident ID |
| `update check` | Discover metadata without activation | No | Yes / yes | Read-only and attributable |
| `update` | Verified risk-off/drain/backup/replace/reconcile workflow | Yes; registry credential, not signer unless reconciliation requires it | Yes / license not needed to reach safety | Transaction/state audit; repeated call resumes or reports terminal state |
| `rollback` | Activate known previous digest through safe workflow | Yes | Yes / yes for recovery | Never restores exchange truth from stale state |
| `risk-off` / `emergency-stop` | Emit global kill, block new risk and cancel/recover per policy | Emergency command should be explicit but immediately actionable | Yes / yes | Repeat-safe; highest-priority audit without secrets |
| `support-bundle` / `export-incident` | Build local sanitized diagnostic package | Explicit confirmation before external transfer | Yes / yes | Deterministic manifest; redaction checks fail closed |

## Exit-code classes

`0` success/safe terminal state; `2` invalid invocation/config; `3` precondition or readiness failure; `4` authentication/permission failure; `5` integrity/compatibility failure; `6` partial/recovery-required result; `7` internal failure. Exact numeric mapping is an `OPEN` CLI design until implementation freezes it, but machine-readable classes and stable reason codes are required.

Every state-changing invocation records actor/source, installation, command, correlation/incident ID, before/after state, artifact/config hashes and redacted result. No command prints or exports private material.
