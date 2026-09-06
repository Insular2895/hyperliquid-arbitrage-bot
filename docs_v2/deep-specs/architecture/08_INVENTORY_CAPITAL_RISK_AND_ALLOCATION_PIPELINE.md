# 08 — Inventory, Capital, Risk and Allocation Pipeline

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

Actual fills produce Inventory deltas. Account balances minus Reservation state produce available resources. Inventory class/bands, future post-action state, exit cost, stranded risk and Atlas-supported future utility produce Terminal Viability and Capital Reachability.

Sizing evaluates a deterministic q grid/refinement inside balance, book, hard inventory, Risk, model/execution support, `Q_validated` and capability scope. `Q_validated` is the supremum of sizes passing all evidence and safety gates, not account balance, visible depth or maximum profitable size. It shrinks whenever support is lost.

Portfolio allocation acts after individual candidate viability and jointly respects shared capacity. Risk constructs `A_safe`, sets ceilings and issues structured decisions; the allocator optimizes only within them. Reservation atomically converts permission into owned capacity before an effect.

Every capital action is classified as `STRATEGY`, `BRIDGE/RELOCATION`, `REBALANCE`, `RECOVERY` or `STAY/HOLD`. Bridge intentionally seeks future destination utility against STAY on a slower horizon. Rebalance restores desired structure. Recovery reduces already-existing exposure under constitutional priority. Their economics and accounting cannot be merged.
