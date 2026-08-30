# ADR-018 — Docker client distribution

## Context

Des installations clientes doivent être reproductibles, isolées et rollbackables.
## Decision

Distribuer une image OCI signée/digest-pinned avec runtime Docker/Compose durci.
## Alternatives considered

Binaire copié manuellement; Kubernetes; install source; SaaS central.
## Why selected

Packaging uniforme, update/rollback et volumes/state séparés.
## Consequences

Supply-chain controls, non-root/no socket, networking/overhead benchmarkés.
## Status

PROPOSED FOR REVIEW — LOCKED packaging, runtime details OPEN.
## Sources

SRC-006 D5.
