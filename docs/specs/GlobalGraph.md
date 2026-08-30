# GlobalGraph

## Purpose

Représenter toutes les AssetLocations et arêtes dirigées disponibles.
## Responsibilities

Build venue-aware, version, adjacency, reachability et invalidation.
## Non-responsibilities

Ne calcule pas EV/fill et n'active pas cross-venue.
## Inputs

Metadata snapshots.
## Outputs

Immutable GraphSnapshot et structural changes.
## Dependencies

MetadataEngine, PrecisionEngine.
## State

Nodes/edges/version avec single-writer build.
## Algorithms / formulas

Deux edges par market; graph traversal borné.
## Invariants

Edge side/base/quote/venue typés; no dangling route.
## Failure modes

Metadata conflict, duplicate edge, stale snapshot.
## Risk interactions

Graph inconsistency retire readiness.
## Performance requirements

Immutable read/ID lookup rapide; rebuild hors hot path.
## Metrics

Nodes/edges/connectivity/rebuild/invalidation latency.
## Persistence

Graph manifests/snapshots versionnés.
## Configuration

Venue/capability allowlist, pas asset intuition.
## Tests

Enumeration, direction/unit, metadata changes, reachability.
## Maturity requirement

M1 structural; M2 replay history.
## Open calibrated parameters

Aucun; future venue activation via ADR/capability.
