# ADR-008 — No blind market orders

## Context

Un market sans limite peut convertir un edge faible en perte non bornée.
## Decision

Interdire market order aveugle et retry d'ordre aveugle.
## Alternatives considered

Market pour certitude; retry timeout; FOK/TWAP systématique.
## Why selected

Contrôle physique du prix et respect de l'état unknown.
## Consequences

Plus de rejects/partials possibles; recovery/reconciliation obligatoires.
## Status

PROPOSED FOR REVIEW — LOCKED candidate.
## Sources

SRC-001, SRC-004/005.
