# Execution Pipeline Map

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

```mermaid
flowchart TD
  EP[Immutable ExecutionPlan + RiskDecision] --> RV[ReservationState committed]
  RV --> OI[OrderIntent with stable CLOID]
  OI --> FX[Transport submit effect]
  FX --> OBS{Observed event}
  OBS -->|ACK/open| OS[OrderState active]
  OBS -->|unique partial/full fill| FL[FillLedger]
  OBS -->|reject/not transmitted| RR[terminal/release by rule]
  OBS -->|possible transmission/timeout| U[UNKNOWN; reservation locked]
  OS -->|cancel intent| CR[CANCEL_REQUESTED]
  CR -->|cancel confirmation| RR
  CR -->|racing fill| FL
  U --> Q[query orders/fills/balances]
  Q --> RC[Reconciliation]
  FL --> AI[Account + Inventory actual update]
  AI --> NX{T3/T4 revalidate actual remainder}
  NX -->|continue| OI
  NX -->|unsafe/unviable| RE[Recovery proposal → Risk → new plan]
  NX -->|complete| RC
  RE --> FL
  RC --> AC[Accounting + evidence + safe release/readiness]
```

`SubmitOrder` is an effect request, not proof. `SENT` may already have executed. Cancel request does not remove risk. Actual fills alone update inventory and determine the next leg. Partial fills, `DUST_EXPOSURE` and `PendingIntermediateBuffer` remain explicit exposure.

TT/MT/TTT/MTT vary plan structure and order role, not truth semantics. TM/MM stay default-disabled. Transport is mode-specific but reducer, reservation, state-machine, Recovery and accounting contracts remain the same.
