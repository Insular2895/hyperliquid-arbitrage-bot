# 01 — Inventory State, Asset Classes and Bands

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Truth and state separation

Actual inventory changes only from deduplicated actual fills. Every partial fill applies its asset delta immediately; fees and rounding follow the canonical Data/Execution calculation order. Plans, submitted quantities, forecasts, simulated `PortfolioAfter` and order ACKs are not inventory truth.

| State | Meaning | Truth owner |
|---|---|---|
| `ActualBalance` | Exchange-equivalent wallet/account quantity | Account reducer + reconciliation |
| `ReservedBalance` | Quantity claimed by unresolved work | Execution reservation system |
| `AvailableBalance` | Spendable quantity under QF-073 | Derived from actual minus reserved |
| `InventoryState` | Economic positions, targets, bands, flow and classes | Inventory reducer |
| Pending intermediate | Real partial-route exposure | Execution/Inventory |
| MTM | Numeraire valuation, not spendable balance | Accounting/QF-107 |

`UNKNOWN` capital remains reserved. Reconciliation disagreement blocks affected new risk. State includes source versions/timestamps and is reproducible from the canonical event journal.

## Asset classes

The frozen enum spelling is `CoreInventory`, `Transit`, `Excluded`; reporting also carries the source labels `CORE_INVENTORY`, `TRANSIT`, `EXCLUDED`.

- `CORE_INVENTORY`: may be accumulated intentionally only inside validated bounds and only if Terminal Viability remains true. It still needs a credible exit.
- `TRANSIT`: temporary intermediate; normal target is low/short-lived residual inventory. An aged or excessive residual triggers Rebalance/Recovery under Risk.
- `EXCLUDED`: no intentional holding or routing. Accidental exposure is real and must be recovered safely.

Classification is learned from current Hyperliquid evidence and versioned. Reclassification requires calibrated persistence/hysteresis, a reason and an audit event. An example token name is never a default class.

## Targets and bands

Every tradable asset uses `HardMin <= SoftMin <= Target <= SoftMax <= HardMax`. Numeric values are calibrated, not locked.

- QF-064 `Normalized Inventory Deviation` gives comparable distance from target using a scaling band.
- QF-065 `Soft Inventory Penalty` is a calibrated decision term; it changes ranking/size inside the safe set.
- QF-066 `Hard Inventory Gate` rejects new-risk actions whose future state breaches a hard bound.

The future post-trade state is tested. Risk-reducing exceptions must strictly improve an existing violation; they are never a permission to add exposure. Exact concentration, dust, `TransitMaxAge`, `TransitMaxValue`, band widths and penalty coefficients remain calibrated under OPEN-009.

## Required invariants

1. Fill application is exact, deduplicated and ordered.
2. Available balance never becomes negative.
3. Reserved, pending, inventory and MTM are never collapsed into one value.
4. An asset outside its classification policy cannot be a normal terminal.
5. Hard bounds cannot be traded through by a soft penalty.
6. Classification and bands are point-in-time, versioned inputs to Replay.

Sources: SRC-003 §§20–29 and inventory-flow discussion; SRC-004 QF-064–067/QF-073; SRC-005 §§59–74 and Data §§33–41; SRC-006 §§78–96.
