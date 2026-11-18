# Route Generation and Invalidation Matrix

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

| Family | Generation condition | Metadata dependencies | Precomputed | Hot-path generation | Invalidation/version | `pair_to_routes` | Replay |
|---|---|---|---:|---:|---|---|---|
| Direct | one valid directed conversion A→B | venue, market, base/quote, status, precision | Yes | No | any material dependency change publishes new route/graph version | registered under its market | reconstruct from metadata at T |
| Route2Leg | compatible A→X and X→B; legal ordered legs | both markets/assets/directions and constraints | Yes | No | either leg/asset/metadata change | registered under both markets | deterministic set for GraphVersion T |
| OWA candidate | Route2Leg plus valid Direct A→B comparator | indirect legs plus comparator and classification | Yes | No | any of three markets; comparator availability can remove OWA class | registered under all dependent markets | comparator/version at T |
| Cycle3Leg | A→X→B→A exact asset closure | three directed markets and legal ordering | Yes | No | any leg/asset/metadata change | registered under all three markets | deterministic set for GraphVersion T |
| Bridge candidate | structurally valid path exposed to PASS07 | route topology; dynamic Capital decision separate | supported fixed families precomputed | no generic search | topology invalidation; economic activation reversible | all constituent markets | point-in-time route plus Atlas/Capital state |
| Recovery path | bounded safe exits from current exposure | current graph/capability; owned by Recovery | supported paths may be prepared | no unbounded search in opportunity path | current market/capability change | affected markets | recovered from historical state |
| Cross-exchange | future venue/transfer topology | venue, transfer and trade metadata | Future | Disabled V1 | future governed contract | future | future |

## Update protocol

`MetadataUpdate → validate affected metadata → build affected Graph edges, route definitions and reverse-index entries off to the side → validate one coherent immutable generation → atomically publish the compatible GraphVersion + RouteDefinitionVersion + reverse-index generation → retire/deactivate superseded definitions for new readers`. Publication is one reader-visible generation boundary, not a sequence in which a new Graph can be paired with old routes or indexes. Readers already holding the previous immutable generation may finish against it; new work acquires the published generation. A worker result tagged with an older incompatible generation is rejected or explicitly recomputed.

Fee changes invalidate economic caches and force re-evaluation; they need not change structural identity unless the route definition embeds material fee context. Historical route definitions remain retained for Replay. This protocol is an in-process immutable publication contract and does not introduce a distributed transaction system.

Structural generation never asks whether the edge is profitable now. A structurally valid route can be inactive; an active route can stop producing opportunities; an `Opportunity` never becomes a `RouteDefinition`.
