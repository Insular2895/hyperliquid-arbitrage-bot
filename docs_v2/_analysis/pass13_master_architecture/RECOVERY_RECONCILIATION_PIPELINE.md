# Recovery and Reconciliation Pipeline

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Boundary

| Subsystem | Input truth | Output | Must not do |
|---|---|---|---|
| Execution | immutable plan + ordered order/fill events | lifecycle state/effect intents | invent fills or mutate original plan |
| Inventory | unique actual fills + reconciled balances | current exposure snapshot | infer planned exposure as actual |
| Recovery | current exposure, legal exits, formulas, Risk | bounded recovery-plan proposal/state | privilege original route or chase sunk cost |
| Risk | current snapshots + Recovery policy | recovery-only/deny/bounds decision | allow generic fail-open |
| Reconciliation | exchange orders→fills→balances + journal | consistency/mismatch/readiness evidence | trust checkpoint over exchange |
| Accounting | reconciled actual outcomes | disjoint Recovery/strategy PnL | hide recovery loss in alpha |

```text
material fill/failure/UNKNOWN
→ commit actual facts and lock uncertain resources
→ determine exposure
→ Recovery searches current bounded viable exits
→ Risk authorizes only safe risk-reducing action
→ Execution creates a new immutable plan and uses normal transport
→ repeat from actual events within attempt/time/loss/capacity bounds
→ reconcile orders, fills, balances
→ accounting/evidence
→ release/readiness only when consistent
```

Split recovery is allowed when validated and atomically reserved. Negative immediate EV can be acceptable only for reducing known exposure. Exhausted/no-safe actions contain scope and escalate manually. Reconciliation also gates every startup, restart, reconnect, update, rollback and ownership transfer.
