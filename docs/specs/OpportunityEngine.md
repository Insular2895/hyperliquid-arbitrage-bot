# OpportunityEngine

## Purpose

Transformer routes affectées en opportunités comparables et auditées.
## Responsibilities

BBO filter, exact curves, OWA/triangle metrics, snapshot/reason logging.
## Non-responsibilities

Ne réserve pas et n'envoie pas d'ordre.
## Inputs

Book/fee/metadata snapshots, RouteCatalog, compute state.
## Outputs

OpportunitySnapshot ou typed reject observation.
## Dependencies

RouteEngine, NetConvert, MarketAtlas, QuantEngine.
## State

Ephemeral candidates plus immutable records.
## Algorithms / formulas

QF-017..027; direct/indirect intention équitable.
## Invariants

Même input/output/comparator; Edge(q), pas edge scalaire.
## Failure modes

Stale mixed snapshots, comparator mismatch, missed affected route.
## Risk interactions

Pré-risk seulement; hard invalid inputs rejetées.
## Performance requirements

Cheap filter first; exact work seulement candidates; bounded queue.
## Metrics

Funnel/update, candidates/routes, reject reasons, latency.
## Persistence

Toutes opportunités utiles, exécutées ou rejetées, avec versions.
## Configuration

BBO margin et grids versionnés/calibrés.
## Tests

Golden routes, stale/mixed snapshots, affected-route completeness.
## Maturity requirement

M2 replay; M3 shadow decision parity.
## Open calibrated parameters

BBO margin, recording sample policy, candidate grid.
