# NetConvert Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

`NetConvert` is the single canonical economic conversion primitive. QF-016 in SRC-004 owns its equation; this document defines the implementation-facing contract without duplicating that equation.

## Inputs

| Input | Contract |
|---|---|
| identity | venue, market, input asset, output asset, explicit `BaseToQuote` or `QuoteToBase` |
| quantity | positive input amount plus unit; no implicit reporting-currency conversion |
| book | immutable valid L2 snapshot, side, source quality, exchange/receive times and BookVersion |
| metadata | base/quote mapping, size/price precision, lot/tick/minimum rules, status and MetadataVersion |
| fees | account/market/execution-mode fee state, debit-asset semantics and FeeVersion |
| execution context | supported mode and protected/limit price constraints |
| formula | FormulaVersion identifying QF-007–016 semantics |

## Algorithmic obligations

1. Resolve direction. Base→Quote walks bids with QF-009; Quote→Base walks asks with QF-010.
2. Apply source-authoritative input quantization and price validity (QF-007/008). Rounding direction must never assume unavailable value.
3. Walk exact available L2 monotonically from best price, respecting the protected limit. Stop at input exhaustion, book exhaustion or protection boundary.
4. Derive filled input, gross output, residual input, levels and QF-011 VWAP. QF-012/013 may describe mechanical slippage but are not independently subtracted after the walk.
5. Resolve QF-014 fee rate and QF-015 fee value under the same state. Apply QF-016 exactly once in the correct asset.
6. Validate market minimums and output usability. The output actually legal after rounding is the only value passed to the next leg.

## Outputs

Economic output amount and unit; filled/unfilled input; completion flag; gross output; fee rate/value/asset; VWAP and consumed-level evidence; residual/dust; all consumed versions and timestamps; deterministic validity/reason result.

## Fail-closed conditions

Unknown fee/metadata, stale/invalid book, mismatched asset roles, invalid price/size, insufficient protected depth, minimum violation, overflow/precision loss, version mismatch or unsupported execution mode cannot return a tradable full output. The caller distinguishes a rejected calculation from a partial executable result.

## Determinism

Same immutable book, metadata, fee state, direction, quantity, execution context and FormulaVersion produce the same result and trace. Decimal/fixed-point representation follows Data Contracts; no floating-point or language-specific behavior is declared here. Rust and Python golden vectors must agree exactly under the accepted numeric contract.

## Sequential routes

Leg *n+1* receives the validated economic output of leg *n*, not its original input, gross output, midpoint estimate or theoretical quantity. If output is below the next leg minimum, the route is invalid for that `q`; remaining amount becomes explicit residual/dust and is handled by the owning Execution/Recovery policy.

## Illustrative example

The source's HYPE/USDC walk demonstrates that selling 50 HYPE consumes bid levels sequentially; the reverse conversion spends USDC through asks. Values are illustrative, not hardcoded tests. Canonical golden vectors must be derived from source-authoritative Formula Book cases during PASS11.
