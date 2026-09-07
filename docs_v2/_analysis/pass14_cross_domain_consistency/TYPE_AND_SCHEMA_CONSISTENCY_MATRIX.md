# Type and Schema Consistency Matrix

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Type/schema | Frozen or authoritative core | Producer / writer | Consumer rule | Consistency result |
|---|---|---|---|---|
| `RawEvent` | event/sequence/source/optional exchange time/receive times/optional market/type/payload/schema | Recorder | L0 immutable; missing optional source data stays absent | PASS |
| normalized events | closed `MarketEvent`, `AccountEvent`, plus Infra/Timer/Control | Normalizer | invalid/unknown cannot mutate L2 | PASS |
| `BookState` | sorted valid sides, freshness/gap state, monotonic version | Book reducer | readers use immutable version | PASS |
| `SourceQuality` | fidelity, age, sequence integrity, clock quality | Normalizer | missing/gapped is not healthy or zero | PASS |
| `RiskSnapshot` | ten frozen version/reference fields | Risk coordinator | one coherent evaluation snapshot | PASS |
| `RiskDecision` | decision/snapshot, allowed/action/max size/protection/reasons/time | Risk | mode/model/config semantics resolve via snapshot/plan | PASS |
| `ExecutionPlan` | execution/opportunity/route/size/legs/mode/reservations/Risk/models/config/time/version | Execution boundary | immutable once planned | PASS |
| `OrderIntent` | intent/execution/leg/market/side/ticks/lots/TIF/CLOID/optional nonce/Risk/time | Execution | quantized and immutable after signing | PASS |
| `FillEvent` / FillLedger | fill identity, order IDs, ticks/lots, optional fee asset, fee, times/source | Account/Execution reducers | dedupe once; only actual fills change economics | PASS |
| `InventoryState` | positions/classes/bands/flows/version | Inventory reducer | actual-fill-derived; no private strategy copy | PASS |
| `ReservationState` | balance/book/Risk claims and lifecycle/version | Reservation Engine | `UNKNOWN` retains affected claim | PASS |
| `InfraState` | exactly `HEALTHY`, `DEGRADED`, `UNSAFE` | Infrastructure | Risk/Operations do not add enum values | PASS AFTER FIX |
| `RunManifest` | eleven frozen fields including optional dataset/seed | Data/Run | artifact evidence links outward; no silent field expansion | PASS AFTER FIX |
| `DecisionTrace` | decisions/intents/transitions/Risk decisions | ordered Core | canonical ordering/hash | PASS |
| `ValidatedCapability` | strategy/market/size/mode/models/level/validity/review/restrictions | Validation | exact-subset match only | PASS |
| phase/evidence binding | `EvidenceId` references RunManifest/artifacts; ValidationReport aggregates; CapabilityManifest links | Data + producer + Validation | reference/hash integrity, no duplicated schema | PASS AFTER FIX |
| accounting record | classified actual components + IDs/versions/numeraire/period/inclusion owner | Accounting logical owner under Data schema | no predicted-as-realized or duplicated component | PASS; concrete serialization remains implementation work |

Schema-version rules are uniform: additive optional fields may be compatible; missing required fields fail; breaking changes increment major schema; migrations are explicit and replay-tested. No competing frozen field set was found.
