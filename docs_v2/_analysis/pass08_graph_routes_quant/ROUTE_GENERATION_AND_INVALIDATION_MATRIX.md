# Route Generation and Invalidation Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

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

`MetadataUpdate → validate affected metadata → publish new GraphVersion → regenerate only affected edges/routes → rebuild affected reverse-index entries → publish RouteVersion(s) → deactivate invalid definitions`. Fee changes invalidate economic caches and force re-evaluation; they need not change structural identity unless the route definition embeds material fee context. Historical route definitions remain retained for Replay.

Structural generation never asks whether the edge is profitable now. A structurally valid route can be inactive; an active route can stop producing opportunities; an `Opportunity` never becomes a `RouteDefinition`.
