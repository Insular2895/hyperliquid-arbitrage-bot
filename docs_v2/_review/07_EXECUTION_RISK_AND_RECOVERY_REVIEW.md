# Execution, Risk and Recovery Review

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Normal bounded flow

1. Coherent state produces a size-dependent candidate.
2. Sizing returns a bounded proposal; Risk evaluates current versions and capability scope.
3. Shared balance, book, inventory and Risk capacity are atomically reserved.
4. An immutable `ExecutionPlan` emits an order intent/effect.
5. Observed exchange facts drive `OrderState`; unique actual fills drive Inventory.
6. After every fill, next-leg feasibility and Risk are recomputed from actual output.
7. Completion, abandonment or Recovery ends in Reconciliation and accounting.

Five state families stay distinct: Engine, RouteExecution, Order, Recovery and Reconciliation. TT, TTT, MT and MTT share the actual-output rule; maker support alone grants no maker mode.

## Failure branches

| Branch | State truth | Inventory / reservation | Risk action | Required next step |
|---|---|---|---|---|
| Submit result unknown | order may exist or have filled | no invented fill; reservation remains locked | no new overlapping risk | query by identity, reconcile, then decide |
| Partial fill | received fill is economic truth | update exact filled delta; retain/recompute needed reservation | re-run T3/T4 gates | continue with actual output, resize, or Recovery |
| Reject before fill | terminal reject observed | Inventory unchanged; release only proven unused claims | reevaluate candidate | end or create a new separately authorized plan |
| Cancel requested | still nonterminal | Inventory follows later fills; reservation remains | treat exposure as live | await observed terminal state/query/reconcile |
| Disconnect/reconnect | local state may be stale | no speculative release/change | halt new risk or Recovery-only | restore subscriptions and reconcile |
| Crash/restart/rollback | prior external effects persist | rebuild journal/fills/reservations | not READY | reconcile orders→fills→balances before activity |
| Next leg infeasible | existing exposure is real | preserve actual intermediate inventory | prohibit planned continuation | bounded current-state Recovery or containment |
| Recovery exhausted/uncertain | exposure may remain | keep conservative ownership and inventory truth | halt/escalate; never unbounded retry | reconciliation plus operator incident path |

## Risk checkpoints

Risk evaluates at T0 detection, T1 pre-reservation, T2 pre-send, T3 after each fill, T4 before each next leg and T5 while maker liquidity rests. The hierarchy is Global → Inventory/Allocation → Route → Leg → Order. Higher scopes can narrow but never relax lower hard safety.

Recovery ignores the planned route’s sunk costs because they cannot be recovered and must not rationalize added risk. It chooses a bounded, Risk-approved exit from current exposure, possibly split and possibly negative-EV. Reconciliation restores exchange truth at startup and after UNKNOWN, reconnect, crash, update, rollback or material inconsistency.

Reviewer must reject the baseline if any path permits blind retry, planned-fill propagation, premature reservation release, hard-gate bypass, unresolved exposure reaching READY or license/telemetry failure preventing safe containment.

## CORR-03→06 completion and priority boundary

Actual outcomes retain zero fill, partials, later-leg failures, `UNKNOWN`, Recovery entry/result, reconciliation and PnL as separate evidence axes. `p_full` predicts original-route completion; it cannot update state or grant Risk. Current Hyperliquid IOC and ALO write priorities are optional typed policies with different mechanics/cost bases. A charge is not a fill and payment does not guarantee completion.

The latency guide recommends fast cancels, while the exchange endpoint says `f:true` currently has no other effect and expects a future upgrade. The current measurable advantage remains `DOC-SCOPE CONFLICT / REVALIDATION REQUIRED`; no execution assumption is invented. Every state invariant above remains unchanged.
