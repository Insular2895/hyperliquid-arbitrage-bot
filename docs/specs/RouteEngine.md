# RouteEngine

## Purpose

Pré-calculer direct, OWA, triangles, bridges et leurs dépendances.
## Responsibilities

Enumeration 2/3 legs, comparator, market→routes et versioning.
## Non-responsibilities

Ne price pas une taille et ne sélectionne pas le capital.
## Inputs

GraphSnapshot, capability rules.
## Outputs

RouteCatalog, RouteDependencies, invalidations.
## Dependencies

GlobalGraph.
## State

Immutable catalog/version et activation labels séparés.
## Algorithms / formulas

Paths `A-X-B` avec direct `A-B`; cycles `A-X-B-A`; no 4+ core.
## Invariants

Sans direct jamais OWA; no duplicated equivalent route; venue explicit.
## Failure modes

Combinatorial explosion, stale dependency, wrong comparator.
## Risk interactions

Invalid route/version = reject.
## Performance requirements

Precompute/rebuild off-path; affected-route lookup borné.
## Metrics

Route counts/type, dependency fanout, rebuild/lookup latency.
## Persistence

Catalog manifest/version.
## Configuration

Max leg/type capability locked; activation elsewhere.
## Tests

Graph fixtures, exhaustive small graphs, metadata invalidation.
## Maturity requirement

M1 enumeration; M2 replay affected-route coverage.
## Open calibrated parameters

Compute policy not route validity.
