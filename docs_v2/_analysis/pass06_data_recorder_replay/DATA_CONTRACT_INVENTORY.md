# Data Contract Inventory

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

This inventory indexes **68 canonical contracts/representations** recovered from SRC-005 Dossier 4. “Version” means a direct schema/version field or a mandatory link to its enclosing versioned envelope/manifest.

| # | Contract | Layer | Logical owner | Identity/core fields | Time/source | Version/lineage | Principal validation |
|---:|---|---|---|---|---|---|---|
| 1 | RawEvent | L0 | Recorder | event_id, recorder_seq, payload_bytes | all receive/source fields | schema_version | checksum/order/roundtrip |
| 2 | Source | L0/L1 | Adapter | closed enum | source identity | schema-owned | enum exhaustiveness |
| 3 | SourceQuality | L1 | Normalizer | fidelity, age, integrity, clock | source/receive | event lineage | unknown/gap semantics |
| 4 | PriceLevel | L1 | Market schema | price_ticks, quantity_lots | enclosing event | schema-owned | integer bounds |
| 5 | BookSnapshot | L1 | Adapter | market, bids, asks, sequences | exchange?/receive/source | schema_version | ordering/invariants |
| 6 | BookDiff | L1 | Adapter | market, changes, source_seq | exchange?/receive | schema-owned | continuity/resync |
| 7 | TradeEvent | L1 | Adapter | trade?, market, price, quantity, side? | exchange?/receive/source | schema_version | units/dedup |
| 8 | MarketEvent | L1 | Normalizer | six closed variants | envelope | event schema | variant fixtures |
| 9 | MarketDefinition | L1/L2 | Metadata owner | assets, decimals, price rules, min, active | update time/source | metadata_version | dependency invalidation |
| 10 | MetadataVersion | L1/L2 | Metadata owner | monotonic identity | update event | lineage to routes | monotonic change |
| 11 | BookState | L2 | Book owner | sides, best prices, validity | last_update/source quality | version | sorted/gap/hash |
| 12 | BookSnapshotId | L2 | Book owner | snapshot/version set ID | decision cutoff | book versions | exact resolution |
| 13 | AccountEvent | L1 | Account adapter | five closed variants | envelope | event schema | fixtures/dedup |
| 14 | OrderUpdate | L1 | Account adapter | cloid?, oid?, status, sizes | exchange?/receive/source | schema-owned | transition/idempotence |
| 15 | FillEvent | L1/L4 | Account adapter | fill_id, order IDs, price/size/fee | exchange?/receive/source | schema-owned | dedup/units |
| 16 | AssetBalance | L2 | Account owner | total, reserved, available | state cutoff | account version | balance invariant |
| 17 | AccountState | L2 | Account owner | balances, orders, fills, fees, reconciled | event cutoff | state_version | exchange reconciliation |
| 18 | InventoryState | L2 | Inventory owner | positions, targets, bands, flows, classes | event cutoff | version | fill delta/reconcile |
| 19 | InventoryPosition | L2 | Inventory owner | quantity/value/target/bands | valuation time | enclosing version | band/unit tests |
| 20 | AssetClass | L2 | Inventory owner | CoreInventory/Transit/Excluded | classification time | config/atlas version | closed enum |
| 21 | ReservationState | L2 | Reservation owner | balance/book/risk reservations | event cutoff | version | no double spend |
| 22 | BalanceReservation | L2 | Reservation owner | reservation/execution/asset/amount/state | created_at | state version | lifecycle/conservation |
| 23 | BookCapacityReservation | L2 | Reservation owner | market/side/notional/depth/book version | created context | book version | revalidation |
| 24 | RouteDefinition | L2/config | Route owner | route/type/assets/legs/dependencies | metadata context | route_version | graph continuity |
| 25 | RouteLeg | L2/config | Route owner | market/assets/direction | enclosing context | route version | asset continuity |
| 26 | RouteDependencies | L2/config | Route owner | markets/assets/shared books/neighborhood | enclosing context | route version | affected-route lookup |
| 27 | Opportunity | L4 | Strategy | ID/route/size/edges/PnL/state/snapshot | detected_at | state/feature IDs | no stale inputs |
| 28 | OpportunityEpisode | L3/L4 | Research | birth/death/censoring/edge path/regime | event times | dataset_version | label/no-lookahead |
| 29 | FeatureSnapshot | L3 | Feature owner | immutable features | timestamp | feature_schema_version | recompute/parity |
| 30 | ModelForecast | L3 | Model owner | model/input/prediction/confidence/OOD | produced_at | model version | schema/support |
| 31 | EdgeSurvivalForecast | L3 | Participant model | survival/half-life/edge quantiles | horizons | model/input lineage | calibration/OOS |
| 32 | LiquidityForecast | L3 | Participant model | depth/loss/replenishment/spread | horizons | model/input lineage | calibration/OOS |
| 33 | MakerForecast | L3 | Participant model | fill/time/partial/adverse selection | horizons | model/input lineage | calibration/OOS |
| 34 | CrossMarketForecast | L3 | Participant model | source market/responses/confidence | horizon in responses | model/input lineage | lift/ablation |
| 35 | ResponseForecast | L3 | Participant model | target/horizon/move/quantiles/probability | horizon | parent forecast | calibration |
| 36 | ExecutionForecast | L3/L4 | Simulator | outcome probs/PnL quantiles/cost/confidence | arrival scenario | simulation_version | distributions/calibration |
| 37 | RiskSnapshot | L2/L4 | Risk coordinator | exact state/model/config version set | created_at | risk IDs/versions | immutable/canonical order |
| 38 | RiskDecision | L4 | Risk | allow/action/size/protection/reasons | created_at | snapshot ID | deterministic gate tests |
| 39 | ExecutionPlan | L4 | Execution | IDs/size/legs/mode/reservations/risk | created_at | plan/model/config versions | immutable/revalidate |
| 40 | ExecutionLegPlan | L4 | Execution | market/assets/role/policy/amounts/protection | plan time | plan version | actual-input/protection |
| 41 | OrderPolicy | L4 | Execution | liquidity role/TIF/post-only/protection | plan context | config/plan | exchange boundary |
| 42 | OrderIntent | L4 | Execution | intent/execution/leg/market/side/price/size/TIF/cloid/nonce?/risk | created_at | risk/plan lineage | idempotence/protection |
| 43 | SignedOrderIntent | L4 | Signer | intent/nonce/signature | signed_at | intent lineage | immutability/nonce |
| 44 | TransportRequest | L4 | Effect executor | signed intent/type/request/send? | send_at? | intent lineage | transport idempotence |
| 45 | EngineInputEvent | L1 | Core coordinator | Market/Account/Infra/Timer/Control | envelope | event schema | total order/exhaustive |
| 46 | InfraEvent | L1 | Infra adapter | clock/network/compute/recorder/feed health | event time | schema/version | health fault tests |
| 47 | TimerEvent | L1 | Clock/scheduler | five strategic timer variants | Clock time | event schema | exact Replay firing |
| 48 | ControlEvent | L1 | Control adapter | start/stop/kills/config update | receive time | config/event version | authorization/order |
| 49 | DecisionEvent | L4 | Core modules | typed important decision | decision time | snapshot IDs | trace completeness |
| 50 | RejectEvent/Reason | L4 | Strategy/Risk | route/opportunity?/reasons/snapshots | timestamp | versioned closed reasons | aggregation/counterfactual |
| 51 | InfraState | L2 | Infra owner | health distributions/recorder/state | state cutoff | version | update/fault tests |
| 52 | ResolvedConfig | config | Config owner | resolved values/hash/version/provenance | effective time | config hash/version | validation/bounds |
| 53 | RunManifest | run | Run owner | run/mode/code/build/config/dataset/models/formulas/events/seed | start_time | all run inputs | resolvability |
| 54 | DecisionTrace | L4 | Run owner | decisions/intents/transitions/risk decisions | ordered sequence | run/input lineage | canonical hash |
| 55 | NormalizedEvent | L1 | Normalizer | schema version/raw ID/payload | derived from RAW | raw-event lineage | deterministic roundtrip |
| 56 | RawChunkManifest | L0 | Recorder | file/time/count/checksum/size/schema | start/end | chunk/schema | checksum/count/order |
| 57 | ExecutionJournalEvent | L4 | Journal | journal_seq/event/checksum? | timestamp | execution lineage | append/replay |
| 58 | Effect | boundary | Reducer/executor | submit/cancel/persist/metric/reconcile | ordered request | trigger event/state | command/event separation |
| 59 | StateTransition | L4 | State owner | entity/from/to/trigger/reason | timestamp | trigger event | reason/order |
| 60 | IncidentRecord | L4/ops | Operations | ID/severity/scope/triggers/actions/resolution | start/end? | evidence bundle | reconstruction |
| 61 | ClockQualityRecord | L1/L2 | Infra/Clock | offset/uncertainty/source count | timestamp | clock source/version | uncertainty gate |
| 62 | ReplayFidelity | run | Simulator/Replay | F0Historical..F4Interactive | run context | manifest | declared support |
| 63 | SimulationMode | run | Simulator | ExogenousReplay/InteractiveCounterfactual | branch context | manifest/branch | mode isolation |
| 64 | ConfidenceState | L3 | Model/Simulator | level/fidelity/freshness/support/OOD/disagreement/latency uncertainty | snapshot time | model/input | decomposed confidence |
| 65 | LatencyTrace | L3/L4 | Infra/Execution | stage timings and correlation IDs | receive/send/ack/fill | infra/run IDs | monotonic/uncertainty |
| 66 | ModelVersion | artifact | Model registry | ID/semver/training dataset/feature schema/hash | availability/training range | artifact lineage | hash/schema/OOS |
| 67 | DatasetId | dataset | Data registry | ranges/manifests/normalization/filters | covered ranges | full lineage | quality/resolution |
| 68 | ExperimentResult | research | Research registry | run/strategy/config/metrics | created_at | run/dataset IDs | manifest/no-notebook-only |

Field-level schemas remain source-accurate where SRC-005 freezes them. Cross-domain semantic expansion belongs to its owning pass and must not mutate the frozen Data contract silently.

## Mandatory attribute completion

This table completes, for every numbered contract above, purpose, producer/consumer, units, persistence, Replay/Risk/Execution role, source locator and status. Read it together with the first table for exact fields, layer, timestamp and version/provenance.

| # / contract | Purpose | Producer → consumers | Units | Persistence | Replay role | Risk role | Execution role | Source locator | Status |
|---|---|---|---|---|---|---|---|---|---|
| 1 RawEvent | Preserve observed bytes/order | Recorder → Normalizer/Audit | typed times/raw bytes | RAW chunks | Primary input evidence | Data eligibility | Incident evidence | SRC-005 D4 §5 | LOCKED |
| 2 Source | Type origin | Adapter → all event consumers | enum | Event envelope | Select adapter semantics | Fidelity input | Transport trace | §11 | LOCKED |
| 3 SourceQuality | Qualify evidence | Normalizer → State/Risk/Replay | age duration + enums | Normalized/quality | Fidelity gate | Eligibility/confidence | Pre-send context | §12 | LOCKED |
| 4 PriceLevel | Exact book level | Adapter → Book/Simulator | ticks/lots | Normalized | Rebuild book | Liquidity/impact | Protected pricing | §15 | LOCKED |
| 5 BookSnapshot | Full observed book | Adapter → Book/Replay | ticks/lots/times | RAW-derived normalized | Bootstrap/resync | Freshness/validity | Arrival state | §14 | LOCKED |
| 6 BookDiff | Incremental book change | Adapter → Book | ticks/lots/source seq | Normalized | Exact state evolution | Gap gate | Arrival state | §17 | LOCKED |
| 7 TradeEvent | Observed trade | Adapter → Features/Models | ticks/lots/times | Normalized/long | Market evidence | Volatility/model input | Calibration context | §18 | LOCKED |
| 8 MarketEvent | Close market union | Normalizer → Core | variant-specific | Normalized | Core input | Market eligibility | Strategy/execution context | §13 | LOCKED |
| 9 MarketDefinition | Exchange rules/identity | Metadata → Routes/Precision | decimals/notional typed | Versioned metadata | Point-in-time input | Rule validity | Quantization | §22 | LOCKED |
| 10 MetadataVersion | Pin metadata | Metadata → all dependants | integer/version | Permanent references | Historical rules | Unknown metadata blocks | Plan pin | §23 | LOCKED |
| 11 BookState | Canonical market projection | Book owner → readers | ticks/lots/time | Checkpoint optional | Reconstructed state | Gate/snapshot | Price input | §24–27 | LOCKED |
| 12 BookSnapshotId | Identify exact books | Book owner → Decision/Risk | typed ID | Decision lineage | Resolve state cutoff | Frozen market versions | Plan provenance | §28 | LOCKED |
| 13 AccountEvent | Close account union | Account adapter → Core | variant-specific | P0/permanent | Account input | Reconciliation gate | State-machine input | §29 | LOCKED |
| 14 OrderUpdate | Observe order state | Account adapter → Execution | ticks/lots/status/time | P0/permanent | Rebuild order state | Unknown exposure | Transition trigger | §30 | LOCKED |
| 15 FillEvent | Observe economic fill | Account adapter → State/Accounting | ticks/lots/fee amount | P0/permanent | Sim/live common event | Actual exposure truth | Next-leg quantity | §31–32 | LOCKED |
| 16 AssetBalance | Exact account resource | Account owner → Risk/Execution | exact asset amount | Checkpoint + P0 | Rebuild account | Capacity gate | Reservation/send | §33 | LOCKED |
| 17 AccountState | Canonical account state | Account owner → readers | exact asset amounts | Checkpoint/journal | Simulated/live schema | Reconciled eligibility | Order/fill truth | §34–35 | LOCKED |
| 18 InventoryState | Canonical portfolio inventory | Inventory owner → Risk/Portfolio | quantities/values/bands | Checkpoint + evidence | Simulated inventory | Band/capital gates | Recovery input | §36 | LOCKED |
| 19 InventoryPosition | Per-asset exposure | Inventory owner → Risk | quantity/value/bands | State/checkpoint | State input | Hard/soft bands | Recovery target | §38 | LOCKED |
| 20 AssetClass | Classify asset use | Inventory policy → Strategy/Risk | enum | Config/state | Same classification | Terminal viability | Route/recovery role | §37 | LOCKED |
| 21 ReservationState | Canonical commitments | Reservation owner → Risk/Execution | asset/book/risk quantities | Journal/checkpoint | Same engine reservations | No double spend | Send/continuation | §39 | LOCKED |
| 22 BalanceReservation | Lock balance | Reservation owner → Execution/Risk | exact asset amount | Journal/state | Simulated commitment | Available capacity | Order permission | §40 | LOCKED |
| 23 BookCapacityReservation | Lock depth | Reservation owner → Risk/Execution | notional/depth/ticks context | Journal/state | Shared-depth correctness | Liquidity capacity | Pre-send revalidate | §41–42 | LOCKED |
| 24 RouteDefinition | Define conversion path | Route registry → Strategy/Simulator | typed IDs | Versioned config | Same routes | Scope/dependencies | Plan construction | §43–44 | LOCKED |
| 25 RouteLeg | Define one conversion | Route registry → Engines | typed IDs/direction | Route artifact | Same legs | Leg eligibility | Order derivation | §45–46 | LOCKED |
| 26 RouteDependencies | Identify affected state | Route registry → Coordinator | ID sets | Route artifact | Incremental replay | Snapshot completeness | Shared-book context | §47–48 | LOCKED |
| 27 Opportunity | Record candidate economics | Strategy → Simulator/Risk/Data | size/edge/PnL/time | Long/permanent | Expected decision input | Candidate only | Not yet a plan | §49–51 | LOCKED |
| 28 OpportunityEpisode | Label lifecycle | Research pipeline → Models | times/edges/regime | Derived/permanent | Training/analysis | Bias/OOD evidence | No direct action | §52 | LOCKED |
| 29 FeatureSnapshot | Freeze model inputs | Feature owner → Models/Strategy | feature-specific | Long/lineage | Deterministic input | Freshness/schema | Decision context | §53–54 | LOCKED |
| 30 ModelForecast | Standard prediction | Model → Simulator/Risk | probability/value/confidence | Decision evidence | Same artifact output | Support/OOD | Plan context | §55 | LOCKED |
| 31 EdgeSurvivalForecast | Predict edge persistence | Participant model → Risk/Simulator | probabilities/time/edge | Derived evidence | Arrival scenarios | Survival gate | TTL/continuation | §56 | LOCKED |
| 32 LiquidityForecast | Predict future liquidity | Participant model → Simulator/Risk | depth/probability/spread | Derived evidence | Arrival distribution | Impact support | Fill/recovery context | §57 | LOCKED |
| 33 MakerForecast | Predict maker outcome | Participant model → Execution/Simulator | probabilities/time/adverse value | Derived evidence | Queue scenarios | Maker support | Maker policy | §58 | LOCKED |
| 34 CrossMarketForecast | Predict neighbour response | Participant model → Simulator/Risk | move/probability/horizon | Derived evidence | Interactive input | Confidence | Recovery context | §59 | LOCKED |
| 35 ResponseForecast | Per-target response | Participant model → Simulator | move/quantiles/time | Derived evidence | Branch response | Confidence input | No direct command | §60 | LOCKED |
| 36 ExecutionForecast | Outcome distribution | Simulator → Risk/Sizing | probabilities/PnL/cost | Decision evidence | Simulated outcome | Tail/EV gates | Plan choice input | §61 | LOCKED |
| 37 RiskSnapshot | Freeze authorization inputs | Coordinator → Risk | versions/IDs/time | Permanent decision lineage | Deterministic input | Core snapshot | Pre-plan contract | §62 | LOCKED |
| 38 RiskDecision | Authorize/reject | Risk → Execution/Data | size/protection/reasons | Permanent | Expected trace output | Canonical decision | Permission boundary | §63 | LOCKED |
| 39 ExecutionPlan | Freeze allowed action | Execution → Signer/Coordinator | sizes/prices/slippage | Permanent | Same state machine | Pins permission | Plan contract | §64–66 | LOCKED |
| 40 ExecutionLegPlan | Specify leg | Execution → Order builder | amounts/prices/slippage | Permanent with plan | Same plan logic | Leg limits | Intent derivation | §67–68 | LOCKED |
| 41 OrderPolicy | Specify order behavior | Execution policy → Transport | TIF/role/protection | Plan/config | Emulator behavior | Protection gate | Transport semantics | §69 | LOCKED |
| 42 OrderIntent | Stable order intention | Execution → Signer/Journal | ticks/lots/time | P0/permanent | Emulator input | Risk decision link | Idempotent command identity | §70–71 | LOCKED |
| 43 SignedOrderIntent | Immutable signed intent | Signer → Transport | nonce/signature/time | P0/permanent | Simulated boundary may bypass signing only explicitly | Authorization trace | Submit payload | §72 | LOCKED |
| 44 TransportRequest | Isolate transport | Effect executor → transport | request/time/type | Journal/trace | Swap transport | No policy change | Submit/cancel boundary | §73–75 | LOCKED |
| 45 EngineInputEvent | Core input union | Adapters/Clock/Control → Core | variant-specific | Ordered stream | Primary engine input | Gates react | Drives state machine | §79 | LOCKED |
| 46 InfraEvent | Observe runtime health | Infra → Core/Risk | health values/time | Long/incident | Reproduce health | Eligibility | May halt sends | §80 | LOCKED |
| 47 TimerEvent | Deterministic strategic time | Clock/scheduler → Core | logical time | Ordered stream | Exact timer replay | Rechecks/expiry | Cancel/reconcile timing | §81–82 | LOCKED |
| 48 ControlEvent | Record operator/config control | Control plane → Core | enum/time | Permanent if material | Reproduce control | Kills/config | Start/stop actions | §83 | LOCKED |
| 49 DecisionEvent | Structure important choice | Core modules → Trace | IDs/reasons/time | Permanent/long | Trace output | Audit decision | Execution lifecycle | §84 | LOCKED |
| 50 RejectEvent/Reason | Preserve non-actions | Strategy/Risk → Dataset | codes/IDs/time | Permanent/long | Counterfactual labels | Explain rejection | No order | §85–87 | LOCKED |
| 51 InfraState | Canonical health state | Infra owner → Risk/Core | distributions/health/version | Checkpoint/incident | State input | System gate | Send readiness | §88–89 | LOCKED |
| 52 ResolvedConfig | Pin effective config | Config loader → all modules | typed values/hash | Permanent per run | Exact replay input | Bounds/policy | Plan semantics | §90–92 | LOCKED |
| 53 RunManifest | Resolve full run | Run owner → Replay/Validation | IDs/hashes/time/seed | Permanent | Required input identity | Evidence scope | Execution provenance | §93–95 | LOCKED |
| 54 DecisionTrace | Canonical run decisions | Core/run owner → Validation | ordered arrays | Permanent | Equality target | Risk trace | Intent/transitions | §96–100 | LOCKED |
| 55 NormalizedEvent | Link typed event to RAW | Normalizer → Core/Data | schema/ID/payload | Normalized | Direct input | Quality/schema | Trigger event | §122 | LOCKED |
| 56 RawChunkManifest | Prove chunk integrity | Recorder → Archive/Replay | time/count/bytes/checksum | Long/permanent manifest | Dataset resolution | Quality gate | Incident evidence | §119–121 | LOCKED |
| 57 ExecutionJournalEvent | Append critical transition | Execution journal → Recovery/Audit | sequence/time/checksum | P0/permanent | Rebuild state | Unknown/reconcile | Crash consistency | §130–132 | LOCKED |
| 58 Effect | Isolate side effect | Reducer → EffectExecutor | variant-specific | Journal if material | Swap executor | No hidden bypass | Submit/cancel/persist request | §133–139 | LOCKED |
| 59 StateTransition | Explain state change | State owner → Trace | states/reason/time | Permanent/long | Equality output | Audit invariants | State-machine proof | §274–275 | LOCKED |
| 60 IncidentRecord | Group anomaly evidence | Operations → Audit/Replay | severity/scope/time | Permanent | Reconstruction entry | Kill/recovery evidence | Affected executions | §276–279 | LOCKED |
| 61 ClockQualityRecord | Qualify time comparison | Clock/Infra → Data/Risk | offset/uncertainty/time | Long/incident | Validate merge/timing | Clock-health gate | Latency confidence | §246–249 | LOCKED |
| 62 ReplayFidelity | Declare simulation support | Replay/Simulator → Validation | enum | Run manifest/result | Bound claims | Confidence gate | Fill-model support | §168–169 | LOCKED |
| 63 SimulationMode | Declare exogenous/interactive | Simulator → Replay/Validation | enum | Run manifest | Select semantics | Confidence context | Exchange emulator context | §170–172 | LOCKED |
| 64 ConfidenceState | Decompose uncertainty | Models/Simulator → Risk | levels/probabilities/age | Decision evidence | Fidelity report | OOD/size gate | Recovery confidence | §176–177 | LOCKED |
| 65 LatencyTrace | Attribute runtime timeline | Infra/Execution → Research/Risk | ns timestamps/durations | Long/permanent for trades | Counterfactual latency | Infra/model input | Actual timing | §178–183 | LOCKED |
| 66 ModelVersion | Identify artifact | Model registry → all consumers | versions/hash/ranges | Permanent | Exact artifact | Support/OOD | Forecast provenance | §113–115/255–256 | LOCKED |
| 67 DatasetId | Identify evidence corpus | Data registry → Run/Research | ranges/IDs | Permanent manifest | Resolve events | Quality/support | Calibration evidence | §116–117/300 | LOCKED |
| 68 ExperimentResult | Persist research outcome | Research runner → Validation | metrics/time/versions | Permanent if material | Replay result | Promotion evidence | Capability evidence | §301–304 | LOCKED |
