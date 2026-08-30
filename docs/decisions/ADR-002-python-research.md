# ADR-002 — Python research

## Context

Calibration/statistiques demandent un écosystème analytique souple.
## Decision

Utiliser Python/Parquet/DuckDB pour research, training et rapports offline.
## Alternatives considered

Tout Rust; Python live; services ML distants.
## Why selected

Vitesse d'expérimentation sans dépendance synchrone live.
## Consequences

Artefacts versionnés/promus; golden parity aux frontières Rust/Python.
## Status

PROPOSED FOR REVIEW — LOCKED candidate.
## Sources

SRC-002, SRC-003, SRC-006/007.
