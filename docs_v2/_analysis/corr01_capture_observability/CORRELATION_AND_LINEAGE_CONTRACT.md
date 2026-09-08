# CORR-01 — Correlation and Lineage Contract

DOCUMENTATION STATUS: POST-RECONSTRUCTION CORRECTION — AWAITING HUMAN REVIEW

## Canonical chain

```text
RunId / RunManifest
  -> MarketEventId -> BookVersion
  -> ReevaluationId -> RouteEvaluationId
  -> OpportunityId -> [OpportunityEpisodeId, derived]
  -> ForecastBundleId -> ExecutionPlanCandidateId
  -> SizingDecisionId -> RiskDecisionId
  -> ReservationSetId -> ExecutionId -> ExecutionPlanId
  -> LegId -> IntentId -> CLOID -> [OID]
  -> FillId(s) -> InventoryDeltaId(s)
  -> [RecoveryId -> RecoveryExecutionId(s)]
  -> ReconciliationId -> AccountingOutcomeId
```

Brackets denote optional objects. Optionality must be explicit, not inferred from an absent join.

## Identity rules

- IDs identify immutable records; corrections append a replacement/supersession reference.
- `ExecutionId` is allocated before reservation/plan commitment and remains the attempt-scope correlation root even if nothing can be transmitted.
- `ExecutionAttemptId` may be identical to `ExecutionId` only if its schema contract makes the `CF-13` boundary explicit; otherwise it is a distinct child created at possible transmission.
- Recovery receives its own `RecoveryId` and execution lineage while preserving `originating_execution_id`.
- `OpportunityEpisodeId` is derived and versioned. It may be absent until the projector runs and never blocks runtime.
- `OID` may be absent before exchange acknowledgement; `CLOID`/intent lineage remains mandatory where current exchange semantics support it.
- all records bind `RunMode`, `RunId`, schema version and relevant source/config/model/formula versions.

## Fan-out and fan-in

One market observation can trigger many route evaluations. One opportunity can produce zero or more forecast/candidate revisions but at most one selected immutable plan version per `ExecutionId`. One execution can have many intents, orders and fills. Many fills/recovery actions fan into one terminal reconciliation and one complete attempt-level accounting outcome version.

No positional, timestamp-only or “nearest event” join is canonical where an explicit ID should exist. A derived repair join is labeled `INFERRED_JOIN`, includes algorithm/version/confidence and is excluded from decision-grade rates unless allowed by that metric’s missing-data policy.

## Completeness indicators

Every projected funnel row exposes:

- `lineage_complete` and missing-link reason codes;
- `timing_complete` for the metric-specific endpoints;
- `outcome_complete` and reconciliation status;
- `economic_complete` plus valuation horizon/numeraire;
- `forecast_actual_join_complete` where a forecast is required;
- source/mode and projection version.

Completeness itself is measured. Missing links never disappear from the originating population; reports present included, excluded, unresolved and invalid counts.
