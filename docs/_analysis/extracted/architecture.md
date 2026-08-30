# Extraction — architecture et hot path

## Sources

- SRC-001 et SRC-002 pour l'historique architectural.
- SRC-004 à SRC-006 priment pour exécution, formules, risque, données,
  validation et déploiement.

## Architecture retenue

- Core de production et replay en Rust; Python reste hors hot path pour la
  recherche et la calibration. C++ n'est pas prévu par défaut.
- `FeedAdapter → BookEngine → features → GlobalGraph/RouteEngine →
  OpportunityEngine → forecasts → simulation → sizing/portfolio → RiskEngine
  → ExecutionCoordinator`.
- Le graphe est orienté, venue-aware et pré-calcule les routes 2/3 jambes. Une
  update ne recalcule que ses routes dépendantes.
- HOT/WARM/COLD contrôle le coût du calcul live. Le Global Watcher observe
  l'univers; CapitalReachability concentre le calcul cher près du capital.
- Aucune I/O, lookup distant, allocation non bornée ou analyse lourde dans le
  hot path. Les états nécessaires sont maintenus en mémoire.
- Lock-free, zero-copy et pinning CPU sont des optimisations guidées par profil,
  pas des prérequis universels.

## Statuts

- Architecture finale progressive : **LOCKED**.
- Rust live/replay et Python research : **LOCKED**.
- Pré-calcul 2/3 legs, routes affectées seulement : **LOCKED**.
- HOT/WARM/COLD et Global Watcher : **LOCKED**; seuils : **CALIBRATED**.
- Node local, C++, lock-free généralisé, GPU/FPGA hot path : **FUTURE/REJECTED**
  jusqu'à preuve de ROI ou benchmark.
