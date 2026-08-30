# ADR-009 — Protected IOC / ALO

## Context

Taker exige vitesse avec prix maximal/minimal; maker doit rester post-only.
## Decision

Protected IOC limit pour taker; ALO/Post Only pour maker.
## Alternatives considered

Market, FOK exclusif, ordinary limit, TWAP.
## Why selected

Prix borné, non-resting taker et absence de taker accidentel maker.
## Consequences

Partials sont normaux; exact support exchange doit être revalidé.
## Status

PROPOSED FOR REVIEW — LOCKED architecture / external rule verify.
## Sources

SRC-001, SRC-004 D1.
