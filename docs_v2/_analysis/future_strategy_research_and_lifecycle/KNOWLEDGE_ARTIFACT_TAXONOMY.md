# Knowledge Artifact Taxonomy

| Family | Identity rule | Role |
|---|---|---|
| `HYP-*` | documentary, immutable version | falsifiable hypothesis |
| `EXP-*` | documentary, immutable/superseded | experiment protocol and result |
| `BENCH-*` | documentary; not `REQ-BENCH-*` | measured benchmark artifact |
| `STRAT-*` | documentary strategy lineage | `StrategySpec` version |
| `ADR-*` | durable design decision | does not replace HDC/authorization |
| `POST-*` | linked to canonical `IncidentId` | postmortem document |
| `REL-*` | release evidence | not deployment authorization alone |
| `EXT-*` | existing external register | dated external fact/revalidation |
| `DatasetId`, `RunId`, `IncidentId`, `EvidenceId` | existing typed authority | runtime/data identity |
| `HDC-*` | post-reconstruction human request ledger | pending human acceptance |

Display labels `DATASET-*`, `RUN-*` and `INC-*` must serialize existing typed IDs; they never create parallel identities. IDs are never reused. Supersession preserves every version and every losing/failed artifact.
