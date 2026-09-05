# Capacity Reservation Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Resource | Reserver | Reservation point | Release | `UNKNOWN` | Cross-route sharing | Replay |
|---|---|---|---|---|---|---|
| Balance | Execution coordinator | after accepted allocation, before plan/send | known terminal/reconciled state | retain | per asset/location pool | ordered reservation events |
| Book depth | Execution coordinator | current book/side/band/version | terminal, expiry or revalidation | retain if possible exposure | joint market/side capacity | reproduce from book/reservation versions |
| Inventory budget | Risk/allocation | candidate future-state authorization | new coherent decision/state | conservative | aggregate per asset/location | policy + inventory snapshot |
| Risk budget | Risk | RiskDecision | known closed/reconciled exposure | retain | aggregate route/asset/portfolio | RiskDecision/journal |
| Strategy capacity | capability/Sizer | eligible selected curve | expiry/demotion | conservative | mode/route support | RunManifest policy |
| Bridge capital | Bridge allocation -> Execution | before Bridge execution | terminal/reconciled | retain | competes with opportunity/Rebalance | Bridge decision/events |
| Recovery capital | Risk/Execution | priority Recovery plan | Recovery verified/reconciled | retain/escalate | preempts lower priority | Recovery journal |

Ranking alone does not reserve. QF-073/QF-074 are the reserved-adjusted views; negative available capacity is an invariant failure.
