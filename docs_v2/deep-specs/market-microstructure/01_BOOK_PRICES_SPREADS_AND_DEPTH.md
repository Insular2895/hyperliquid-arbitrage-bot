# Book Prices, Spreads and Depth

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Formula references

QF-001 Mid Price, QF-002 Absolute Spread, QF-003 Relative Spread, QF-004 Cumulative Base Depth, QF-005 Cumulative Quote Depth and QF-006 Depth Within Price Band are locked in SRC-004. This specification does not restate their equations.

## Input contract

A valid canonical BookSnapshot supplies ordered bid/ask levels, exact price and base-size units, MarketId/base/quote roles, source quality, exchange/receive times and BookVersion. MetadataVersion identifies precision and market status. Empty, crossed, stale, gapped or unit-ambiguous books are invalid/unknown under PASS06/Risk policy.

## Semantics

Mid is descriptive, never executable. Absolute spread uses price units; relative spread is dimensionless/bps under its canonical reference. Base depth and quote/notional depth are distinct. Band depth states side, reference price, band and resulting unit. Values from different side, K, bands, books or time windows cannot be compared as if identical.

## Runtime

BBO and bounded depth aggregates update incrementally from accepted book publications. Deep or arbitrary band queries can use precomputed cumulative structures but must remain bounded for hot-path use. Atlas stores time-windowed aggregates with provenance, not a replacement BookState.

## Validation

Golden cases cover one/multiple levels, empty side, crossed/invalid book, unit transformations and boundary inclusion. Incremental results must equal offline batch reference and Rust/Python parity. No numeric K/band threshold is locked here.
