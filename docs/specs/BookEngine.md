# BookEngine

## Purpose

Maintenir des carnets locaux valides point-in-time.
## Responsibilities

Snapshot/update, séquence, resync, freshness, immutable publication.
## Non-responsibilities

Ne calcule pas opportunité, fee ou fill.
## Inputs

BookSnapshot/BookUpdate, Clock, metadata.
## Outputs

BookState versionné et BookHealth.
## Dependencies

FeedAdapter, Normalizer, MetadataEngine.
## State

Single-writer levels, sequence, timestamps, validity.
## Algorithms / formulas

BBO, QF-001..006; structure de niveaux déterministe.
## Invariants

Bid<Ask, quantités valides, gap invalide, stale interdit au trading.
## Failure modes

Gap, reorder, crossed book, resync loop, memory/backpressure.
## Risk interactions

Book invalid/stale est hard gate.
## Performance requirements

Update/lookup bornés; snapshots readers immuables.
## Metrics

Update latency, age, gaps, invalid/resync count, depth.
## Persistence

Events et checkpoints; pas de mutation historique.
## Configuration

Depth/freshness/resync policy versionnées.
## Tests

Golden reconstruction, property ordering, gaps, crash/load.
## Maturity requirement

M2 replay puis M3 live stable.
## Open calibrated parameters

Freshness threshold, depth retained, checkpoint cadence.
