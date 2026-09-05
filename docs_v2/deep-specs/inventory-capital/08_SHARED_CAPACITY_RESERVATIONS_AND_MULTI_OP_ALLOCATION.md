# 08 — Shared Capacity, Reservations and Multi-Opportunity Allocation

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Resource model

QF-073 and QF-074 define reserved-adjusted balance and book capacity. The canonical ReservationState separates balance, book and Risk reservations. A book reservation is bound to market, side, depth band and book version; stale book state requires revalidation.

| Resource | Reserved by | Release | Sharing rule |
|---|---|---|---|
| Balance | Execution after accepted allocation | Known terminal/reconciled release | Same asset/location is one pool |
| Book depth | Execution per market/side/band/version | Expiry/revalidation/terminal outcome | Shared legs consume joint L2 capacity |
| Inventory budget | Risk decision/allocation | State transition or re-evaluation | Candidate future deltas aggregate by asset |
| Risk budget | Risk | Known terminal/reconciled outcome | Route/asset/portfolio contributions aggregate |
| Strategy capacity | Sizer/Risk capability | Candidate expiry or policy/version change | Mode/route support cannot be duplicated |
| Bridge capital | Bridge allocation then Execution | Bridge terminal/reconciliation | Competes with strategy/rebalance |
| Recovery capital | Risk/Execution priority path | Recovery verified/reconciled | Reserved before lower-priority new risk |

`UNKNOWN` keeps affected capacity reserved. Ranking alone reserves nothing. Opportunity expiry releases through canonical Execution/Risk lifecycle, never through a private allocator counter.

## Multi-Opportunity Allocation

QF-078 jointly selects quantities for already viable, Risk-eligible candidates using their RAEV curves under shared constraints. Its locked constraint matrix covers capital, shared book capacities, inventory and Risk budgets. Absolute value and validated capacity matter; relative bps alone is insufficient.

```text
individual viability
-> hard Risk eligibility
-> size curves
-> constrained portfolio allocation
-> atomic/canonical reservations
-> final pre-send revalidation
```

## Required interaction cases

- independent opportunities may be funded independently only after proving no shared resource;
- same input balance shares one reserved-adjusted pool;
- same market/side/depth cannot each claim full visible L2;
- same intermediate/terminal asset aggregates future inventory and tail risk;
- Bridge/Rebalance compete with new opportunity capacity;
- Recovery/protection of existing exposure preempts lower-priority allocation.

The Portfolio Optimizer cannot relax constraints, authorize rejected routes or invert PASS05 priority. Two concurrent opportunities must never spend the same balance or book capacity.

## Replay and race properties

Replay reproduces allocation/reservation from ordered events, immutable snapshots and policy version. Property tests cover balance overspend, shared-depth double count, stale candidate release, `UNKNOWN` retention, final revalidation and brute-force equivalence on small optimization cases.

Sources: SRC-003 §§41–47; SRC-004 QF-073–078; SRC-005 §§88–91/145–152 and Data §§39–42; SRC-006 §§97–100.
