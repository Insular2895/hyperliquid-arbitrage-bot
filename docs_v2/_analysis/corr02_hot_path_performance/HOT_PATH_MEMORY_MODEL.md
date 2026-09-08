# Hot-Path Memory Model

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

| Lifetime | Examples | Allocation expectation | Identity rule |
|---|---|---|---|
| topology/static | canonical metadata, route definitions, reverse index | allocate/rebuild on validated topology publication | canonical IDs + generation |
| run | resolved config, formula/model tables, queues, pools | allocate at startup/warm-up | RunManifest-linked |
| market mutable | book levels, BBO, feature windows | bounded stable storage where measured useful | MarketId + BookVersion |
| event | normalization/evaluation context | borrow/reuse scratch where safe | EventId/recorder order |
| opportunity | exact route result/candidate | compact typed value; evidence retained | OpportunityId + input tuple |
| execution | reservation/plan/order/fill state | safety-owned durable objects | Execution/Cloid/Oid/Fill IDs |

Topology updates may allocate and publish a new immutable generation; they must not mutate storage observed by old readers. Hot lookups avoid repeated symbol strings where dense/canonical ID lookup suffices, while diagnostic/serialization layers retain human-resolvable canonical identity.

AoS, SoA, flat arrays, arenas, inline collections and borrowing are benchmark candidates. Lifetime clarity, deterministic ordering and safe reclamation precede locality gains.

“Zero allocation” and “zero copy” are steady-state objectives, not constitutional invariants. A required copy for ownership, immutability, audit or async lifetime safety is valid and must be measured rather than deleted blindly.
