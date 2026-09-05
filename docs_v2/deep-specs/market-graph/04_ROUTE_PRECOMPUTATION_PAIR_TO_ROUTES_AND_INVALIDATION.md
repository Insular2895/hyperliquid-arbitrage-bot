# Route Precomputation, `pair_to_routes` and Invalidation

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Generation

On a GraphVersion/metadata change, Route Engine deterministically enumerates supported DirectRoute, Route2Leg and closed Cycle3Leg definitions and valid direct-comparator relationships. Legal ordered direction, asset continuity, duplicate/cycle rules and V1 venue scope come from source-owned policies. Invariant topology is never rebuilt per book tick.

RouteId incorporates family and ordered directed structure; RouteVersion changes with a material definition/dependency change. A RouteDefinition lists legs and dependencies. Profit, size and HWC are not identity inputs.

## Reverse dependency index

`pair_to_routes: MarketId → bounded RouteId collection` includes every executable leg and an OWA comparator dependency. A book update obtains only dependent routes. The forward definitions and reverse index are published atomically and agree bidirectionally.

## Invalidation

Market add/remove/status, base/quote mapping, precision, minimums or material metadata changes trigger affected regeneration. Fee changes invalidate cached economics. Removed/unhealthy dependencies deactivate routes before selection. Old versions remain for audit/Replay.

## Concurrency and stale work

Route Engine is the single logical writer and publishes immutable generations. Workers record generation, GraphVersion, RouteVersion and BookVersions. A returned result whose dependency state moved is discarded or explicitly revalidated; there is no blind commit.

## Hot-path prohibition

No Dijkstra, arbitrary path search, graph-wide scan or blocking service call belongs in opportunity detection. General routing can exist offline for Bridge research/future families. See [generation matrix](../../_analysis/pass08_graph_routes_quant/ROUTE_GENERATION_AND_INVALIDATION_MATRIX.md) and [`pair_to_routes`](../../_analysis/pass08_graph_routes_quant/PAIR_TO_ROUTES_CONTRACT.md).
