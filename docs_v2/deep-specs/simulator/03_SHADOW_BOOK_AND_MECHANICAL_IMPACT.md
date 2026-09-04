# 03 — Shadow Book and Mechanical Impact

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## State model

For market `i` at time `t`, the branch keeps a historical/current baseline and an explicit `Δour_i`. Their materialized view is the `Shadow Book`. It holds our deterministic or declared-queue-effects without rewriting the original dataset. `Shadow State` also tracks simulated order, fill, inventory, reservation, and account consequences; it never overwrites actual state.

`Δour` may represent consumed quantities, changed price levels, our resting maker quantity, queue insertion estimate, filled/remaining quantity, partial fill, residual cancellation, and consequent inventory. Every mutation is traceable to branch/order/event IDs.

## Taker mechanical impact

A protected marketable order walks the arrival book. It removes only executable quantity inside its price boundary. The outputs are per-level fills, total filled and residual size, VWAP, QF-012/QF-013 slippage, QF-014/QF-015 fees, QF-016 net conversion, and QF-042 Mechanical Impact.

Mechanical Impact is known conditional on arrival state and exchange rules. It is not the later response of other participants. QF-040 depth participation and QF-041 volume participation measure intervention scale/support; they are not generic slippage formulas.

## Mechanical locality

An order in `A/X` mechanically changes only `A/X`. Other triangle books do not inherit the consumed quantity. A move in `X/B` or `B/A` belongs to later market events or `Δresponse` through Cross-Market Response. This prevents double-counting and false conservation across independent books.

## Our order as shock

The known mutation may also be encoded as response-model inputs: signed OFI shock, depth consumption, levels consumed, spread/imbalance change, queue insertion, and participation. OFI is one conditioning feature; the actual mutated book is primary truth.

## Invariants

- No negative level quantity.
- No fill outside the protected price or available arrival depth.
- Filled plus residual quantity reconciles with submitted valid quantity.
- Same-time fragments on the same immutable starting book approximate aggregate immediate consumption after deterministic ordering.
- Mechanical consumption is not re-added as learned response.
- Baseline and delta remain separately auditable.

## Dependencies

Formula Book owns math; Execution owns order states; Data owns schemas; Participant owns post-intervention conditional response; Risk owns permissions. L2 is sufficient for taker depth walking but not exact maker queue reconstruction.
