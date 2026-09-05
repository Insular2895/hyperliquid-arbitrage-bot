# `pair_to_routes` Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Contract

- **Key:** canonical `MarketId`; the historical name `pair_to_routes` does not permit symbol-string ambiguity.
- **Value:** deterministic bounded collection of stable `RouteId` values whose current `RouteDefinition` consumes that market, whether as direct comparator or executable leg.
- **Generation:** derived from a published route set after topology validation; duplicate membership is forbidden.
- **Update:** metadata changes replace affected entries atomically with the new `GraphVersion`/`RouteVersion` publication.
- **Invalidation:** a route is removed from active evaluation for every dependency before the invalid definition can be selected.
- **Ownership:** Route Engine is single logical writer; workers read an immutable snapshot/generation. Exact concurrency mechanism remains implementation detail.

## Event path

`BookUpdate(MarketId, BookVersion) → pair_to_routes[MarketId] → affected RouteId values only → BBO prefilter → exact evaluation for survivors`.

The lookup must not trigger a graph-wide scan or generate routes. A route dependent on three markets is registered under all three. The direct comparator is also a dependency for OWA, even though it is not an indirect execution leg.

## Determinism and staleness

Given the same eligible metadata, ordering rules and GraphVersion, route generation and reverse-index membership are identical. Each worker result carries index generation, route version and consumed book versions. A result returned against superseded dependencies is discarded or revalidated through PASS06; it is never committed blindly.

## Invariants

One market update cannot select a route absent from that market's dependency set. Removing a market leaves no active route dependent on it. Reverse and forward dependency maps agree. Historical Replay uses the index that was derivable at event time, not today's route universe.
