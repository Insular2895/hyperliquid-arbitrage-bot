# 10 — `botctl`, Diagnostics, Redaction and Incident Export

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Operator interface

`botctl` is the supported local operator surface. Source-exact commands are `status`, `health`, `benchmark`, `config validate`, `start`, `stop`, `reconcile`, `update check`, `update`, `rollback`, `support-bundle` and `emergency-stop`. Public workflow vocabulary additionally covers `install`, `preflight`, `diagnose`, `logs`, `stop --safe`, `risk-off`, `export-incident` and `version`; exact alias naming is frozen only by implementation/API review.

Every command contract defines purpose, reads/writes, Risk effect, confirmation, credential needs, availability while HALTED/unlicensed, stable exit/reason class, audit, redaction and idempotence. `start` never skips readiness; `stop --safe` resolves/persists; `update`/`rollback` run their state machines; `risk-off`/`emergency-stop` immediately removes new-risk permission.

## Audit

State-changing invocations record actor/source, installation, command, time, incident/correlation ID, before/after state, digest/config hash and sanitized result. Repeated safe-stop/risk-off is success; repeated install/preflight converges; repeated start fails safely if an owner exists. Secrets never appear in argv, output or audit.

## Diagnostic bundle

Allowed content includes artifact/schema/model versions, config hash and allowlisted sanitized config, host/runtime/clock/disk/network health, bounded recent logs, readiness reasons and incident IDs. Keys, seeds, API/registry/license tokens, environment dumps, memory/core dumps, raw journal/checkpoint and unnecessary raw orders/full balances/history are omitted.

The bundle is constructed locally, versioned, and accompanied by an inclusion manifest/hashes. Redaction combines field allowlists, denylist/token formats, entropy checks and canary-secret tests. Any hit fails closed. The client reviews and explicitly exports; creation does not transmit.

## Incident export

Incident export is scoped by time/incident and minimizes account/host identifiers through omission, aggregation, hashing or pseudonymization. Exceptional raw evidence uses a separate explicit client-controlled procedure. Support tooling may not widen telemetry consent or create remote-control authority.
