# Directed Conversion Edges and NetConvert

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Two operations per market

| Conversion | Action/side | Units |
|---|---|---|
| Base→Quote | sell base into bids | base input → quote output |
| Quote→Base | buy base through asks | quote input → base output |

The direction is part of edge and RouteId identity. A reciprocal price is not a reciprocal executable conversion.

## Edge contract

A directed edge resolves MarketId/VenueId, input and output AssetId, `BaseToQuote`/`QuoteToBase`, current market availability, precision/minimum metadata and the appropriate book side. Structural identity is separated from current BookSnapshot and FeeState.

## Exact evaluation

QF-009 and QF-010 walk only available protected L2. QF-007/008 validate sizes/prices; QF-011–013 expose walk/VWAP/slippage; QF-014/015 resolve fee rate/value; QF-016 returns the one economic output. The route cannot apply spread, slippage or fees a second time.

Inputs and outputs retain asset units. The valid output after fees/rounding becomes the next leg's input. If it violates the next minimum or depth is insufficient, full route economics are invalid for that `q`; residual/dust remains explicit.

## Failure and provenance

Wrong side, stale/invalid book, unknown fee, metadata mismatch, unsupported mode, invalid precision/minimum or insufficient protected depth fails closed. The result records book, metadata, fee, formula and graph/route versions plus consumed levels.

Same accepted immutable inputs must be deterministic and Rust/Python-equivalent under the canonical numeric contract. See [`NETCONVERT_CONTRACT.md`](../../_analysis/pass08_graph_routes_quant/NETCONVERT_CONTRACT.md).
