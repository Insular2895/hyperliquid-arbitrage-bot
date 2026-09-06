# 05 — Market-to-Decision Pipeline

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

```mermaid
flowchart LR
  M[Valid versioned market/rule state] --> D[affected precomputed routes]
  D --> C[cheap reject-only filters]
  C --> NC[NetConvert over q]
  NC --> E[direct/indirect/cycle economics]
  E --> F[required features/forecasts]
  F --> S[configured Simulator distribution]
  S --> T[terminal viability + inventory effect]
  T --> V[RAEV / P+ / ES / confidence]
  V --> Q[size curve within Q_validated]
  Q --> A[joint allocation]
  A --> R[staged Risk gates]
  R --> Z[atomic reservations]
  Z --> P[immutable ExecutionPlan]
```

Graph is structural; Books are current; Atlas is rolling evidence; HWC is compute relevance; none substitutes for another. BBO can reject but cannot accept. `NetConvert(q)` owns exact L2/fee/precision conversion. Opportunity classifies OWA only with a valid direct comparator and Triangle only when returning to the start asset.

The Participant engine is optional unless the exact capability declares it critical. Simulator fidelity is likewise explicit; conservative F0/F1 and Risk baselines prevent bootstrap cycles. Sizer evaluates candidate q states; it does not recursively ask Simulator to choose q. Portfolio receives individually valid candidates and shared constraints. Risk applies early eligibility and final T1/T2 authorization, with later T3–T5 checks during Execution.

All arrows name actual data contracts detailed in [Decision Pipeline Map](../../_analysis/pass13_master_architecture/DECISION_PIPELINE_MAP.md).
