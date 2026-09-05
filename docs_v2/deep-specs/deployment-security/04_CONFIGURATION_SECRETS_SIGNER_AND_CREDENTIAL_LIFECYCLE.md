# 04 — Configuration, Secrets, Signer and Credential Lifecycle

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Configuration

`bot.toml`, `risk.toml` and `markets.toml` are conceptual external inputs, not hard-coded filenames promised by implementation. Parsing creates one immutable normalized `ResolvedConfig` and `config_hash`. Validation covers types, ranges, cross-field invariants, constitutional Risk floors and schema compatibility. A failure blocks READY.

Schema evolution is explicit. Migration must name input/output versions, semantic changes, backup, rollback impact and audit result. Unknown fields/versions are never silently reinterpreted. Client policy may tighten constitutional limits, never relax them.

## Secret boundary

The preferred input is a client-owned read-only secret file under `/run/secrets` or an equivalent safe runtime secret mechanism. Secret values are forbidden from image/layers, ordinary config, CLI parameters, environment/log dumps, state serialization, metrics, diagnostics, telemetry and vendor systems.

The signer has minimum order/account permissions and no withdrawal authority. Registry credentials are pull-only. License material is distinct from the exchange signer. Panic/error paths redact sensitive fields; core dumps are disabled or strongly protected and never enter ordinary support export.

## Lifecycle state machine

```text
PROVISION_LOCAL -> SCOPE_CHECK -> MOUNT_READ_ONLY -> AUTHENTICATE
                -> IN_USE -> RISK_OFF -> ROTATE -> REVALIDATE
                -> RECONCILE -> REVOKE_OLD
```

Rotation does not create two active signers/processes. Stop new risk, reconcile and stabilize ownership before replacement. After change, validate permissions/authentication and reconcile again before READY; revoke the old credential after the safe handoff. Suspected leakage skips to risk-off, cancel/reconcile and incident response.

## Evidence

Tests scan images, process invocation/environment, logs, panics and diagnostic bundles with canary secrets. Audit records secret identity/version or fingerprint only where needed—never the material itself. Memory zeroization is used where practical, with its limitations documented.
