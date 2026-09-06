# Component Catalog

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

Logical component does not mean process, crate or microservice. `HP` = hot path; `NL` = near-line; `BG` = background/control; `OFF` = offline. All runtime readers consume immutable snapshots and all decision outputs retain input versions.

| Component | Purpose / owner | Inputs | Outputs and owned mutable state | Commands / events / effects | Placement; persistence | Modes; failure/Risk; minimum maturity | Source master |
|---|---|---|---|---|---|---|---|
| Public Feed Adapter | Translate market source / Data | WS payload, connection state, clock | `RawEvent`, normalized market observations; adapter health | subscribe/reconnect; feed events; network I/O | HP I/O; RAW async | all; affected market invalid; M1/M2 then M3+ | 11/12 |
| Account Adapter | Translate authenticated account facts / Execution+Data | order/fill/balance payload | account events; adapter health | query/subscribe; account events; network I/O | HP I/O; P0 journal | all effect modes; account uncertainty blocks risk | 10/11 |
| Metadata Adapter | Translate spot rules / Graph+Data | metadata payload | metadata events | refresh; rule events; network I/O | NL; RAW/versioned | all; unknown rules fail closed | 03/11 |
| Normalizer | Validate external schemas / Data | RAW payload | typed L1 events | normalize command; normalized/reject event | HP bounded; derived persisted | all; invalid cannot mutate state; M1 | 11 |
| Clock | Provide explicit time domains / Data+Infra | wall/monotonic/exchange/replay time | clock observations/quality | timer command; `TimerEvent`; none | HP service + BG sync evidence | all; unhealthy narrows Risk | 11/13 |
| Ordered Event Coordinator | Establish deterministic commit order / Data | `EngineInputEvent`, worker result | committed versions/order | accept event/result; transition events; effect requests | HP single logical writer; journal | all identical; stale result rejected; M2 | 11/12 |
| Book Engine | Reconstruct coherent L2 / Graph | market events | `BookState`/`BookSnapshot` | reduce event; book state event | HP; checkpoint/replay | all; stale/gap disables market; M2/M3 | 03/11 |
| Metadata Engine | Own point-in-time market definitions / Graph | metadata events | `MetadataState` | reduce; version event | NL/HP read; checkpoint | all; unknown disables affected scope | 03/11 |
| Fee Engine | Own fee schedule/version / Formula | fee/account rules | `FeeState` | update; version event | NL/HP read; point-in-time data | all; unknown rejects economics | 04/11 |
| Precision Engine | Own tick/lot/minimum rules / Graph | metadata rules | `PrecisionState` | update; version event | NL/HP read; point-in-time data | all; unknown rejects order | 03/11 |
| Global Market Graph | Own structural topology / Graph | metadata/asset locations | `GraphState`, directed edges | rebuild delta; graph-version event | NL update/HP read; persisted version | all; invalid topology disables route | 03 |
| Route Engine | Own fixed route definitions/economics requests / Graph | Graph, Book/rules | `RouteDefinition`, `RouteEconomics` | evaluate route; candidate/reject events | HP bounded; definitions persisted | all; coherent versions mandatory | 03/04 |
| `pair_to_routes` | Reverse dependency lookup / Graph | route definitions | MarketId→RouteIds index | rebuild/update; index-version event | HP read/NL update; graph artifact | all; invalid index disables affected eval | 03 |
| Global Watcher | Cheap broad awareness / Graph | metadata/BBO/freshness | promotion proposals/anomalies | observe; watcher event | HP/NL cheap; Recorder | all; no trade permission | 03 |
| HWC / Route Activation | Allocate compute relevance / Graph | Watcher, Atlas, reachability | activation snapshot | promote/demote proposal; activation event | NL/HP read; versioned | all; HOT is not safe; validation scoped | 03/16 |
| Quant Feature Engine | Produce bounded features / Quant | Book/trades/versions | `FeatureSnapshot`; `FeatureState` | compute; feature event | HP incremental; L3 persisted | all; stale/unsupported rejected | 05 |
| Formula Core | Canonical QF math / Formula | typed formula inputs | typed deterministic outputs | pure calls; no event/effect | HP pure; golden artifacts | all identical; fail typed/closed; M1 | 04 |
| Opportunity Engine | Detect/classify current candidates / Graph | routes, books, formulas | Opportunity/RejectEpisode | evaluate; opportunity/reject event | HP; L4 evidence | all; no permission; M2/M3 | 03/05 |
| Participant/Survival Engine | Collective forecasts / Participants | features/episodes/artifact | model forecasts | infer; forecast/OOD event | HP bounded inference + OFF training | capability-specific; fallback/shrink | 06 |
| Counterfactual Simulator | Outcome distributions / Simulator | state, plan candidate, forecasts, RNG | `ExecutionForecast`, confidence | simulate bounded; forecast event | HP configured F0/F1/F2/F3; OFF F4/jobs | Replay/Shadow/Live decision support; low confidence narrows | 07 |
| Market Atlas | Rolling economic evidence / Graph+Capital | Recorder/features/opportunities/outcomes | `MarketAtlasState`/version | aggregate; Atlas snapshot event | NL/BG; persisted derived | point-in-time all modes; no direct permission | 03/08 |
| Inventory Engine | Own actual exposure / Inventory | unique fills, balances, reservations | `InventoryState` | reduce fill/reconcile; inventory event | HP commit; journal/checkpoint | all; unknown locks; capital-critical | 08 |
| Capital Reachability | Project usable capital paths / Capital | inventory, graph, Atlas, costs | reachability snapshot | recompute; proposal event | NL/HP read | all; does not change topology/Risk | 08 |
| Terminal Viability | Validate post-state economics / Capital | projected inventory/exits/Risk | viability result | evaluate; reject reason | HP pure/bounded | all; failure rejects normal commitment | 08 |
| Position Sizer | Choose total economic q / Capital | curves, support, capacity, Risk ceiling | size proposal/q curve | size; proposal event | HP bounded deterministic grid | capability scoped; q=0 fail-safe | 08 |
| Portfolio Allocator | Jointly choose eligible candidates / Capital | viable candidates/shared constraints | allocation proposal | allocate; proposal event | HP/NL bounded | later capability; never relaxes Risk | 08 |
| Bridge/Relocation Engine | Propose intentional capital relocation / Capital | Atlas, exits, utility, inventory | Bridge/STAY proposal | evaluate; proposal event | BG/NL slow | later V1; separate validation | 08 |
| Risk Engine | Construct safe action set / Risk | immutable current snapshots | `RiskSnapshot`, `RiskDecision`, kill events | assess/revalidate; risk events | HP; decisions persisted | all; constitutional priority; M1–M5 by action | 09 |
| Reservation Engine | Atomically claim shared capacity / Execution+Inventory | RiskDecision, availability | `ReservationState` | reserve/release; reservation events | HP commit; journal/checkpoint | effect modes/replay; UNKNOWN retains | 10/08 |
| Execution Coordinator | Own plan/route/order lifecycle / Execution | plan, ordered observations | `ExecutionState`, intents | start/continue/cancel; transition events; effects | HP single-writer family; journal | all; stateful; M2–M5 | 10 |
| Execution Transport | Execute external/simulated/no-effect actions / Execution | effect requests | transport observations | send/query/cancel; ACK/fill/error events; network effect | HP I/O; P0 evidence | mode-specific adapter; no permission | 10 |
| Recovery Engine | Choose bounded exit of current exposure / Execution | actual exposure, graph, Risk | `RecoveryState`, recovery plan proposal | recover/replan; recovery events | HP/NL bounded | all effect modes; remains available | 10 |
| Reconciliation Engine | Restore exchange/local consistency / Execution | orders→fills→balances, journal | `ReconciliationState`, reconciled facts | reconcile; consistency/mismatch events; queries | startup/incident HP-adjacent; journal | all; blocks readiness/new risk | 10 |
| Accounting | Attribute realized economic results / Inventory | fills/fees/inventory/classification | PnL/accounting records | close/classify; accounting events | NL/BG; persistent | all; no permission; exact units | 04/08 |
| Recorder | Preserve ordered evidence non-blockingly / Data | RAW/core/execution/decision events | `RecorderState`, chunks/quality | enqueue/rotate; quality events; disk effects | NL/BG; persistent | all; degradation explicit | 12 |
| Replay Engine | Feed historical events into same Core / Data | dataset/manifest/artifacts | `DecisionTrace`, ReplayReport | run/seek; replay events | BG/OFF or test runtime | Replay; deterministic M2 | 12 |
| Model Artifact Manager | Own approved artifact registry view / Models | validation decisions/artifacts | `ModelArtifactState` | stage/promote/demote; artifact events | BG control; immutable artifacts | all consumers; exact support/fallback | 06/16 |
| Capability Manager | Own promoted scope / Validation | EvidenceIds, config, release/license | Capability state/manifest | promote/demote; capability events | BG control/HP read; signed/versioned | all; missing coverage fails closed | 16 |
| Operations / Health | Aggregate observable health / Operations | metrics/events/states | health snapshots/alerts/incidents | alert/ack/runbook; control commands | NL/BG; evidence retained | all; observes, does not trade | 18 |
| Infrastructure Monitor | Own infra health evidence / Infra | feed/clock/CPU/network/disk | `InfraHealthState` | sample; health event | NL/BG/HP snapshot read | all; Risk maps DEGRADED/UNSAFE | 13 |
| Deployment / `botctl` | Lifecycle and local admin / Deployment | operator/config/artifact | deployment state/audit | install/start/stop/update/diagnose | control plane; persistent audit | client runtime; readiness gates | 14 |
| Licensing boundary | Commercial entitlement / Deployment | signed cached license | license state | refresh; entitlement event; network effect BG | BG/cold; cached signed state | Live eligibility only; safety remains | 14 |

The Event/Command/Effect details are normalized in [EVENT_AND_COMMAND_OWNERSHIP_MATRIX.md](EVENT_AND_COMMAND_OWNERSHIP_MATRIX.md). No component listed as a reader may mutate the owner’s state directly.
