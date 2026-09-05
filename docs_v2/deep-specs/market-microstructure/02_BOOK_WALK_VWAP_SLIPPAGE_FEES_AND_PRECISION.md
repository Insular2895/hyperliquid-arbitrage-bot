# Book Walk, VWAP, Slippage, Fees and Precision

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Formula references

QF-007/008 govern size/price validity; QF-009/010 govern directed book walks; QF-011 VWAP; QF-012/013 BUY/SELL slippage; QF-014/015 fee rate/value; QF-016 NetConvert. SRC-004 remains authoritative.

## Direction

Base→Quote sells base through bids. Quote→Base buys base through asks. A walk consumes valid levels best-first, never beyond available/protected depth, and returns filled input, gross output, residual, VWAP and consumed-level evidence. Input and output units change with direction.

VWAP derives only from actual fills. BUY and SELL slippage retain separate reference/sign conventions. Neither is an additional debit after exact walk prices are already embodied.

## Precision/minimums

Input size and protected prices are validated under the point-in-time exchange metadata. Rounding is conservative and deterministic. Minimum quantity/notional and output usability are checked for every leg. Current Hyperliquid digits, tick/lot, minimum and matching details require external revalidation.

## Fees

FeeState resolves account/market/mode rate, discount and debit asset. Fee rate and fee value remain distinct and versioned. No hardcoded baseline belongs in route code; no downstream component subtracts fees twice.

## NetConvert

NetConvert returns the one economic output plus validity/provenance. Same inputs must produce identical Rust/Python results. See the [full contract](../../_analysis/pass08_graph_routes_quant/NETCONVERT_CONTRACT.md).
