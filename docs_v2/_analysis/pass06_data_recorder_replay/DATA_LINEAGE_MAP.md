# Data Lineage Map

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

```text
RawChunkManifest/checksum
  └─ RawEvent(event_id, recorder_seq, source, times, schema)
      └─ NormalizedEvent(source_raw_event_id, normalization schema)
          ├─ BookState/AccountState(state version)
          │   └─ FeatureSnapshot(feature schema)
          │       ├─ Opportunity
          │       └─ ModelForecast(model artifact)
          └─ Execution/account evidence
                  ↓
ExecutionForecast(simulation version) + RiskSnapshot(exact versions)
  → RiskDecision → ExecutionPlan → OrderIntent → transport effect
  → OrderUpdate/FillEvent → Inventory/Account/Execution state
  → PnL/ExperimentResult/IncidentRecord
```

| Edge | Required provenance key |
|---|---|
| RAW chunk → RawEvent | file ID, checksum, recorder sequence range |
| RawEvent → NormalizedEvent | `source_raw_event_id`, schema/normalizer version |
| Event → State | trigger event ID, prior/new state versions |
| State → Feature | input snapshot IDs/versions, feature schema |
| Feature → Forecast | input snapshot ID, model version/artifact hash |
| State/Forecast → Risk | RiskSnapshot ID and all frozen versions |
| Risk → Plan/Intent | decision/plan/execution/leg/intent IDs |
| Intent → exchange result | cloid, oid, fill IDs and journal sequence |
| Fill → PnL | fill ledger IDs, fees, valuation/formula version |
| Any research conclusion | RunManifest, DatasetId, ExperimentResult |

IDs/versions/hashes avoid copying every upstream object while keeping resolution mandatory. A broken reference is a validation failure. Historical truth also proves each config/model/metadata/fee artifact was available at the decision time.
