# Data Lineage, Point-in-time Correctness and Contamination

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Lineage graph

```text
RawEvent → NormalizedEvent → Book/Account State → FeatureSnapshot
→ Opportunity → ModelForecast + ExecutionForecast → RiskDecision
→ ExecutionPlan → OrderIntent → Order/Fill events → PnL + evidence
```

Edges carry IDs, versions and hashes rather than full copies. An EdgeCalculation records route, quantity, book versions, fee version, formula version and result. This makes source/schema/model corrections impact-queryable.

## Point-in-time modes

`Historical truth` uses only metadata, fees, configs, models and artifacts available at historical T. `Research counterfactual` may use a later model on older source evidence only when marked `COUNTERFACTUAL_MODEL` and never described as what the historical bot knew.

Training, calibration, validation and untouched test windows are chronologically separated; at minimum `training_end < validation_start`. Random series splits and future-trained models in historical-truth replay are forbidden. Model artifacts store training range; DatasetId stores filters and included/invalid ranges.

## Quality boundary

Gaps, corrupt clock regions, invalid books or missing markets are labeled with affected scope. Research results state which fidelity they require. No preprocessing may silently drop failed trades, rejects or inconvenient market periods and then claim unbiased evidence.

## Acceptance

A point-in-time audit resolves what was knowable at T and proves that no referenced artifact had a later availability/training boundary. A lineage audit starts at any decision/PnL and reaches checksummed RAW manifests with zero unexplained link.
