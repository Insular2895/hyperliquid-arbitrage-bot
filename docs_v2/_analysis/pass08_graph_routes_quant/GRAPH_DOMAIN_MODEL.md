# Graph Domain Model

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Type | Identity and meaning | Mutability/version | Producer | Consumers | Authority |
|---|---|---|---|---|---|
| `AssetId` | Stable asset identity; not a balance or location | Metadata-governed | metadata adapter | Graph, Route, Inventory | SRC-003; SRC-005 |
| `VenueId` | Stable venue identity | Metadata/config governed | adapter/config | Graph, Data, future XEX | SRC-003 |
| `GraphNode` / `AssetLocation` | `(VenueId, AssetId)` conversion endpoint | Added/removed through topology version | Graph Engine | Route, Capital reachability | SRC-003 lines 2048+ |
| `MarketId` | Stable venue-market identity with base and quote roles | Metadata-governed | metadata adapter | Book, Graph, Route | SRC-005 |
| `DirectedConversion` / `GraphEdge` | One executable input→output operation on one market | Structural identity stable; availability/metadata versioned | Graph Engine | Route Engine, NetConvert | SRC-003; SRC-004 QF-009/010 |
| `GraphVersion` | Identity of a complete point-in-time topology/metadata view | Monotonic immutable publication | Graph Engine | Route, Replay, DecisionTrace | SRC-005 Data closure |
| `DirectRoute` | One directed conversion from A to B | Rebuilt when dependency metadata changes | Route Engine | comparator/economics | SRC-004 QF-017 |
| `Route2Leg` | Ordered A→X→B directed conversions | Precomputed; direction and order part of identity | Route Engine | OWA/Bridge/economics | SRC-003/005 |
| `Cycle3Leg` | Ordered A→X→B→A closed route | Precomputed; start asset and order preserved | Route Engine | Triangle economics | SRC-004 QF-021–023 |
| `RouteId` | Stable identity over ordered directed legs and route family | Never derived from transient edge | Route Engine | `pair_to_routes`, traces | SRC-005 |
| `RouteVersion` | Version of a route definition and its structural dependencies | Changes on material route/metadata change | Route Engine | Opportunity, Replay, Risk | SRC-005 |
| `RouteDefinition` | Static route type, input/output, legs, dependencies and version | Immutable snapshot | Route Engine | Opportunity/Execution/Risk | SRC-005 lines 6118–6177 |
| `MarketState` / `BookState` | Current economic state, separate from topology | Per-market versioned publication | Book/Feature Engines | NetConvert, Risk | SRC-001; PASS06 |
| `Opportunity` | Ephemeral economic condition for a route, size and state | Expires/revalidates with state | Opportunity Engine | Participants, Simulator, Risk | SRC-005 |
| `AtlasVersion` | Point-in-time version of rolling learned/economic records | Immutable publication with model/dataset provenance | Atlas Engine | Activation, Capital, research | SRC-005 |

## Invariants

- A spot market creates **two** directed conversions, not one fungible edge.
- `BaseToQuote` means selling base into bids; `QuoteToBase` means buying base through asks.
- Topology says what can exist. Market state says what can execute now. Atlas says what has been economically interesting. HWC says where expensive computation is allocated.
- V1 activates same-venue Hyperliquid spot trade edges. Transfer/rebalance edges and cross-exchange execution are `FUTURE`; venue-aware identity prevents a later domain rewrite.
- Names above follow source concepts; exact serialized fields remain Data Contracts-owned and must not be invented here.
