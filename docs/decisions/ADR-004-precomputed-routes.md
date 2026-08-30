# ADR-004 — Precomputed 2/3-leg routes

## Context

Rechercher tous les cycles sur chaque update est coûteux et inutile.
## Decision

Pré-calculer direct/OWA/triangles et `market→affected routes`.
## Alternatives considered

Bellman-Ford/generic cycles; scan complet; routes codées manuellement.
## Why selected

Périmètre 2/3 spécialisé, testable et travail hot path borné.
## Consequences

Metadata changes invalident/rebuild; cycles 4+ hors core.
## Status

PROPOSED FOR REVIEW — LOCKED candidate.
## Sources

SRC-002/003.
