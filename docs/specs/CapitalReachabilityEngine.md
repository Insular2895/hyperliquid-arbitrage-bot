# CapitalReachabilityEngine

## Purpose

Déterminer quelles régions/routes sont atteignables et à quel coût.
## Responsibilities

Inventory graph, bridge paths, exit quality and HOT neighborhood inputs.
## Non-responsibilities

Ne déplace pas le capital et n'active pas cross-venue.
## Inputs

GlobalGraph, InventorySnapshot, NetConvert curves, atlas/risk.
## Outputs

ReachabilitySnapshot and candidate relocation paths.
## Dependencies

GlobalGraph, NetConvert, InventoryEngine, MarketAtlas.
## State

Versioned reachability by size/time.
## Algorithms / formulas

Path comparison through QF-068..072; capital-aware graph traversal.
## Invariants

Costs executable/size-dependent; unreachable not treated as zero cost.
## Failure modes

Stale path, hidden exit cost, combinatorial/path cycles.
## Risk interactions

Terminal viability and stranded risk; cannot bypass excluded asset.
## Performance requirements

Precompute/cache; bounded live lookup.
## Metrics

Reachable capacity/path costs/exit quality/update latency.
## Persistence

Snapshots and input versions.
## Configuration

Max path length, eligible assets/venues and refresh.
## Tests

No-path, alternative paths, size curves, metadata/inventory changes.
## Maturity requirement

M2 before Bridge/HOT capital policy.
## Open calibrated parameters

Path limits, refresh and viability thresholds.
