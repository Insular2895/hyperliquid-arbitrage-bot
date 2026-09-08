# CORR-03 — Predicted / Actual Join Contract

DOCUMENTATION STATUS: IMMUTABLE EVIDENCE JOIN

```text
DecisionTimeFeatureSnapshot + frozen ExecutionForecast
  -- ExecutionPlanCandidateId / ExecutionId / OpportunityId / versions -->
canonical actual path + terminal/reconciled outcome + separate economic outcome
```

The frozen side records forecast label/horizon, route objective, q/mode, completion-model and Participant/Simulator versions, fidelity/seed, Formula/FeatureSchema/Config versions, books/fees/metadata and infra/run identity. The actual side derives only from unique exchange/account events, canonical Execution/Recovery/Reconciliation and Accounting.

Join states are `EXACT`, `MISSING_PREDICTION`, `UNRESOLVED_ACTUAL`, `INVALID_ACTUAL_EVIDENCE` and separately reported inferred repair. Missing prediction is not 0%; unresolved actual is not 0; an inferred repair cannot enter primary calibration. `PredictedActualJoinRate` and raw counts are mandatory; low completeness invalidates evidence.

Post-outcome simulation is `COUNTERFACTUAL_MODEL` and cannot replace the historical frozen value. Replay/Shadow/Simulated outcomes retain mode/fidelity provenance and cannot be pooled as actual Live labels.
