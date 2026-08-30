# ADR-010 — Recovery first-class

## Context

Les jambes ne sont pas atomiques; partial/unknown créent exposition réelle.
## Decision

Recovery et Reconciliation sont des modules/états de premier rang.
## Alternatives considered

Rollback fictif; continuer route; liquidation unique forcée.
## Why selected

Optimiser depuis l'état courant réduit les pertes et rend restart sûr.
## Consequences

Réserves, multi-route/split recovery, failure tests et permissions dédiées.
## Status

PROPOSED FOR REVIEW — LOCKED candidate.
## Sources

SRC-003/004/005.
