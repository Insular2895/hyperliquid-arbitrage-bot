# 06 — Execution, Recovery and Reconciliation Pipeline

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

Execution consumes only a current `RiskDecision`, successful reservation and immutable plan. Transport executes effects and reports observations; it owns no business permission.

After every unique actual fill, the FillLedger and Account/Inventory reducers commit the actual amount and fee. The next leg is recomputed from that actual output, rounded under current rules and reauthorized. A planned amount never updates inventory. Partial fills and dust/intermediate buffers are explicit exposure, not errors to hide.

`SENT` means transmission may have occurred. Timeout/ambiguous state becomes `UNKNOWN`: no blind resend, no resource release, stable CLOID lookup/query and reconciliation. `CANCEL_REQUESTED` leaves the order live until a terminal observation; racing fills remain actual.

Recovery begins from current exposure and searches bounded legal risk-reducing exits. It may split and may accept negative immediate EV within the Recovery Risk policy. Execution applies the resulting new plan through the same machinery, avoiding a circular private call path.

Reconciliation establishes orders, then fills, then balances and only then consistency/readiness. It runs on startup, reconnect, crash, UNKNOWN, update/rollback and relevant incidents. Accounting and evidence consume reconciled actual facts. Exact machines remain owned by [Execution](../../10_EXECUTION_STATE_MACHINE.md).
