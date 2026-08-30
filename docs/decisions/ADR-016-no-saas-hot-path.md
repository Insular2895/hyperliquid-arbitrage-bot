# ADR-016 — No SaaS hot-path dependency

## Context

Licence/dashboard/registry distant peuvent tomber ou ajouter latence.
## Decision

Le chemin critique reste Client VPS↔Hyperliquid; contrôles commerciaux async/local.
## Alternatives considered

Licence par trade, decision API central, shared execution service.
## Why selected

Disponibilité, latence, autonomie client et recovery sûre.
## Consequences

Entitlements signés/grace; recovery/reconcile toujours disponibles.
## Status

PROPOSED FOR REVIEW — LOCKED candidate.
## Sources

SRC-006 D5.
