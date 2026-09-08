# CORR-03 — Recovery Evidence Contract

DOCUMENTATION STATUS: DERIVED EVIDENCE CONTRACT

Each Recovery episode correlates originating `ExecutionId`, trigger/path flags, canonical `RecoveryId`, actual or conservatively uncertain exposure at entry, current book/version, considered candidate exits, chosen `RecoveryPlan`, Risk decisions, reservations, child intents/orders/unique fills, quantities/fees, attempts, elapsed time, QF-080 cost/loss evidence, final inventory/exposure, final `RecoveryState` and Reconciliation proof.

Recovery begins from current actual exposure/current valid books, not original planned quantities. An unknown Recovery order remains locked and is reconciled; a partial Recovery fill changes exposure once, then a new plan is computed for the remainder. Blind replay of the old order is forbidden.

`RecoverySucceeded=1` only when canonical `RecoveryState::RECOVERED` and required account evidence agree. This does not imply original route completion or nonnegative Recovery PnL. `RECOVERY_FAILED` means the permitted automated lifecycle did not reach `RECOVERED`; residual/manual state stays visible and economically accounted.
