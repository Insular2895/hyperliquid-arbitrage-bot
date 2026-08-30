# MetadataEngine

## Purpose

Fournir la vérité point-in-time des marchés et règles exchange.
## Responsibilities

Découverte, versioning, historical lookup et invalidation dépendante.
## Non-responsibilities

Ne hardcode pas frais/précision et ne construit pas les routes seul.
## Inputs

Official metadata responses/events, Clock.
## Outputs

MarketMetadataSnapshot et MetadataChanged.
## Dependencies

FeedAdapter/transport bootstrap, Recorder.
## State

Versions effectives par venue/market.
## Algorithms / formulas

Diff structurel et dependency invalidation.
## Invariants

Unknown/stale required metadata interdit nouvelle exécution.
## Failure modes

Schema drift, market delist, conflicting effective time.
## Risk interactions

Déclenche rebuild/risk-off des objets affectés.
## Performance requirements

Lookup mémoire O(1)-like; refresh hors hot path.
## Metrics

Age, changes, lookup misses, invalidations.
## Persistence

Snapshots/events historiques checksummés.
## Configuration

Refresh/source policy; aucune règle externe non vérifiée.
## Tests

Changes, delist, history replay, invalidation, unknown version.
## Maturity requirement

M1 avec règles officielles revalidées; M2 historical.
## Open calibrated parameters

Refresh cadence et propagation grace.
