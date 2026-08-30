# ADR-003 — Replay equals Live core

## Context

Deux implémentations créeraient frais, rounding et risk divergents.
## Decision

LiveFeed et ReplayFeed émettent les mêmes contrats vers le même core.
## Alternatives considered

Backtest Python séparé; simulateur simplifié non contractuel.
## Why selected

Parité, reproductibilité et validation de la vraie logique.
## Consequences

Clock/RNG/transport injectés; no-lookahead et manifests obligatoires.
## Status

PROPOSED FOR REVIEW — LOCKED candidate.
## Sources

SRC-001/002, SRC-005 Data Contracts, SRC-006 Validation.
