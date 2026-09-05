# Directed Conversion Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Direction | Input | Output | Exchange action | Consumed side | Formula reference |
|---|---|---|---|---|---|
| `BaseToQuote` | base units | quote units | sell base | bids, best to worse | QF-009 |
| `QuoteToBase` | quote units | base units | buy base | asks, best to worse | QF-010 |

The two operations are asymmetric. Inverting a price, multiplying midpoint, or reusing the opposite walk is invalid.

## Required inputs

The conversion is bound to `MarketId`, `VenueId`, explicit input/output assets, exact input amount and unit, directed side, immutable L2 `BookSnapshot` plus book version/freshness, fee state/version, market metadata/version, execution mode and protected price/validity context. Current Hyperliquid field names and exchange limits require external revalidation.

## Processing contract

1. Resolve the unique market and direction; reject ambiguity or an unavailable market.
2. Quantize size and validate price under QF-007/QF-008 using the point-in-time metadata.
3. Walk only the correct side under QF-009 or QF-010. Never consume unavailable depth.
4. Produce filled input, gross output, unfilled input, VWAP and level-consumption evidence.
5. Resolve dynamic fee rate under QF-014 and fee amount under QF-015, including the debit/output asset semantics.
6. Apply the locked QF-016 `NetConvert` contract once; do not subtract costs again downstream.
7. Validate minimum quantity/notional, output quantization and the next leg's usable input. Dust/shortfall remains explicit.

## Reject/error states

`UNKNOWN_MARKET`, `WRONG_DIRECTION`, `MARKET_UNAVAILABLE`, `BOOK_STALE`, `BOOK_INVALID`, `INSUFFICIENT_DEPTH`, `INVALID_SIZE`, `INVALID_PRICE`, `MINIMUM_VIOLATION`, `FEE_UNKNOWN`, `METADATA_MISMATCH`, and `VERSION_MISMATCH` are semantic families, not a final enum declaration. Any unknown material input fails closed. Partial executable output is not silently promoted into full route output.

## Output and provenance

The result carries output amount/unit, fill completeness, residual/dust, gross and economic outputs, fee evidence, VWAP/levels, market/book/metadata/fee/formula versions and deterministic reason. A route feeds the **actual valid output** of leg *n* into leg *n+1*.

## Illustrative source example

For `HYPE → USDC`, the base asset is sold through bids. For `USDC → HYPE`, asks are consumed. The example clarifies direction only; symbols, prices and quantities are not configuration or golden vectors.
