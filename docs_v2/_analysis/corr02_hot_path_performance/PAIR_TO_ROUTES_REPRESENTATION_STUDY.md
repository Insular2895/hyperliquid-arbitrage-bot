# `pair_to_routes` Representation Study

DOCUMENTATION STATUS: CANDIDATES — AWAITING FINAL HUMAN REVIEW

The logical contract remains `MarketId → deterministic bounded dependent RouteId values`, including OWA comparator dependencies, with no duplicate and no graph-wide tick search.

| Candidate | Expected property | Main risk | Required comparison |
|---|---|---|---|
| `HashMap<MarketId, Vec<RouteId>>` | simple canonical-ID lookup | hashing/pointer chasing | baseline |
| dense `Vec<Vec<RouteIndex>>` | direct indexed access | per-vector allocation/locality; generation coupling | realistic degree and topology churn |
| CSR-like offsets + flat route indices | contiguous bounded scan | rebuild complexity; offset correctness | lookup tails, memory and rebuild cost |
| small-inline collection per market | avoids heap for common degree | overflow branch and dependency/tool choice | real degree distribution |
| flat indices + separate activation bitset | compact scan and reversible HWC | stale mask/generation mix | parity under activation churn |

All candidates preserve deterministic canonical route order, forward/reverse agreement, comparator membership, atomic generation publication, topology invalidation and point-in-time Replay. The chosen structure is an empirical implementation decision, not a documentation assumption.

Benchmark with real/synthetic distributions for market count, routes per market, comparator/triangle mix, HOT/WARM/COLD activation, update burst, rebuild frequency and memory footprint. Hash function substitution is not assumed necessary; dense mapping may remove hashing from the lookup entirely.
