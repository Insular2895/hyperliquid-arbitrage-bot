# Point-in-Time Replay, Versioning and Data Contracts

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Required versions

| Version | What it identifies |
|---|---|
| GraphVersion | eligible nodes/edges/topology publication |
| RouteVersion | ordered definition/dependency publication |
| AtlasVersion | rolling evidence publication available by T |
| MetadataVersion | market roles, precision, minimums and status |
| BookVersion(s) | exact leg/comparator states consumed |
| FeeVersion | point-in-time fee state |
| FormulaVersion | QF semantics |
| ModelVersion | learned forecasts/Atlas producers |
| Dataset/RunManifest | event set, code/config/provenance |

## Historical reconstruction

Replay at T discovers only markets/listings and metadata known at T, generates the route set deterministically for that GraphVersion, consumes Atlas observations available by T and applies historical books/fees/formulas/models. Today's market universe or later learned aggregate is lookahead contamination.

## Coherent route state

The route snapshot records every required leg/comparator BookVersion, times and freshness. Required-leg freshness exposes the worst/oldest leg under Risk's canonical policy. Mixing states is allowed only under an explicit snapshot/skew contract recorded in DecisionTrace; a future leg can never be paired silently with an earlier decision state.

## Publication/staleness

Graph, routes and Atlas publish immutable generations. Worker results carry consumed generations. If book, metadata, fee, route or risk-critical versions advance beyond allowed TTL/skew, the result is discarded or revalidated before decision/send.

## Determinism

Same RunManifest, metadata/event order, graph generator, versions, q and formulas reproduce topology, reverse indexes and route economics. Checkpoint restore cannot combine incompatible schema/version state. Data Contracts/Recorder Replay remain authoritative for serialization, ordering, clocks, hashes and compatibility.
