# ADR-017 — No Black-Scholes core

## Context

La stratégie active est routing spot, pas pricing d'options.
## Decision

Exclure Black-Scholes/Greeks/Heston/SABR et modèles voisins du core V1.
## Alternatives considered

Les inclure par anticipation; module générique quant.
## Why selected

Ils n'adressent aucune décision actuelle et augmentent surface/ambiguïté.
## Consequences

Extension options/perps future avec scope/formula book/ADR propres.
## Status

PROPOSED FOR REVIEW — REJECTED FOR CORE.
## Sources

SRC-004 D2.
