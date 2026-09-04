# Recovery Risk and Action Classification

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Action classification

`RISK_INCREASING` enlarges exposure/commitment and requires every applicable gate. `RISK_NEUTRAL` is not intended to change exposure but must be classified from actual context; query/reconcile are typical, while a cancel can race a fill. `RISK_REDUCING` strictly improves a known existing exposure.

The exact work priority is protection, cancel, reconciliation, recovery, safe continuation, rebalance, new opportunity. Schedulers and scarce API/capital budgets honor that order.

## Limited exception

Unknown safety is fail-closed for new risk. The only wider permission applies to an action that reduces a known exposure and passes `RecoveryRiskPolicy`. This requires:

- actual, reconciled or explicitly bounded exposure identity;
- current valid executable market state and precision/fee rules;
- protected price and reservation;
- strict improvement of the relevant exposure/violation;
- maximum loss/Expected Shortfall and inventory/capital bounds;
- attempt count and elapsed-time bounds;
- post-fill reevaluation and escalation path.

Recovery may have negative expected value because existing exposure protection outranks PnL. Sunk costs are excluded from forward choice. The original intended destination has no privilege; PASS 04's Recovery state machine selects among currently allowed exits/splits through QF-079/QF-080.

## No unlimited loop

Each recovery attempt consumes risk/API/capital budgets until economically resolved. Timeout or lost response becomes UNKNOWN; reservation remains. Every material event triggers reevaluation. Exhausting attempt/time/loss bounds produces appropriate halt and manual escalation, never recursive unbounded trading.

## Mode interactions

`RECOVERY_ONLY` permits no new risk. `HALTED` permits no new risk. A kill may still allow protected reducing exits; it does not guarantee them if books, account truth or price bounds are invalid. Reconciliation is always prioritized where it can safely restore truth.

Source: SRC-005 lines 708–883, 1911–1928, 2415–2512, 3318–3329, 3475–3504 and 4762–4923.
