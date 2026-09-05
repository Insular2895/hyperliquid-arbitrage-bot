# Structural Graph, Venues, Assets and Markets

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Contract

The Global/Market Graph is a point-in-time catalogue of eligible conversion topology. A node is an `AssetLocation` identified by `(VenueId, AssetId)`. A `MarketId` declares venue, base and quote roles. Each market produces two directed trade edges when status and metadata are valid.

The graph contains no current profitability, capital balance, inventory band, model forecast or Risk permission. Those are consumers or parallel state. A node existing does not make it HOT; capital moving does not create topology.

## Metadata build

1. Ingest metadata through the canonical Data adapter.
2. Validate identity, base/quote roles, precision/minimum rules and status.
3. Diff against the current immutable graph.
4. Add/remove/update affected nodes and directed edges.
5. Regenerate dependent route definitions/reverse indexes.
6. Publish one internally consistent GraphVersion and change events.

Unknown or contradictory material metadata makes affected conversions unavailable. New markets become globally known but require evidence before expensive activation. Removal disables current routes while preserving historical topology/Atlas records.

## Version boundaries

GraphVersion identifies topology publication; MetadataVersion identifies its exchange rules; BookVersion identifies dynamic market state; AtlasVersion identifies learned aggregates. These are never collapsed. Replay reconstructs all identities as-of T.

## Venue boundary

The schema is venue-aware. V1 enables same-venue Hyperliquid spot trade edges only. Future venue nodes and transfer/rebalance edges require settlement, latency, outage, security, inventory and accounting contracts before activation. Representability is not capability.

## Invariants

- base/quote roles and conversion direction are unambiguous;
- stable IDs never rely solely on display symbols;
- equal assets at different venues are distinct nodes;
- identical metadata plus deterministic ordering yields identical topology;
- a book event never silently changes topology.

Authority: SRC-003 venue-aware closure; SRC-005 version/data closure; current exchange schema in external register.
