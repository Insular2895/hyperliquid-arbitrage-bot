# 07 — Position Sizing vs Order Slicing

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Non-overlapping questions

| Capability | Question | Inputs | Output | Owner |
|---|---|---|---|---|
| Position Sizing | How much total exposure is economically valid? | Size curves, Simulator distributions, Risk, inventory, balance/book capacity | `q* <= Q_validated` | Inventory/Capital Sizer inside Risk |
| Order Slicing | How is the fixed validated quantity executed through time/orders? | `q*`, book/queue/response, edge survival, Execution constraints | Child-order schedule whose sum does not exceed `q*` | Execution/Slicing |

Sizing precedes Slicing. Slicing cannot create capacity, raise `Q_validated`, avoid shared reservations or change the approved terminal exposure. A material new quantity requires sizing/Risk revalidation.

## Execution-plan examples

| Mode | Sizing consideration | Slicing consideration |
|---|---|---|
| `TT` | Both taker legs' depth, impact, completion and Recovery curve | IOC/protected child timing within approved total |
| `MT` | Maker fill-time/adverse-selection distribution plus taker completion | Placement/reprice/cancel policy for first leg; no second-leg maker default |
| `TTT` | Three dependent taker legs and intermediate future exposure | Leg/child ordering under current state revalidation |
| `MTT` | Maker first-leg support plus two taker legs and longer tail | Maker child lifecycle, then bounded taker continuation |

TM/MM are not silently introduced. Their activation remains an explicit Execution/Risk/Validation decision.

## Fragmentation tests

Same-time children on the same book should consume approximately the same mechanical depth as the equivalent parent quantity; `40 x 50` does not transform a `2,000` order into new liquidity. Temporal slicing must demonstrate benefit after edge decay, competition and replenishment. Otherwise it is not activated.

## Simulator and Execution boundaries

Simulator supplies size- and slicing-dependent distributions. Sizer consumes them to cap exposure. Execution owns real child orders, fills, partials, cancel races and Recovery. Actual child fills update actual inventory immediately; unfilled intention does not.

Sources: SRC-003 §§39–46; SRC-004 QF-075–077; SRC-006 §§83–86; SRC-007 §§40/53–60; SRC-008 §§46–48.
