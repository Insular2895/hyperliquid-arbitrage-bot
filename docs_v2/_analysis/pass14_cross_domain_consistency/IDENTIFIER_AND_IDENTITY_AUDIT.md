# Identifier and Identity Audit

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Family | Identity rule | Producer | Cross-domain consumers | Audit result |
|---|---|---|---|---|
| `event_id` / `recorder_seq` | Unique event plus definitive local capture order | Recorder | Core, Replay, audit | CONSISTENT |
| `source_connection_id` | Separates reconnect/capture contexts | Adapter | Ordering, data quality | CONSISTENT |
| `VenueId` + `AssetId` | Asset location; same symbol at two venues is not one node | Metadata | Graph, Inventory, future venue work | CONSISTENT |
| `MarketId` | Venue/base/quote market identity | Metadata | Book, Route, Orders, Atlas | CONSISTENT |
| `RouteId` / route version | Ordered directed leg family; reverse direction differs | Route Engine | Opportunity, Execution, Replay | CONSISTENT |
| Opportunity/evaluation IDs | Candidate episode and evaluated q/version tuple | Opportunity | Models, Risk, evidence | CONSISTENT |
| `risk_snapshot_id` / `decision_id` | Frozen input set and its decision | Risk | Reservation, Execution, trace | CONSISTENT |
| `execution_id` / `plan_version` | One route execution and immutable plan revision | Execution | Orders, Recovery, Accounting | CONSISTENT |
| `intent_id` / CLOID / OID | Internal intent, stable client identity, exchange identity remain distinct | Execution/Transport | Reconciliation, FillLedger | CONSISTENT |
| `FillId` | Deduplicates stream/snapshot/reconciliation observations | Account/Execution | Inventory, Accounting, Replay | CONSISTENT |
| reservation IDs | One claim with resource/scope/lifecycle owner | Reservation | Risk, Execution, Capital | CONSISTENT |
| `RunManifest.run_id` | One fully resolved run input identity | Data/Run | Replay, Validation | CONSISTENT |
| `DatasetId` | Point-in-time corpus and filters | Data registry | Replay, Research, Models | CONSISTENT |
| `ModelArtifactId` / version/hash | Immutable approved model artifact | Model manager | Participants, Simulator, Risk | CONSISTENT |
| `EvidenceId` | Immutable evidence package, not mutable dashboard URL | Validation | Capability, Release, Incident | CONSISTENT |
| `IncidentId` | Incident timeline/evidence correlation | Operations | Data, Execution, Validation | CONSISTENT |
| `InfraInstanceId` | Material host/runtime/network identity | Infrastructure | Benchmark, Validation, Deployment | CONSISTENT |

Range checks: 2,590/2,590 stable `REQ-*` headings are unique; QF-001–110 are complete; `CONFLICT-001..128` are complete after adding the two genuine PASS14 domain contradictions; `OPEN-001..028` are complete after restoring root `OPEN-016`; `INV-001..030` remain the exact Risk invariant range. No pre-existing stable ID was renumbered.

The words “market”, “asset”, “route”, “plan”, “order”, “fill”, “run” and “evidence” are not sufficient serialized identifiers without their typed form and version/context.
