# Route Index and Work Deduplication

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

`pair_to_routes` remains the canonical logical reverse dependency: canonical `MarketId` maps to a deterministic bounded collection of every dependent canonical `RouteId`, including an OWA direct comparator. No physical representation may omit, duplicate or reorder membership nondeterministically.

HashMap+Vec, dense nested arrays, CSR-like flat offsets, small-inline collections and separate activation masks are benchmark candidates. A dense runtime index is a location inside one immutable `GraphVersion`/index generation, not persistent identity. Mapping is deterministic and round-trippable; width is checked; telemetry/evidence retains canonical IDs; old generations cannot interpret new indices.

Work is duplicate only when its complete economic input tuple is equal: route/version, ordered relevant books, fee, metadata, graph/index, formula, q, execution/protection context and every consumed feature/model/config version. Equality is collision-safe. Distinct ordered states remain distinct even if their prices or fingerprint match.

Dirty generations/cancellation may stop work already proven stale, but a Boolean flag cannot silently collapse dirty→processed→dirty. Default cross-event coalescing is forbidden. Any future coalescing/scheduling policy is an intentional versioned semantic change requiring human review, Replay/Shadow and capture/economic evidence.

Validation covers forward/reverse equality, comparator inclusion, deterministic order, topology invalidation, dense/canonical round-trip, exact tuple duplicate suppression and preservation of every distinct ordered input. See the [representation study](../../_analysis/corr02_hot_path_performance/PAIR_TO_ROUTES_REPRESENTATION_STUDY.md), [dense ID contract](../../_analysis/corr02_hot_path_performance/DENSE_RUNTIME_ID_CONTRACT.md) and [dedup contract](../../_analysis/corr02_hot_path_performance/ROUTE_WORK_DEDUPLICATION_CONTRACT.md).
