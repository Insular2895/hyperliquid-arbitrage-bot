# Validation, Property Tests and Failure Modes

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Mandatory properties

1. Base→Quote consumes bids; Quote→Base consumes asks.
2. Crossing a spread round trip is not free profit.
3. NetConvert never consumes unavailable/protected-out depth.
4. Route output equals sequential valid leg outputs.
5. OWA without valid direct comparator is rejected as OWA.
6. Triangle terminates in its exact starting asset.
7. One market update selects only dependent RouteIds.
8. Invalidating a market removes every affected active route.
9. Same metadata/version deterministically yields the same route/index set.
10. Same immutable state/formula/q yields the same route economics.
11. Larger q is recalculated against depth rather than linearly extrapolated.
12. Every economic result records leg/comparator book versions.
13. Historical Replay uses historical topology/Atlas only.

## Test layers

Unit tests cover identity/direction/continuity/classification/minimums and reason codes. Property tests cover reversal, closure, determinism, dependency symmetry, monotonic consumed depth and no output from absent depth. Formula golden datasets cover QF-007–027. Replay validates event/order/version determinism. Shadow compares detected/predicted outcomes without orders. Micro-live validates mechanics and fills only after Risk/operations authorization.

Rust/Python parity is exact under the numeric contract for conversion and formula golden vectors. Fuzzing targets malformed metadata/books, duplicate levels, boundaries, overflows, min/rounding discontinuities and stale publications.

## Failure modes

Wrong market side, symbol ambiguity, missing comparator, open cycle mislabeled Triangle, fee double debit, gross output forwarded, precision/minimum violation, stale/mixed leg, reverse-index omission, route leak after delisting, Atlas lookahead, COLD blindness, score overriding Risk and QF-027/QF-076 confusion are release-blocking semantic failures.

Acceptance requires zero unexplained golden/parity difference, zero active reference to invalid topology, explicit unknown/failure outputs, deterministic Replay hashes and complete version provenance. Numeric performance thresholds are calibrated separately.
