# BBO Safe-Bound Analysis

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

## Proof obligation

A C2 rejector is valid only if, for every state and quantity in its declared domain:

`C2 rejects ⇒ canonical exact L2 route result cannot pass the same acceptance predicate`.

The proof record identifies strategy/family, direction, `q`, BBO prices and sizes, protected limits, fee assets/rates/rebates, quantization, minima, comparator, bound construction, version domain, failure cases and whether deeper L2 can overturn the conclusion.

## Candidate bounds

| Candidate | Classification | Current disposition | Why |
|---|---|---|---|
| invalid/crossed/stale BBO | C1 | permitted under existing state contract | state is not executable input |
| best-price unlimited-fill upper bound for one directed gross conversion | C2 building block | conditionally sound before fees/rules | deeper bids cannot exceed best bid; deeper asks cannot cost less than best ask |
| one-leg net upper bound with arbitrary fee debit/rebate/minimum/rounding | C2 | `TO_PROVE` | monotonicity and asset transforms are not universally implied |
| Triangle product of optimistic leg bounds | C2 | `TO_PROVE` | composition requires monotonic fee/quantization transforms and closure in start asset |
| OWA indirect optimistic upper bound vs exact direct output | C2 | potentially sound if direct lower/comparator value is executable at same q/state | both sides and terminal unit must be comparable |
| OWA indirect optimistic upper bound vs optimistic direct output | C4 only | rejected as permanent rejector | an overestimated comparator can create a false rejection |
| price product, midpoint or learned profitability score | C4 | priority only | not executable economics |

## Permanent rejectors proven by CORR-02

Only C1 validity rejections already owned by canonical state contracts are fully available. The structural statement that a one-leg best-price fill is optimistic is proven, but no complete route-level fee/quantization/minimum-aware C2 predicate is promoted here. Exact C2 set remains calibrated/proof-gated. Uncertain cases fall through to full L2.
