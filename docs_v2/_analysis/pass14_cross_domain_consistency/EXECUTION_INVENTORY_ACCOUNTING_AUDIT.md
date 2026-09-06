# Execution–Inventory–Accounting Audit

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

```text
OrderIntent → observed order/fill events → deduplicated FillLedger
           → Inventory reducer → classified accounting records
           → Reconciliation orders→fills→balances
```

| Event/state | Inventory consequence | Accounting consequence | Reservation consequence | Result |
|---|---|---|---|---|
| plan/intent/sent | none actual | predicted/intent evidence only | remains claimed | PASS |
| zero fill + known terminal reject/cancel | none actual | zero-fill outcome retained | unused amount released after reconciliation | PASS |
| partial fill | apply actual asset/fee delta immediately | route/leg actuals plus explicit residual | used converted; remainder locked/reconciled | PASS |
| full order fill | apply actual fill, not planned size | order fact; route may remain incomplete | used claim reconciled | PASS |
| cancel requested | possible later fill remains | no terminal realization inferred | stays locked | PASS |
| `UNKNOWN` | do not guess | uncertainty evidence | affected capacity stays locked | PASS |
| duplicate fill observation | idempotent no second delta | no second PnL | no second consumption | PASS |
| Recovery fill | update current exposure | separate Recovery PnL/loss | own bounded reservation | PASS |
| external deposit/withdrawal | balance/external-flow change | excluded from profit/MTM per QF-107 | reconcile availability | PASS |
| route completion | only after fills/dust/reservations agree | close disjoint route/recovery/inventory buckets | release only terminal-reconciled unused | PASS |

Accounting authority is now explicit: Inventory/Capital deep spec owns attribution semantics; Formula Book owns QF-105–110; Execution/FillLedger owns actual event facts; Data owns serialized records/lineage. Accounting never becomes a second inventory or fill owner. Actual-versus-hypothetical conflations: **0**. Double application paths: **0**.
