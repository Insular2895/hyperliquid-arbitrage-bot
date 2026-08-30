# ADR-005 — HOT/WARM/COLD

## Context

Le système doit connaître tout l'univers sans calcul L2/modèles partout.
## Decision

Classifier le compute live HOT/WARM/COLD avec Global Watcher et hystérésis.
## Alternatives considered

Tout calculer; whitelist/top-K statique; ignorer les régions froides.
## Why selected

Conserve la couverture tout en bornant le hot path.
## Consequences

Policy/calibration requise; ne réduit pas arbitrairement l'enregistrement R&D.
## Status

PROPOSED FOR REVIEW — structure LOCKED, thresholds CALIBRATED.
## Sources

SRC-001/002/003.
