# Synchronous Dependency DAG Audit

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

```text
Adapter/Normalizer
  → Ordered Coordinator
  → Book/Metadata/Fee/Precision
  → Graph/affected Routes
  → Formula/Opportunity
  → capability-specific Participants/Simulator
  → Terminal/Sizer/Allocator proposal
  → Risk T1
  → atomic Reservation
  → immutable ExecutionPlan
  → Risk T2
  → Effect Executor/Transport
  → observed events
  → Execution/Account/Fill/Inventory reducers
  → Risk T3–T5 / continuation or Recovery
  → Reconciliation / Accounting
```

| Apparent cycle | Staging that removes synchronous recursion | Result |
|---|---|---|
| Opportunity ↔ Participants | current opportunity records episode; offline learned artifact returns later | ACYCLIC |
| Simulator ↔ Sizer | Sizer declares bounded q grid; Simulator evaluates; Sizer selects returned curve | ACYCLIC |
| Atlas ↔ Capital | outcomes feed a later AtlasVersion; current decision pins prior version | ACYCLIC |
| Risk ↔ Sizer | cheap Risk removes invalid region; Sizer proposes; final T1/T2 Risk authorizes | ACYCLIC |
| Execution ↔ Recovery | observed exposure triggers Recovery proposal; Risk authorizes; Execution applies a new plan | ACYCLIC |
| Evidence ↔ capability | runtime emits evidence asynchronously; Validation later publishes immutable manifest | ACYCLIC |
| Infra ↔ trading economics | runtime metrics feed later comparison; host choice never blocks current hot path | ACYCLIC |

Recorder, archive, training, large Monte Carlo, slow Atlas aggregation, license refresh, diagnostics and report generation are asynchronous/background. Synchronous dependency cycles: **0**. Hot-path remote control/storage dependencies: **0**.
