# Prompt 2/6 — Functional Architecture Documentary Correction Report

`DOCUMENTATION STATUS: CORRECTED WORKING CANDIDATE — HUMAN REVIEW REQUIRED`

This report is a focused audit/disposition artifact. It does not replace the Master, domain
masters, Formula Book, Risk Constitution, Execution State Machine, Data contracts, PASS 13
catalogs or maintained Architecture Visual Atlas. It records only source-backed documentary
corrections and traceability. No production implementation, test maturity, capability, order or
capital permission is asserted.

## 1. Executive verdict

Verdict: **FUNCTIONALLY SPECIFIED AT DOCUMENTARY M0, WITH OPEN FIELD-LEVEL AND IMPLEMENTATION
DEPENDENCIES**.

- All **42** logical components in the PASS 13 Component Catalog were retained and reviewed.
- All **31** live interfaces in the Domain Interface Catalog were checked producer-to-consumer.
- **46** major documented operations are mapped below. `FOP-*` IDs are documentary locators, not
  verified Rust symbols.
- One active functional contradiction was confirmed and corrected: the Graph master still showed
  Participants/Simulator as an implicit mandatory stage and only one Risk position before Sizing.
  It now matches the owning contracts: required features, capability-specific optional forecasts,
  preliminary Risk, Terminal/Sizing, full Risk, Reservations, immutable plan and pre-send checks.
- The interface catalog lacked an inspectable validity/failure/test dimension. It now records these
  for every interface without inventing wire fields.
- The maintained atlas contains `ARCH-MAP-015..024`, ten module-level functional maps, plus
  `ARCH-MAP-025..037`, thirteen selected operation-level maps after an explicit 46-operation
  complexity assessment. All retain input, decision, owner, version, failure and test anchors.
- No formula, Risk rule, Execution state, current/Future classification or Recorder durability
  claim was changed. `ARCH-016`, `ARCH-019`, `ARCH-026`, `ARCH-027`, Accounting serialization and
  calibrated constants remain open under their existing owners.
- No production source exists in the audited scope and no implementation/runtime evidence was
  established. Documentary completion is not M1/M2/M3/M4/M5 evidence.

## 2. Exact repository snapshot

| Field | Exact value / boundary |
|---|---|
| Branch | `audit-corrections-p1` |
| Prompt-2 original reference/base | `49da9413c49f2be24a0711578d3e3d6763ec1805`; tree `10c99a668b7530c45546a421dd8a6e56bd1d2606` |
| Prompt-2 completion commit | `377e500dfe1d776ea4a57745c9d48c5882f58be8`; tree `910f5fd9e280f3ec52c609396fc5999031dd942f` |
| Current deepening base / upstream | `377e500dfe1d776ea4a57745c9d48c5882f58be8`; `origin/audit-corrections-p1` equal before this delta |
| Current deepening changes | intentionally uncommitted working-tree documentation delta |
| Production code | unchanged; mission edits only `docs_v2/` |
| Unrelated file | untracked `.DS_Store`, preserved and excluded |
| Commit/push/PR | original completion was later pushed by explicit user command; this deepening is not committed, pushed or submitted as a PR |

Primary local sources read for this audit were the full Master Architecture, source-authority,
cross-domain dependency, contradiction and human-decision registers; all ten PASS 13 catalogs;
the Prompt-1 report and both atlases; relevant domain-master sections; and the directly linked deep
contracts for Data, Graph, Formula/Features, Participants, Simulator, Inventory/Capital, Risk,
Execution, Recorder/Replay, Validation and Deployment. The repository—not the focused reports—is
the semantic authority.

Source shorthand used in the matrices is path-stable: `00`, `03`–`14`, and `16`–`19` mean the
same-numbered master in the [`docs_v2` root](../../README.md). Deep references resolve as follows:
`data-02/09` are [RAW/event schemas](../../deep-specs/data/02_RAW_NORMALIZED_AND_DOMAIN_EVENT_SCHEMAS.md)
and [adapter contracts](../../deep-specs/data/09_MODULE_CONTRACTS_ADAPTERS_AND_TESTABILITY.md);
`graph-01/04/05/11` are [topology](../../deep-specs/market-graph/01_STRUCTURAL_GRAPH_VENUES_ASSETS_AND_MARKETS.md),
[route publication](../../deep-specs/market-graph/04_ROUTE_PRECOMPUTATION_PAIR_TO_ROUTES_AND_INVALIDATION.md),
[opportunity economics](../../deep-specs/market-graph/05_OPPORTUNITY_DETECTION_AND_SIZE_DEPENDENT_ECONOMICS.md)
and [route indexing](../../deep-specs/market-graph/11_ROUTE_INDEX_AND_WORK_DEDUP.md);
`micro-06` is the [feature engine](../../deep-specs/market-microstructure/06_INCREMENTAL_FEATURE_ENGINE_AND_HOT_PATH_CONSTRAINTS.md);
`participant-08/09` are [model governance](../../deep-specs/participants/08_MODEL_GOVERNANCE_VALIDATION_OOD_AND_FALLBACK.md)
and [runtime inference](../../deep-specs/participants/09_RUNTIME_INFERENCE_AND_CROSS_DOMAIN_CONTRACTS.md);
`simulator-01/08/12` are [scope](../../deep-specs/simulator/01_PURPOSE_MODES_AND_EPISTEMIC_LIMITS.md),
[scenarios](../../deep-specs/simulator/08_SCENARIOS_MONTE_CARLO_AND_RISK_DISTRIBUTIONS.md) and
[runtime determinism](../../deep-specs/simulator/12_RUNTIME_DATA_CONTRACTS_AND_DETERMINISM.md);
`inv-02/06/08/10` are [reachability/terminal](../../deep-specs/inventory-capital/02_NETFLOW_CAPITAL_REACHABILITY_AND_TERMINAL_VIABILITY.md),
[sizing](../../deep-specs/inventory-capital/06_POSITION_SIZING_VALIDATED_CAPACITY_AND_SEARCH.md),
[shared capacity](../../deep-specs/inventory-capital/08_SHARED_CAPACITY_RESERVATIONS_AND_MULTI_OP_ALLOCATION.md)
and [accounting](../../deep-specs/inventory-capital/10_ECONOMIC_PNL_ACCOUNTING_AND_CAPITAL_EFFICIENCY.md);
`risk-02/05/06` are [eligibility](../../deep-specs/risk/02_MARKET_DATA_AND_ACCOUNT_ELIGIBILITY_GATES.md),
[capital gates](../../deep-specs/risk/05_INVENTORY_CAPITAL_PORTFOLIO_AND_SIZING_GATES.md) and
[decision/revalidation](../../deep-specs/risk/06_RISK_SNAPSHOT_DECISION_TTL_AND_REVALIDATION.md);
`exec-01/04/09/10/11` are [five state machines](../../deep-specs/execution/01_ARCHITECTURE_OWNERSHIP_AND_FIVE_STATE_MACHINES.md),
[reservations/plans](../../deep-specs/execution/04_RESERVATIONS_BALANCES_AND_EXECUTION_PLAN.md),
[Recovery](../../deep-specs/execution/09_RECOVERY_STATE_MACHINE_AND_EXIT_SELECTION.md),
[Reconciliation](../../deep-specs/execution/10_RECONCILIATION_RESTART_AND_CRASH_CONSISTENCY.md) and
[transport](../../deep-specs/execution/11_EXECUTION_TRANSPORT_REPLAY_SHADOW_AND_LIVE.md);
`recorder-01/03/05/06/07` are the numbered files in
[Recorder/Replay](../../deep-specs/recorder-replay/README.md); `deploy-06/08/10/11` are the numbered
files in [Deployment/Security](../../deep-specs/deployment-security/README.md); and `arch-14` is the
[ordered-commit contract](../../deep-specs/architecture/14_ASYNC_CONCURRENCY_AND_ORDERED_COMMIT.md).

## 3. Component coverage

Status legend: `CONFORMANT` means the documentary boundary is coherent; `CORRECTED` means this
mission changed an active representation; `OPEN` means a named owner decision/evidence remains.
Every maturity entry describes documentary status only, not earned runtime maturity.

| Component | Owner | Inputs | Outputs | State | Version | Consumers | Failure | RunMode | Maturity | Source | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Public Feed Adapter | Data | public payload, connection, Clock | RAW-linked market observations/health | connection only | source/connection/schema | Normalizer, Recorder | invalid/gap quarantines scope | all sources; Live adapter only in live modes | M0; M1+ required | `11`, `12`; data-02 | `CONFORMANT` |
| Account Adapter | Execution + Data | authenticated order/fill/balance payload | account events/health | connection only | account source/schema | Account/Execution reducers, Recorder | ambiguity blocks affected new risk | effect modes; replay adapter isolated | M0; M1/M2+ required | `10`, `11` | `CONFORMANT` |
| Metadata Adapter | Graph + Data | market/rule payload | metadata events | connection/cache only | metadata/schema/source | Metadata/Fee/Precision | unknown rule fails closed | all | M0; M1+ required | `03`, `11` | `CONFORMANT` |
| Normalizer | Data | provisional/final RAW evidence | typed L1 event or rejection | none | RAW + normalization schema | ordered reducers, audit | no guessed event or mutation | all | M0; M1 required | `11`; data-02/09 | `CONFORMANT` |
| Clock | Data + Infrastructure | wall/monotonic/exchange/replay time | time/quality and `TimerEvent` | clock service | clock policy/quality | every time-dependent consumer | unhealthy narrows/blocks scope | mode-specific implementation | M0; M1/M2 required | `11`, `13` | `CONFORMANT` |
| Ordered Event Coordinator | Data | `EngineInputEvent`, worker result | ordered commits/effect requests | ordering cursor; not second domain truth | capture cursor + state generations | all reducers/effects | stale/deadline result rejected | isolated instance per run | M0; deterministic M2 required | `00`, `11`, arch-14 | `CONFORMANT` |
| Book Engine | Graph/Data boundary | ordered market events | `BookState`, `BookSnapshot` | sole Book writer | Book/source/metadata | Graph, Features, Opportunity, Simulator, Risk | stale/gap/crossed -> non-ready | all, isolated state | M0; M2/M3 evidence required | `03`, `11` | `CONFORMANT` |
| Metadata Engine | Graph | metadata events | `MetadataState` | sole Metadata writer | MetadataVersion | Graph, Formula, Precision, Execution | unknown disables affected scope | all | M0 | `03`, `11` | `CONFORMANT` |
| Fee Engine | Formula | fee/account rules | `FeeState` | sole Fee writer | FeeVersion/effective time | Formula, Opportunity, Risk, Accounting | unknown rejects economics | all | M0; external refresh required | `04`, `05`, `11` | `CONFORMANT` |
| Precision Engine | Graph | metadata rules | `PrecisionState` | sole Precision writer | Metadata/Precision version | Formula, Sizer, Execution, Recovery | unknown rejects order/economics | all | M0; external refresh required | `03`, `04`, `11` | `CONFORMANT` |
| Global Market Graph | Graph | MetadataState, asset locations | directed topology/`GraphState` | sole topology writer | GraphVersion | Route, Watcher, Atlas, Capital, Recovery | invalid topology disables affected conversions | all, point-in-time | M0 | `03`; graph-01 | `CONFORMANT` |
| Route Engine | Graph | Graph + current Book/rules | definitions and economics requests/results | sole Route generation writer | Graph/Route/index generation | Opportunity, Execution, Replay | mixed generation withheld | all | M0; atomicity test absent | `03`; graph-04/05 | `CORRECTED` |
| `pair_to_routes` | Graph/Route | RouteDefinitions | MarketId -> RouteIds lookup | immutable generation artifact | index generation + canonical IDs | affected-route evaluation | invalid/stale index disables evaluation | all | M0 | `03`; graph-04/11 | `CONFORMANT` |
| Global Watcher | Graph | metadata/BBO/freshness | anomaly/promotion proposal | watcher state only | input/Watcher version | HWC, Recorder | proposal never grants trade | all | M0 | `03` | `CONFORMANT` |
| HWC / Route Activation | Graph | Watcher, Atlas, reachability | activation snapshot | activation policy state | Atlas/activation/config | route compute scheduling | HOT never means safe | all | M0; thresholds calibrated | `03`, `16` | `CONFORMANT` |
| Quant Feature Engine | Quant | Book/trades/versions | `FeatureSnapshot` | sole Feature writer | input/window/Formula | Participants, Simulator, Risk, Atlas | gap/stale invalidates dependent feature | all | M0; parity required | `05`; micro-06 | `CONFORMANT` |
| Formula Core | Formula | typed QF inputs | typed deterministic results | none/pure | FormulaVersion + rules | all economics consumers | typed invalid/fail-closed | identical all modes | M0; M1 goldens required | `04` | `CONFORMANT` |
| Opportunity Engine | Graph/Quant | routes, Books, formulas/features | Opportunity/RejectEpisode | opportunity evidence only | all economic inputs | Recorder, models, Simulator, Sizer, Risk | typed reject; no permission | all | M0; M2/M3 target | `03`, `05`; graph-05 | `CORRECTED` |
| Participant/Survival Engine | Participants | supported features/episodes/artifact | forecasts/confidence/OOD | artifact refs/forecast state | feature/model/support | Simulator, Risk, Sizer, Atlas, Infra | fallback only in own support; else reject dependent scope | capability-specific | M0; calibration absent | `06`; participant-08/09 | `CONFORMANT` |
| Counterfactual Simulator | Simulator | candidate/state/forecasts/RNG | `ExecutionForecast`/confidence | branch/result state only | q/state/fidelity/model/seed | Sizer, Risk, Validation | non-finite/OOD/unsupported -> reject/narrow | Replay/Shadow support; F4 offline | M0; fidelity evidence absent | `07`; simulator-01/08/12 | `CONFORMANT` |
| Market Atlas | Graph + Capital | recorded features/opportunities/outcomes | `MarketAtlasState`/snapshot | sole Atlas writer | AtlasVersion/support | HWC, Capital, Risk, research | stale evidence cannot replace current truth | point-in-time all modes | M0; learned/calibrated | `03`, `08` | `CONFORMANT` |
| Inventory Engine | Inventory | unique fills, balances, reservations | `InventoryState` | sole Inventory writer | Inventory/Account/Fill cursor | Capital, Sizer, Risk, Accounting | unknown/mismatch locks dependent scope | all, isolated state | M0; exact-once tests absent | `08`, `10`, `11` | `CONFORMANT` |
| Capital Reachability | Capital | Inventory, Graph, Atlas, costs/claims | reachability snapshot | derived proposal state | all dependency versions | Terminal, Sizer, Bridge | absent path/support -> unavailable | all | M0 | `08`; inv-02 | `CONFORMANT` |
| Terminal Viability | Capital | projected inventory, exits, Risk/support | viability/reject result | none/pure | state/exit/model versions | Sizer, Portfolio, Risk | hard band/no exit/OOD rejects | all | M0 | `08`; inv-02 | `CONFORMANT` |
| Position Sizer | Capital | curves, support, capacity, Risk ceiling | candidate curve/q proposal | no permission state | q/state/model/capability | Portfolio, Risk, Reservation evidence | no feasible q -> no action | capability-specific | M0; search evidence absent | `08`; inv-06 | `CONFORMANT` |
| Portfolio Allocator | Capital | viable candidates/shared constraints | allocation proposal | no Risk/Reservation state | candidate/resource/policy | Risk, Reservation | overlap/unknown dependence restricts/rejects | later capability | M0; Later V1 | `08`; inv-08 | `CONFORMANT` |
| Bridge/Relocation Engine | Capital | Atlas, exits, utility, Inventory | MOVE/STAY proposal | relocation proposal state | Atlas/inventory/economic policy | Risk, Execution, Accounting | fail closed on cost ownership/no terminal viability | Later V1 only | M0; deferred activation | `08` | `CONFORMANT` |
| Risk Engine | Risk | immutable current snapshots/forecasts/proposals | `RiskSnapshot`, `RiskDecision`, kills | sole Risk writer | snapshot/config/model/capability/TTL | Reservation, Execution, Recovery, Ops | hard reject/halt/recovery-only; mixed input invalid | all | M0; action-scoped M1–M5 needed | `09`; risk-02/05/06 | `CONFORMANT`; ARCH-026 `OPEN` |
| Reservation Engine | Execution + Inventory | RiskDecision + current capacity | `ReservationState` | sole claim writer | account/book/risk/lifecycle | Risk, Execution, Capital, Reconciliation | atomic conflict rejects; UNKNOWN retains | effect modes + Replay | M0; schema/tests absent | `10`, `08`; exec-04 | `OPEN` ARCH-027 |
| Execution Coordinator | Execution | plan + ordered observations | Execution state/intents/effects | sole execution-family writer | plan/order/state/dependencies | Transport, Recovery, Accounting evidence | stale/invalid/unknown follows five machines | all | M0; M2–M5 required | `10`; exec-01 | `CONFORMANT` |
| Execution Transport | Execution | authorized effect requests | ACK/status/fill/error observations | connection only | request/intent/mode | ordered Execution/Account reducers | timeout may be UNKNOWN; never grants permission | mode-specific | M0; external/parity tests absent | `10`; exec-11 | `CONFORMANT` |
| Recovery Engine | Execution | actual exposure, current Graph/Book, Risk | recovery state/plan proposal | sole Recovery writer | exposure/plan/limits | Risk, Execution, Accounting, Ops | no safe plan/exhaustion -> fail/escalate | effect modes + Replay | M0; evidence absent | `10`; exec-09 | `CONFORMANT` |
| Reconciliation Engine | Execution | orders, fills, balances, journal | consistency/mismatch/readiness facts | sole Reconciliation writer | reconciliation/account cursors | readiness, Risk, Inventory, Ops | unresolved blocks scope and retains claims | all; mandatory startup | M0; fault tests absent | `10`; exec-10 | `CONFORMANT` |
| Accounting | Inventory/Accounting authority | fills, fees, capital flows, valuations/classes | disjoint accounting records | sole Accounting writer | action/entry/ledger/valuation | Ops, Validation, research | duplicate/conflict reconciles; prediction excluded | all | M0; serialized schema open | `04`, `08`; inv-10 | `OPEN` field schema |
| Recorder | Data | RAW/core/execution/decision evidence | chunks/journal/quality/`RecorderState` | sole Recorder writer | sequence/chunk/checksum/quality | Replay, Validation, Ops | explicit drop/gap; P0 threat stops new risk | all | M0; durability proof absent | `12`; recorder-01/03/05 | `OPEN` ARCH-019 |
| Replay Engine | Data | Dataset/RunManifest/artifacts | isolated state, `DecisionTrace`, report | Replay-only C0/domain state | run/dataset/config/model/formula/seed | Validation/research/audit | no Live mutation/Transport; divergence invalid | Replay only | M0; M2 evidence absent | `12`; recorder-06/07 | `CONFORMANT` |
| Model Artifact Manager | Models | artifacts + validation decisions | immutable artifact registry state | sole artifact-state writer | artifact/hash/support/approval | Participants, Simulator, Risk, Replay | corrupt/mismatched/unapproved rejected | all consumers | M0; promotion absent | `06`, `16` | `CONFORMANT` |
| Capability Manager | Validation | EvidenceIds/config/release/license | signed capability state/manifest | sole capability writer | exact scope/evidence/version | Deployment, Risk, Execution, Ops | missing/stale scope fails closed | all | M0; no activation | `16` | `CONFORMANT` |
| Operations / Health | Operations | metrics/events/states | health/alerts/incidents/runbook commands | operations evidence only | metric/policy/incident | operator, Risk/Execution inputs | observes; cannot trade or clear maturity alone | all | M0 | `18` | `CONFORMANT` |
| Infrastructure Monitor | Infrastructure | clock/feed/CPU/network/disk/Recorder | `InfraHealthState` | sole infra-health writer | instance/observation/policy | Risk, Execution, Validation, Ops | `DEGRADED` narrows; `UNSAFE` blocks new risk | all | M0; thresholds calibrated | `13` | `CONFORMANT` |
| Deployment / `botctl` | Deployment | operator/config/artifact/evidence | lifecycle/readiness/audit | deployment state only | digest/config/installation/owner | Runtime, Validation, Ops | non-ready/reconcile; no dual owner | client runtime | M0; tooling unimplemented | `14`; deploy-06/08/10/11 | `CONFORMANT` |
| Licensing boundary | Deployment | cached signed entitlement/clock quality | license state/event | sole license-state writer | entitlement/install/time policy | runtime capability intersection | loss blocks new risk, preserves safety paths | Live eligibility only | M0; policy open | `14` | `CONFORMANT` |

## 4. Interface coverage

The maintained [Domain Interface Catalog](../pass13_master_architecture/DOMAIN_INTERFACE_CATALOG.md)
now contains the full validity/failure and acceptance anchors. The matrix below confirms all 31
rows; “correction” means a documentary catalog clarification, not schema or implementation change.

| Interface | Producer | Consumers | Type / meaning | Version | Validity | Failure | Correction | Test |
|---|---|---|---|---|---|---|---|---|
| `RawEvent` | adapters + ingress; Recorder persists | Normalizer, Replay, audit | immutable locally observed source evidence | RAW/schema/capture/seq | one identity/sequence | retain reject/gap; no mutation | validity + crash gap added | `FUNC-001/021/028` |
| Normalized events | Normalizer | ordered reducers | typed L1 event linked to RAW | normalization + RAW ID | schema/required fields valid | typed reject | failure/test added | `FUNC-001/003/025` |
| `BookSnapshot` | Book | Graph/Features/Opportunity/Simulator/Risk | immutable coherent L2 view | Book/source/metadata | ready, fresh, gap-free | market non-ready | readiness added | `FUNC-004/008` |
| Metadata/Fee/Precision snapshots | owning engines | Graph/Formula/Sizer/Execution | effective point-in-time rules | rule versions | known/current | fail closed; rebuild/invalidate | change class added | `FUNC-005/009/029` |
| `RouteDefinition` / index | Graph/Route | Opportunity/Execution/Replay | ordered legs + dependencies | coherent generation | complete bidirectional generation | withhold/reject stale | atomicity added | `FUNC-005/031` |
| `RouteEconomics` | Route/Formula | Opportunity/Sizer/Risk/evidence | q-specific exact conversion | Book/rules/Formula/Route | units/side/depth valid | typed economic reject | failures added | `FUNC-006..009/030` |
| `FeatureSnapshot` | Feature | models/Simulator/Risk/Atlas | bounded point-in-time features | state/window/formula | supported/fresh | invalidate/fallback/reject | support added | `FUNC-003/010/031` |
| Opportunity/RejectEpisode | Opportunity | Recorder/models/Simulator/Validation | exact-valid observation or reject | all economic inputs | comparator/classification valid | explicit rejection | no-authority added | `FUNC-007/008/013` |
| `EdgeSurvivalForecast` | Participants | Simulator/Risk/Sizer/Infra | supported horizon distribution | model/support/q | current/in support | own fallback or reject scope | fallback added | `FUNC-010/030` |
| liquidity/cross-market/maker forecasts | Participants | Simulator/Execution/Risk/Atlas | scoped distributions | model/horizon/fidelity | supported dependency | missing is not zero | failure added | `FUNC-010/024/030` |
| `ExecutionForecast` | Simulator | Sizer/Risk/evidence | F/P/R/X PnL/tail distribution | q/state/fidelity/seed/model | finite/reproducible/supported | reject/narrow; never actual | validity added | `FUNC-006/010/013/030` |
| `MarketAtlasSnapshot` | Atlas | HWC/Capital/Risk/research | rolling economic evidence | Atlas/support | point-in-time supported | cannot replace current truth | authority added | `FUNC-003/010/024` |
| `AccountSnapshot` | Account/Reconciliation | Inventory/Reservation/Risk/Execution | observed account truth | Account/reconciliation | consistent | retain locks/block risk | non-trade/unknown added | `FUNC-015/019/020/027` |
| `InventoryState` | Inventory | Terminal/Sizer/Portfolio/Risk/Accounting | actual exposure | Inventory/Fill/Account | unique actual facts | duplicate no-op; uncertainty locks | non-mutation added | `FUNC-002/017/020/027` |
| Reachability/Terminal | Capital engines | Sizer/Portfolio/Risk | post-claim path/terminal result | inventory/graph/exit/model | credible exit/gates | reject/downsize | failure added | `FUNC-011/030` |
| Size/allocation proposal | Sizer/Allocator | Risk/Reservation/trace | audited q candidates/shared demand | q/state/policy | exact candidate passes | no action/recompute/reject | no-permission added | `FUNC-011/012/030` |
| `RiskSnapshot` / `RiskDecision` | Risk | Reservation/Execution/Recovery/Data/Ops | immutable authorization result | dependency/config/TTL | compatible/current action | fail closed; no boolean-only send | ARCH-026 preserved | `FUNC-003/013/030` |
| `ReservationState` | Reservation | Risk/Execution/Capital/Reconciliation | owned capacity claims | lifecycle/resource versions | atomic/current | conflict/UNKNOWN lock | ARCH-027 preserved | `FUNC-012/015/017` |
| `ExecutionPlan` | Execution boundary | Coordinator/Replay/Recorder | immutable authorized plan | plan/dependency | envelope current | new version/abort/reconcile | immutability added | `FUNC-003/011/017/026` |
| `OrderIntent` / effect | Execution | Transport | quantized stable intent | intent/plan/Risk | permission + claims + mode | no effect | distinction added | `FUNC-013/014/026` |
| order/fill/cancel observations | Transport/adapters | ordered reducers | external observations | request/external/provenance | unique/typed | UNKNOWN/cancel nonterminal | ambiguity added | `FUNC-014..016/026` |
| FillLedger | Account/Execution | Inventory/Recovery/Accounting/Replay | append-only actual unique fills | fill cursor/IDs | idempotent | reconcile incompatible evidence | truth boundary added | `FUNC-017/019/020` |
| Recovery plan/state | Recovery | Risk/Execution/Accounting/Ops | bounded current-exposure action | exposure/plan/limits | Risk-reducing/current | fail/escalate/replan | no route loyalty added | `FUNC-018` |
| Reconciliation state/report | Reconciliation | readiness/Risk/Inventory/Ops | orders-fills-balances proof | reconciliation/account | consistent | unresolved locks/stops | order of truth added | `FUNC-015/019/032` |
| Accounting record | Accounting | Ops/Validation/research | disjoint actual/economic attribution | entry/action/valuation | unique actual/provenance | reconcile duplicate/conflict | non-trade separation retained | `FUNC-020/027` |
| `RunManifest` | Data/Replay/Deployment | Replay/Validation/research | exact run closure identity | build/config/model/formula/schema/seed | complete/resolvable | non-reproducible evidence | no authority added | `FUNC-022/023/025` |
| `DecisionTrace` | ordered Core | Replay/Validation/incidents | ordered decisions/intents/transitions | run/cursors/hashes | deterministic | first divergence reported | scheduling failure added | `FUNC-022/025/031` |
| `ModelArtifact` | Model Manager | Participants/Simulator/Risk/Replay | immutable supported artifact | hash/schema/support/approval | integrity/support/approval | reject dependent scope | existence vs promotion added | `FUNC-010/023/030` |
| `CapabilityManifest` | Validation/Capability | Deployment/Risk/Execution/Ops | exact validated scope | evidence/market/mode/q/model/infra | current subset | fail closed | intersection added | `FUNC-023/024/030` |
| health snapshot | Infra/Ops | Risk/Execution/Validation | resource/clock/feed/Recorder health | instance/observation/policy | current/observable | narrow/unsafe; no auto-promotion | severity distinction added | `FUNC-013/021/032` |
| Evidence/Validation/Incident | Validation/Ops | Capability/Release/operator | immutable proof/disposition | evidence/scope/provenance | complete/current | retain negative; no promotion | failure added | `FUNC-023/024/032` |

## 5. Function/operation inventory

Every `FOP-*` row below means **DOCUMENTED OPERATION — NO IMPLEMENTATION NAME VERIFIED**. The
identifier is a navigation locator only; it neither freezes a serialized API nor asserts that a
Rust function exists. Exact wire fields remain under Data authority. `C0–C5` denotes the existing
timing class where the source fixes one; otherwise the row records that implementation allocation
must be established by Prompt 3 rather than invented here.

| ID | Component / operation / purpose | Owner / source / ARCH | Inputs and preconditions | Processing and decision | Outputs / state effect | Commands, events, effects | Versions | Failure result | Timing / modes / maturity | Acceptance |
|---|---|---|---|---|---|---|---|---|---|---|
| `FOP-A01` | Public Feed Adapter — capture, subscribe and reconnect without owning Book truth | Data; `11`, data-02; ARCH-001/002/014/016 | external payload/connection/Clock; source identified | capture provisional bytes/provenance; admitted sequence/final RAW identity remains independent of normalization completion; reconnect restores only after data rules pass | RAW-linked observation/health; connection state only | consumes external payload; emits ingress evidence; no trading effect | source, connection, RAW/schema, cursor | reject/gap and market-scoped non-readiness; never guess | ingress boundary; Live source or Replay equivalent; M0 | `FUNC-001/004/028` |
| `FOP-A02` | Account Adapter — observe authenticated orders, fills and balances | Execution + Data; `10`, `11`; ARCH-005/016 | authenticated payload; account/source known | capture and normalize observations; distinguish ACK/status/fill/balance | account observation/health; connection state only | emits ordered observations; no canonical account mutation in callback | source/schema/account cursor/request identity | ambiguity becomes UNKNOWN/reconciliation input; block affected risk | effect modes; isolated replay source; M0 | `FUNC-014..020/027` |
| `FOP-A03` | Metadata Adapter — acquire point-in-time exchange rules | Graph + Data; `03`, `11`; ARCH-014/015 | source payload and effective-time provenance | validate and emit metadata event | metadata observation; cache/connection only | emits metadata event; no Graph mutation | source/schema/effective time | unknown/invalid rule disables affected scope | all modes through mode source; M0 | `FUNC-001/005/029` |
| `FOP-A04` | Normalizer — convert RAW evidence to typed event or rejection | Data; `11`, data-02/09; ARCH-001/002/014 | provisional captured bytes/provenance and supported schema | validate required fields, units and provenance; join one typed outcome to the final RAW identity before reducer admission | normalized event or typed rejection; no state | consumes captured evidence; emits `EngineInputEvent` candidate/rejection | RAW ID, normalization/schema version | invalid input cannot reach reducer or mutate state | ingress C-class to allocate; all; M0 | `FUNC-001/025` |
| `FOP-A05` | Clock — supply mode-correct time and explicit timers | Data + Infrastructure; `11`, `13`; ARCH-014/020 | wall/monotonic/exchange/replay sources; clock quality known | map mode time, evaluate quality, create `TimerEvent` | time/quality/timer; Clock service state only | emits ordered timer events; no economic effect | clock policy, observation, run mode | unhealthy clock narrows/blocks affected capability | C0 timer source; mode-specific; M0 | `FUNC-025/026` |
| `FOP-A06` | Ordered Event Coordinator — serialize canonical commits | Data/Core; `00`, `11`, arch-14; ARCH-002/004/016 | `EngineInputEvent`/worker result; sequence and dependency versions valid | order, dispatch reducer, validate worker completion, commit or reject | committed domain transition/effect request; ordering cursor only | accepts events/results; emits commands/effect requests | capture cursor and state generations | stale/deadline result rejected; no callback commit | C0; one isolated instance per run; M0 | `FUNC-002/025/031` |
| `FOP-A07` | Recorder — accept prioritized evidence and persist inspectably | Data; `12`, recorder-01/03/05; ARCH-001/019 | P0–P3 evidence, bounded handoff, Recorder health | prioritize, chunk/journal, checksum, persist and expose quality/gaps | durable evidence/quality/`RecorderState`; Recorder sole writer | consumes evidence; emits health/gap/stop signal; no economic effect | sequence, chunk, checksum, schema, priority | no silent P0 loss; durability threat stops new risk; crash gap explicit | off-C0 handoff with P0 safety; all; M0 | `FUNC-021/028` |
| `FOP-A08` | Replay — reconstruct one isolated run deterministically | Data; `12`, recorder-06/07; ARCH-011/020 | dataset/manifest/artifacts/config/seed complete | instantiate isolated Core, feed ordered evidence/timers, compare trace | Replay-only states, `DecisionTrace`, report | consumes recorded events; no Live transport/effects | run/dataset/build/config/model/formula/schema/seed | missing input/divergence invalidates evidence | Replay only; C0 semantics reproduced; M0 | `FUNC-022/025` |
| `FOP-B01` | Book reducer — build coherent L2 snapshots | Graph/Data boundary; `03`, `11`; ARCH-002/014 | ordered valid market event and current source/metadata | apply snapshot/delta rules; detect gap, invalid/crossed/stale state | `BookState`/`BookSnapshot`; sole Book writer | consumes market event; emits snapshot/readiness change | Book, source cursor, metadata, timestamp | market non-ready; no invented liquidity | C0 state commit; all; M0 | `FUNC-001/004/008` |
| `FOP-B02` | Metadata Engine — publish effective exchange rules | Graph; `03`, `11`; ARCH-014/015 | valid metadata event/effective time | validate transition and classify structural/precision/fee impact | `MetadataState`; sole writer | consumes metadata event; emits invalidation/rebuild input | MetadataVersion/effective time | affected scope disabled until known compatible state | C0 commit; all; M0 | `FUNC-003/005/029` |
| `FOP-B03` | Fee Engine — resolve fee asset/rate/timing for economics | Formula; `04`, `05`, `11`; ARCH-014/015 | point-in-time fee/account rules | select source-owned fee contract without unit collapse | `FeeState`; sole writer | consumes rule events; no effect | FeeVersion/effective time/account context | unknown fees reject economics | pure/C0 snapshot use; all; M0 | `FUNC-006/009/020` |
| `FOP-B04` | Precision Engine — apply source-owned quantization constraints | Graph; `03`, `04`, `11`; ARCH-014/015 | effective market precision rules | validate/quantize through Formula-owned semantics | `PrecisionState` and typed result; sole writer for state | consumes rule event; no external effect | Metadata/Precision version | invalid/unknown precision rejects calculation/order | pure/C0 snapshot use; all; M0 | `FUNC-003/006/029` |
| `FOP-B05` | Global Market Graph — construct directed structural topology | Graph; `03`, graph-01; ARCH-003/015 | coherent MetadataState and asset locations | generate directed nodes/edges; exclude disabled/invalid markets | `GraphState`; sole topology writer | consumes structural change; emits generation candidate | GraphVersion + MetadataVersion | invalid topology or mixed input not published | worker candidate, C0 atomic commit; all; M0 | `FUNC-005/031` |
| `FOP-B06` | Route Engine — derive definitions and request q-specific economics | Graph; `03`, graph-04/05; ARCH-003/015 | Graph generation; compatible rules/books for economics | enumerate/classify definitions; evaluate only through Formula/NetConvert | RouteDefinitions/economic result; sole route-generation writer | consumes graph/snapshot inputs; emits route generation/opportunity input | Graph/Route/index generation + economic versions | stale generation withheld; typed economic rejection | worker candidate + C0 commit; all; M0 | `FUNC-005..009/031` |
| `FOP-B07` | `pair_to_routes` — find exactly affected routes | Graph/Route; `03`, graph-04/11; ARCH-003/015 | complete RouteDefinitions of one generation | build immutable MarketId→RouteIds reverse index | reverse index generation; part of route publication | lookup only; no mutation/effect | same generation and canonical IDs | missing/stale entry disables affected evaluation | C0 lookup; all; M0 | `FUNC-005/031` |
| `FOP-B08` | Global Watcher — propose anomaly/promotion attention | Graph; `03`; ARCH-014/022 | metadata/BBO/freshness observations | evaluate watcher policy and evidence quality | anomaly/promotion proposal; watcher state only | emits proposal/evidence; never trade command | input/Watcher/policy versions | invalid input means no promotion and explicit evidence | monitoring class; all; M0 | `FUNC-004/023/024` |
| `FOP-B09` | HWC / Route Activation — allocate compute priority, not permission | Graph; `03`, `16`; ARCH-022/024 | Watcher/Atlas/reachability and capability scope | classify activation/priority under configured policy | activation snapshot; activation-policy state | scheduling command only; no order effect | Atlas/activation/config/capability | stale/unsupported input keeps route cold/disabled | scheduling class; all; M0/calibration open | `FUNC-010/023/024` |
| `FOP-B10` | Market Atlas — aggregate point-in-time empirical evidence | Graph + Capital; `03`, `08`; ARCH-021/022 | recorded features/opportunities/outcomes/support | aggregate without replacing current market/account truth | `MarketAtlasState`/snapshot; sole Atlas writer | consumes evidence; read-only to execution | AtlasVersion/support/provenance | stale/unsupported evidence excluded or scoped | off-C0 evidence; all; M0 | `FUNC-003/010/024` |
| `FOP-C01` | Formula Core — execute QF-001..110 semantics exactly | Formula; `04`; ARCH-007/014 | typed units, sides, rules and domain preconditions | apply source-owned deterministic equation/rounding/fee rules | typed value or typed rejection; no state | no command/effect | FormulaVersion + all input versions | non-finite/unit/domain/depth error rejects | pure C0/C1 candidate; identical modes; M0 | `FUNC-006/008/009` |
| `FOP-C02` | NetConvert — walk one directed conversion at q | Formula; `04`; ARCH-007/014 | side-correct coherent L2, q, fees, precision | consume bid for base→quote or ask for quote→base; chain gross→fees→net→quantized | size-specific conversion or reject; no state | no command/effect | Book/Fee/Precision/Formula | insufficient depth/invalid unit/unknown fee rejects | pure; all; M0 | `FUNC-006/008/009` |
| `FOP-C03` | Opportunity Engine — compare executable route and required baseline | Graph/Quant; `03`, `05`, graph-05; ARCH-003/007 | definition, coherent q economics, comparator and classification inputs | validate OWA/TT class, compute exact comparison, preserve reject reason | Opportunity or RejectEpisode; evidence only | emits observation/evidence, never permission | route/books/rules/formula/q | invalid comparator, depth, versions or class → reject | C0/C1 candidate; all; M0 | `FUNC-005..009/013` |
| `FOP-C04` | Quant Feature Engine — produce bounded point-in-time features | Quant; `05`, micro-06; ARCH-014/021 | coherent books/trades/window definitions | compute exact documented feature set and support flags | `FeatureSnapshot`; sole writer | consumes market events; no effect | input cursors/window/FormulaVersion | gap/stale/OOD invalidates dependent feature | C0/C1 candidate; all; M0 | `FUNC-003/010/031` |
| `FOP-C05` | FastL1/BBO-C2 — accelerate or prove rejection without changing semantics | Graph/Quant; `03`, `05`; ARCH-007/014 | fresh BBO and documented eligibility/fallback condition | run exact parity-safe shortcut or fall back to full L2; BBO may prove impossibility only | parity-compatible result/fallback/reject; no state | no effect | BBO/Book/Formula/route versions | ambiguity/staleness forces full path or rejection | fast C-class to benchmark; all; M0 | `FUNC-006/007/008` |
| `FOP-D01` | Participant/survival inference — forecast only inside support | Participants; `06`, participant-08/09; ARCH-021/022 | supported FeatureSnapshot, q/horizon and approved artifact | check support/OOD then infer calibrated distribution | survival/participant forecast + confidence/OOD; forecast state only | no trade command/effect | feature/model/support/horizon/q | own fallback only where defined; otherwise dependent scope rejects | worker/off-C0; capability-specific; M0 | `FUNC-010/030/031` |
| `FOP-D02` | Liquidity/cross-market/maker inference — scoped empirical forecasts | Participants; `06`; ARCH-021/022 | supported features/artifact/fidelity | infer only defined target and distinguish missing from zero | typed forecast/confidence/OOD; forecast state only | no effect | model/support/horizon/fidelity | unavailable/unsupported blocks only requiring capability | worker/off-C0; optional/Future as declared; M0 | `FUNC-010/024/030` |
| `FOP-D03` | Counterfactual Simulator — evaluate synthetic execution branches | Simulator; `07`, simulator-01/08/12; ARCH-021/022 | candidate/current state/required forecasts/RNG and supported q | execute F0–F3 branch under fidelity contract; F4 stays Research | `ExecutionForecast`/confidence/trace; branch state only | synthetic events only; never actual fill/effect | q/state/fidelity/model/seed | non-finite/OOD/unsupported → reject/narrow, not actual mutation | worker; Replay/Shadow/support scope; M0 | `FUNC-006/010/013/030` |
| `FOP-D04` | Model Artifact Manager — validate identity and promotion status | Models/Validation; `06`, `16`; ARCH-021/022/024 | artifact/hash/schema/support and approval evidence | verify integrity, compatibility and exact approved scope | immutable artifact registry state; sole writer | accepts promotion decision; emits registry event | artifact/hash/schema/support/approval | corrupt/mismatched/unapproved artifact rejected | off-C0; all consumers; M0 | `FUNC-010/023/030` |
| `FOP-E01` | Inventory Engine — derive actual exposure from unique evidence | Inventory; `08`, `10`, `11`; ARCH-005/008 | unique fills, proven balances, reservations and classifications | idempotently apply actual facts; distinguish pending/non-trade flows | `InventoryState`; sole writer | consumes fill/account events; no order effect | Inventory/Fill/Account/reservation cursor | conflict/unknown locks affected capacity; forecast ignored | C0 commit; all; M0 | `FUNC-002/017/019/020/027` |
| `FOP-E02` | Capital Reachability — identify feasible conversion/exit paths | Capital; `08`, inv-02; ARCH-008 | Inventory, Graph, Atlas, costs and retained claims | compute reachable capacity under actual dependencies | reachability snapshot/proposal state | no permission/effect | inventory/graph/atlas/cost versions | absent path/support → unavailable | pure/worker candidate; all; M0 | `FUNC-003/011/030` |
| `FOP-E03` | Terminal Viability — enforce terminal exposure constraints | Capital; `08`, inv-02; ARCH-008/009 | projected actual-plus-proposed inventory, exits, support/Risk constraints | evaluate terminal band/credible exit/OOD | viability or typed rejection; no state | no effect | state/exit/model/policy versions | hard band/no credible exit/OOD rejects | pure; all; M0 | `FUNC-011/013/030` |
| `FOP-E04` | Position Sizer — find bounded validated q candidates | Capital; `08`, inv-06; ARCH-008/009 | economic curves, support, depth/capacity, Risk ceiling | search documented q domain/`Q_validated`, recompute exact economics and terminal feasibility | candidate curve/q proposal; no permission | emits proposal only | q/state/model/capability/formula | no feasible q → no action; calibrated search remains open | worker; capability-specific; M0 | `FUNC-011/012/030/031` |
| `FOP-E05` | Portfolio Allocator — arbitrate shared candidate resources | Capital; `08`, inv-08; ARCH-008/009 | viable candidates and shared dependency/capacity map | select proposal without exceeding shared constraints | allocation proposal; no Reservation/Risk state | emits proposal only | candidate/resource/policy | overlap/unknown dependency restricts/rejects | Later V1 worker; disabled unless capability; M0 | `FUNC-012/024` |
| `FOP-E06` | Bridge/Relocation — compare MOVE versus STAY without baseline promotion | Capital; `08`; ARCH-008/009 | Atlas, current Inventory, credible exits, utility/cost ownership | evaluate Later-V1 relocation economics/terminal viability | MOVE/STAY proposal; no permission | proposal only; effect still requires Risk/Execution | atlas/inventory/economic policy | unknown costs/no exit/support → fail closed | Later V1 only; M0 | `FUNC-020/024/030` |
| `FOP-F01` | Risk Engine — preliminary eligibility and full action authorization | Risk; `09`, risk-02/05/06; ARCH-006/009/026 | immutable compatible snapshots/forecasts/proposal/current health/capability | cheap/preliminary gates, then full constitutional/action checks; create typed decision | `RiskSnapshot`/`RiskDecision`/kills; sole Risk writer | accepts evaluation command; emits decision/halt, never transport effect | dependencies/config/model/capability/TTL | hard reject/halt/recovery-only; mixed/stale input invalid; field mapping open | C0 decision; all; M0 | `FUNC-003/013/030` |
| `FOP-F02` | Reservation Engine — atomically claim shared capacity | Execution + Inventory boundary; `10`, `08`, exec-04; ARCH-006/009/027 | compatible RiskDecision and current balance/book/Risk capacity | check and atomically commit lifecycle claim before any new effect | `ReservationState`; sole claim writer | accepts reserve/release command; no exchange effect | account/book/risk/lifecycle | conflict rejects; UNKNOWN retains; schema fields remain open | C0; effect-capable modes + Replay semantics; M0 | `FUNC-012/015/017` |
| `FOP-F03` | Execution Coordinator — run the five canonical state machines | Execution; `10`, exec-01; ARCH-004/005/006/010 | authorized immutable plan and ordered observations | transition only through documented machines; revalidate current dependencies and later legs | execution state/intents/effect requests; sole execution-family writer | consumes events/commands; emits authorized effect request | plan/order/state/dependencies | stale/invalid/UNKNOWN follows state-machine failure path | C0; all isolated modes; M0 | `FUNC-003/014..018/026` |
| `FOP-F04` | Execution Transport — perform only authorized mode-correct effects | Execution; `10`, exec-11; ARCH-005/006/010 | current authorized effect request, intent identity and RunMode transport | submit/query/cancel through configured transport; normalize response observation | ACK/status/fill/error observation; connection state only | performs external effect only in permitted mode; returns event | request/intent/mode/external identity | timeout may be UNKNOWN; ACK not fill; Shadow/Replay no production effect | C2–C5 effect boundary per existing class; M0 | `FUNC-014..016/026` |
| `FOP-F05` | Recovery — reduce current exposure through fresh Risk-controlled plan | Execution; `10`, exec-09; ARCH-005/006/010 | actual exposure, current Graph/Book/Inventory/Risk and attempts | recompute safest supported reduction; never preserve route loyalty over safety | recovery state/plan proposal; sole Recovery writer | emits recovery proposal/command; transport still gated | exposure/plan/limits/dependencies | no safe plan/exhaustion → fail/escalate, no bypass | C0 planning + gated effects; all applicable modes; M0 | `FUNC-017/018` |
| `FOP-F06` | Reconciliation — prove orders→fills→balances before readiness | Execution; `10`, exec-10; ARCH-005/010/019 | exchange/account observations, FillLedger, journal and claims | resolve in truth order; detect mismatch; retain locks until proven | reconciliation state/report; sole writer | query commands/observations; no direct trade permission | reconciliation/account/fill cursors | unresolved mismatch blocks scope/new risk | startup/restart/periodic; all; M0 | `FUNC-015/019/032` |
| `FOP-G01` | Accounting — attribute actual, expected and non-trade records disjointly | Inventory/Accounting; `04`, `08`, inv-10; ARCH-008/025 | unique fills, explicit fees, valuations and classified capital flows | record provenance/class without mutating Inventory or treating forecast as actual | accounting records; sole Accounting writer | consumes facts; emits ledger/evidence; no effect | entry/action/ledger/valuation | duplicate/conflict reconciles; serialized field schema open | off-C0/read model; all; M0 | `FUNC-020/027` |
| `FOP-G02` | Capability Manager — intersect evidence with exact approved scope | Validation; `16`; ARCH-022/023/024 | EvidenceIds, technical results, human decision, release/license/config scope | verify exact scope/currentness and publish signed manifest | `CapabilityManifest`; sole capability writer | accepts approval/disposition; emits capability state; never order effect | evidence/market/mode/q/model/infra/release | missing/stale/out-of-scope fails closed | governance path; all; M0 | `FUNC-023/024/030` |
| `FOP-G03` | Operations/Health — observe, alert and coordinate runbook actions | Operations; `18`; ARCH-018/023 | metrics/events/canonical states/incidents | evaluate health policy and create alert/incident/runbook command | health/alert/incident evidence; operations state only | may request safe stop; cannot trade or promote maturity | metric/policy/incident | missing signal is observable degradation, not success | off-C0 ops; all; M0 | `FUNC-021/023/032` |
| `FOP-G04` | Infrastructure Monitor — classify resource and clock safety | Infrastructure; `13`; ARCH-018/019 | clock/feed/CPU/network/disk/Recorder observations | aggregate current instance health under policy | `InfraHealthState`; sole writer | emits degraded/unsafe event; no economic state mutation | instance/observation/policy | `DEGRADED` narrows; `UNSAFE` blocks new risk | monitoring with C0-consumed snapshot; all; M0 | `FUNC-013/021/032` |
| `FOP-G05` | Deployment/`botctl` — manage one ready runtime owner safely | Deployment; `14`, deploy-06/08/10/11; ARCH-017/023 | operator action, config/artifact/evidence and installation state | validate lifecycle/readiness, start/stop/reconcile without dual owner | deployment state/audit; deployment sole writer | lifecycle command; no direct order authorization | build digest/config/installation/owner | non-ready or ambiguous ownership prevents start; restart reconciles | client runtime ops; M0 | `FUNC-023/026/032` |
| `FOP-G06` | Licensing — constrain Live eligibility while preserving safety paths | Deployment; `14`; ARCH-017/024 | cached signed entitlement and trustworthy time | verify signature/scope/time and intersect with capability/readiness | license state/event; sole license writer | emits eligibility change; no trade command | entitlement/install/time policy | loss blocks new risk; cancellation/recovery/reconciliation remain | Live eligibility boundary; M0/policy open | `FUNC-023/026/032` |
| `FOP-G07` | Evidence closure — bind RunManifest, DecisionTrace and validation/incident facts | Data + Validation + Ops; `12`, `16`, `18`; ARCH-020/022/023 | exact run inputs, ordered decisions, results and provenance | close immutable manifest/trace/evidence; preserve negative results | evidence artifacts; respective canonical owners only | consumes evidence/events; no external economic effect | run/build/config/model/formula/schema/seed/cursors | incomplete closure cannot support reproducibility/promotion | off-C0 closure; all; M0 | `FUNC-022/023/025/031` |

Dependencies in this table are producer/consumer dependencies, not new module dependencies. In
particular, forecast and simulation rows remain optional outside an exact capability that names
them; sizing remains a proposal; Risk remains the only permission owner; Reservation precedes a
new order effect; and Execution remains the only owner of exchange effects.

## 6. Confirmed functional contradictions

The audit found one active semantic contradiction and two material presentation gaps that were
fully resolvable from existing authorities. The remaining findings are deliberately not promoted
to “contradictions” where their owner has not closed the field-level contract.

| Finding | Classification | Evidence / source | Disposition | Status |
|---|---|---|---|---|
| `FGAP-001` — Graph master §17 showed Participants/Simulator as an unconditional chain and one undifferentiated Risk stage before Sizing | `FUNCTIONAL_CONTRADICTION_CONFIRMED` | `03` §17 versus `00`, `08`, `09`, `10`, Participants/Simulator support contracts and Prompt-1 canonical order | show required features, capability-declared optional forecasts, preliminary Risk, Terminal/Sizing, full Risk, Reservations, immutable plan and pre-send gate | `DOC_CORRECTION_APPLIED` |
| `FGAP-002` — live interface catalog named producer/consumer/version but did not make validity, absence/failure and acceptance anchors inspectable per row | `DOCUMENTARY_GAP`; rows also exposed missing failure detail in the secondary catalog | Data/domain owners plus PASS 13 dependency and invariant catalogs | extend the existing catalog, without creating a parallel authority or fields | `TRACEABILITY_CORRECTION_APPLIED` |
| `FGAP-003` — maintained atlas stopped at domain/state boundaries and did not expose L3/L4 functional validation/decision/failure paths for the ten required flows | `DOCUMENTARY_GAP` | all domain owners and Prompt-2 navigation requirement | add `ARCH-MAP-015..024` and per-map contract tables | `DIAGRAM_CORRECTION_APPLIED` |
| `FGAP-004` — exact `RiskDecision.allowed`/`action` compatibility mapping absent | `OPEN_HUMAN_DECISION` | ARCH-026; Risk/Data owner boundary | preserve fail-closed Submit invariant; do not invent truth table | `HUMAN_DECISION_REQUIRED` |
| `FGAP-005` — exact `RiskReservation`/reservation serialized fields absent | `OPEN_HUMAN_DECISION` | ARCH-027; Execution/Data/Inventory owner boundary | preserve owner/lifecycle/atomicity; do not invent fields or second state | `HUMAN_DECISION_REQUIRED` |
| `FGAP-006` — Recorder P0 physical durability/crash-gap proof not established | `TEST_NOT_IMPLEMENTED` | ARCH-019; `12`, recorder-01/03/05 | preserve bounded handoff versus persistence/durability distinction and stop-new-risk rule | `TEST_REQUIRED` |
| `FGAP-007` — canonical ingress arbitration/source-priority policy not selected | `OPEN_HUMAN_DECISION` | ARCH-016; Data owner | keep one ordered coordinator and source-tagged evidence; defer precise arbitration | `HUMAN_DECISION_REQUIRED` |
| `FGAP-008` — Accounting record semantics exist but exact serialized field schema is not frozen | `MISSING_INTERFACE` | `04`, `08`, inv-10 and Data authority | document semantic interface only; field schema remains Data-owned | `HUMAN_DECISION_REQUIRED` |
| `FGAP-009` — no production Rust/function mapping or runtime behavior was verified | `IMPLEMENTATION_NOT_VERIFIED` | repository audited scope and M0 status | keep every FOP documentary; require Prompt-3/implementation mapping later | `TEST_REQUIRED` |
| `FGAP-010` — queue sizes, search grids, thresholds, fan-out, retry and timeout constants require evidence | `CALIBRATION_REQUIRED` | domain masters, calibration register and Validation authority | no new numeric constants frozen | `BENCHMARK_REQUIRED` |
| `FGAP-011` — mutable Hyperliquid API/fee/precision/transport behavior requires current primary-source confirmation before implementation | `EXTERNAL_REVALIDATION` | External Revalidation Register and domain owners | preserve documented boundary; no web claim promoted here | `EXTERNAL_VERIFICATION_REQUIRED` |
| `FGAP-012` — F4, complex allocator/Bridge activation, maker modes, optional nodes and distributed research remain outside initial scope | `FUTURE_DEFERRED` | `00`, `06`–`08`, `16`, roadmaps | keep disabled unless separately evidenced and approved | `FUTURE_DEFERRED` |
| `FGAP-013` — the 46 FOP contracts had no explicit per-operation decision on whether their parent map was sufficient | `DOCUMENTARY_GAP` | §5 inventory, `ARCH-MAP-015..024` and each selected owner contract | assess 46/46; add children only for 13 branch/state/version/effect-heavy operations; retain parent+table for 33 | `DIAGRAM_CORRECTION_APPLIED` |

No owner ambiguity, second state writer, forecast-to-actual mutation, Risk bypass or sixth
Execution state machine was confirmed after the source-authority comparison. That is an M0
document review result, not implementation proof.

## 7. Corrections applied

| Path | Before | After | Reason | Source | Related finding | Validation |
|---|---|---|---|---|---|---|
| `docs_v2/03_MARKET_GRAPH_AND_ROUTES.md` §17 | linear representation made Participants and Simulator appear universal and placed a single Risk step before Sizing | required features; optional capability-declared forecasts; preliminary Risk; Terminal/Sizing; full Risk; Reservations; immutable plan/pre-send | align a secondary Graph representation without changing any owner semantics | `00`, `08`, `09`, `10`; Participants/Simulator support contracts | `FGAP-001` | semantic diff and dependency searches; see §12 |
| `docs_v2/_analysis/pass13_master_architecture/DOMAIN_INTERFACE_CATALOG.md` | 31 rows had producer/consumer/version but no explicit per-interface validity/failure/test columns | same 31 interfaces with validity/failure handling and existing/`FUNC-*` anchors | make producer→consumer absence and negative behavior inspectable without inventing schemas | Data/domain owners; PASS13 dependency/invariant catalogs | `FGAP-002` | `31/31`, links and table structure checked; see §12 |
| `docs_v2/deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md` | stable maps ended at `ARCH-MAP-014`; function/decision/failure navigation was distributed across domain prose | `ARCH-MAP-015..024`, ten focused maps plus contract tables | add L3/L4 navigation while keeping domain owners authoritative | masters/deep contracts cited beside each map | `FGAP-003` | initial maps retained inside the current `37/37` Mermaid render and contiguous-ID check; see §12 |
| `docs_v2/_analysis/f2_final_integration/PROMPT2_FUNCTIONAL_ARCHITECTURE_CORRECTION_REPORT.md` | no Prompt-2 disposition artifact | 42-component, 31-interface and 46-operation traceability; findings, examples, scenarios, backlog and handoff | record the audit delta without becoming semantic authority | all sources listed in §2 | `FGAP-001..012` | counts, links, tables, whitespace and structure checked; see §12 |
| `docs_v2/README.md` | navigation stopped at Prompt 1 | Prompt-2 report linked with an explicit no-proof/no-authorization warning | keep the growing correction series discoverable | focused report and maintained atlas | `FGAP-002/003` navigation | link resolved; diff inspected; see §12 |
| `docs_v2/deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md` operation deepening | 46 FOP rows existed, but only the ten module parents exposed Mermaid navigation | 13 complexity-selected operation maps `ARCH-MAP-025..037`, each linked to its parent and L4 test | deepen only operations with material branching/state/version/effect/failure complexity | selected owner contracts listed in §8 | `FGAP-013` | all 37 Mermaid blocks, anchors and IDs checked; see §12 |
| `docs_v2/_analysis/f2_final_integration/PROMPT2_FUNCTIONAL_ARCHITECTURE_CORRECTION_REPORT.md` operation deepening | no explicit diagram disposition for each FOP | 46/46 selection matrix, 13 selected maps and 33 parent/table-sufficient dispositions | prove diagrams were selected rather than generated mechanically | FOP inventory plus parent/owner contracts | `FGAP-013` | counts, links and tables checked; see §12 |

The changes are review deltas. They do not rewrite historical PASS reports, inherit prior human
approval, or authorize implementation, deployment, trading or capital.

## 8. Deep Mermaid maps

The maintained atlas keeps `ARCH-MAP-001..014` unchanged in identity. `ARCH-MAP-015..024` are the
module parents; `ARCH-MAP-025..037` are selected detailed-operation children. The atlas is a
consumer of the listed owners, never their replacement.

| Diagram | Location / authority | Components and contract depth | Scenario anchors | Validation status |
|---|---|---|---|---|
| `ARCH-MAP-015` | atlas §18; `11`, data-02/09, `03` | adapter → capture → normalize/reject → ordered commit → Book readiness, including reconnect/gap | `FUNC-001/004/028/031` | source reviewed; Mermaid check reported in §12 |
| `ARCH-MAP-016` | atlas §19; `03`, graph-01/04/11 | Metadata → structural decision → Graph/Route/index generation → atomic publication; fee-only branch | `FUNC-005/029/031` | source reviewed; Mermaid check reported in §12 |
| `ARCH-MAP-017` | atlas §20; `04`, `03`, `05` | coherent q inputs → NetConvert/formulas → comparator → Opportunity or typed reject | `FUNC-006..009/030` | source reviewed; Mermaid check reported in §12 |
| `ARCH-MAP-018` | atlas §21; `05`, `06`, `07`, `16` | Feature support → capability dependency decision → forecast/simulator or conservative bypass → OOD/reject | `FUNC-010/024/030/031` | source reviewed; Mermaid check reported in §12 |
| `ARCH-MAP-019` | atlas §22; `08`, inv-02/06/08 | actual Inventory/claims → Reachability/Terminal → q search/shared allocation → proposal only | `FUNC-011/012/030` | source reviewed; Mermaid check reported in §12 |
| `ARCH-MAP-020` | atlas §23; `09`, `10`, risk-02/05/06, exec-01/04/11 | preliminary/full Risk → atomic Reservation → immutable plan → pre-send → mode transport | `FUNC-003/012..015/026/030` | source reviewed; Mermaid check reported in §12 |
| `ARCH-MAP-021` | atlas §24; `10`, exec-04/09/10 | actual partial fill → Inventory/claims → continuation replan or Recovery → Reconciliation | `FUNC-015..019` | source reviewed; Mermaid check reported in §12 |
| `ARCH-MAP-022` | atlas §25; `04`, `08`, inv-10 | unique fills/fees/valuations/capital flows → classification → disjoint records; no Inventory ownership | `FUNC-020/027` | source reviewed; Mermaid check reported in §12 |
| `ARCH-MAP-023` | atlas §26; `11`, `12`, recorder-01/03/05/06/07 | prioritized handoff → persistence/quality → manifest → isolated Replay → DecisionTrace/divergence | `FUNC-021/022/025/028` | source reviewed; Mermaid check reported in §12 |
| `ARCH-MAP-024` | atlas §27; `16`, `14`, `18` | scientific evidence → validation → human exact-scope decision → manifest/readiness/license intersection | `FUNC-023/024/026/032` | source reviewed; Mermaid check reported in §12 |

Each map has an adjacent L4 contract table covering input validation, ordered processing/decision,
output/state effect, failure, versions/consumers and acceptance anchors. Diagram completion does
not close ARCH-016, ARCH-019, ARCH-026 or ARCH-027 and does not prove runtime correctness.

### 8.1 Diagram-selection assessment for all 46 FOP operations

Selection rule: add a child diagram only when the parent plus the complete §5 contract row cannot
show the important internal branching/state/version/effect/failure path without ambiguity.
`PARENT + TABLE` is therefore a positive coverage disposition, not an omitted operation.

| FOP | Existing parent | Disposition | Complexity assessment | Maintained coverage |
|---|---|---|---|---|
| `FOP-A01` | [`ARCH-MAP-015`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-015) | `PARENT + TABLE` | capture/reconnect failure is already explicit; it owns connection state only | parent map + §5 row + `FUNC-001/004/028` |
| `FOP-A02` | [`ARCH-MAP-020`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-020) / [`021`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-021) | `PARENT + TABLE` | account observation boundary is covered by Transport/UNKNOWN/Reconciliation children | parents + §5 row + `FUNC-014..020/027` |
| `FOP-A03` | [`ARCH-MAP-016`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-016) | `PARENT + TABLE` | one validated metadata-event output; no canonical Graph mutation | parent + §5 row + `FUNC-001/005/029` |
| `FOP-A04` | [`ARCH-MAP-015`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-015) | `PARENT + TABLE` | validate-or-reject branch and no-mutation result already occupy the parent | parent + §5 row + `FUNC-001/025` |
| `FOP-A05` | [`ARCH-MAP-023`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-023) | `PARENT + TABLE` | Clock emits explicit mode timers; hidden scheduler risk is covered by Replay child | parent + §5 row + `FUNC-025/026` |
| `FOP-A06` | [`ARCH-MAP-015`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-015) | `DETAIL MAP 025` | canonical commit, multiple input classes, stale worker rejection and asynchronous effects | child map + §5 row + `FUNC-002/025/031` |
| `FOP-A07` | [`ARCH-MAP-023`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-023) | `DETAIL MAP 026` | P0–P3 pressure, persistence/durability distinction, crash gap and Risk response | child map + §5 row + `FUNC-021/028` |
| `FOP-A08` | [`ARCH-MAP-023`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-023) | `DETAIL MAP 027` | isolated mutable state, ordered time/RNG, hash divergence and no-Live-effect boundary | child map + §5 row + `FUNC-022/025` |
| `FOP-B01` | [`ARCH-MAP-015`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-015) | `DETAIL MAP 028` | single-writer mutation, snapshot/delta/gap/reconnect branches and readiness restoration | child map + §5 row + `FUNC-001/004/008` |
| `FOP-B02` | [`ARCH-MAP-016`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-016) | `PARENT + TABLE` | material-change classification and Metadata writer are already explicit in parent | parent + §5 row + `FUNC-003/005/029` |
| `FOP-B03` | [`ARCH-MAP-017`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-017) | `PARENT + TABLE` | point-in-time fee resolution has one fail-closed result; NetConvert child consumes it | parent + §5 row + `FUNC-006/009/020` |
| `FOP-B04` | [`ARCH-MAP-017`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-017) | `PARENT + TABLE` | precision validation/quantization is source-owned and fully traced into NetConvert | parent + §5 row + `FUNC-003/006/029` |
| `FOP-B05` | [`ARCH-MAP-016`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-016) | `DETAIL MAP 029` | off-side build, forward/reverse consistency, stale completion and atomic generation switch | child map + §5 row + `FUNC-005/029/031` |
| `FOP-B06` | [`ARCH-MAP-016`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-016) / [`017`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-017) | `PARENT + TABLE` | structural enumeration is detailed by Map 029 and economic evaluation by Map 030 | parents + §5 row + `FUNC-005..009/031` |
| `FOP-B07` | [`ARCH-MAP-016`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-016) | `PARENT + TABLE` | bounded deterministic lookup/index publication is covered by Graph child | parent + §5 row + `FUNC-005/031` |
| `FOP-B08` | [`ARCH-MAP-016`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-016) / [`024`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-024) | `PARENT + TABLE` | evidence proposal only; no permission/state-owner ambiguity | parents + §5 row + `FUNC-004/023/024` |
| `FOP-B09` | [`ARCH-MAP-024`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-024) | `PARENT + TABLE` | compute-priority classification is not authorization; calibrated policy stays open | parent + §5 row + `FUNC-010/023/024` |
| `FOP-B10` | [`ARCH-MAP-019`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-019) / [`024`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-024) | `PARENT + TABLE` | evidence aggregation cannot replace current truth; no effect path | parents + §5 row + `FUNC-003/010/024` |
| `FOP-C01` | [`ARCH-MAP-017`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-017) | `PARENT + TABLE` | QF-001..110 already have canonical formula/golden contracts; a generic duplicate would obscure ownership | parent + §5 row + `FUNC-006/008/009` |
| `FOP-C02` | [`ARCH-MAP-017`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-017) | `DETAIL MAP 030` | bid/ask walk, depth residual, fee asset, quantization and numerical rejection branches | child map + §5 row + `FUNC-006/008/009` |
| `FOP-C03` | [`ARCH-MAP-017`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-017) | `PARENT + TABLE` | comparator/classification decisions already dominate the focused parent map | parent + §5 row + `FUNC-005..009/013` |
| `FOP-C04` | [`ARCH-MAP-018`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-018) | `PARENT + TABLE` | incremental feature validity/support and consumers are complete in parent/table | parent + §5 row + `FUNC-003/010/031` |
| `FOP-C05` | [`ARCH-MAP-017`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-017) | `PARENT + TABLE` | C1/C2/C3/fallback parity branch is already explicit beside full-L2 NetConvert | parent + §5 row + `FUNC-006/007/008` |
| `FOP-D01` | [`ARCH-MAP-018`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-018) | `PARENT + TABLE` | support/OOD/fallback and no-authority path are already the parent decision spine | parent + §5 row + `FUNC-010/030/031` |
| `FOP-D02` | [`ARCH-MAP-018`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-018) | `PARENT + TABLE` | same scoped forecast contract; Future/maker dependency remains optional | parent + §5 row + `FUNC-010/024/030` |
| `FOP-D03` | [`ARCH-MAP-018`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-018) | `PARENT + TABLE` | fidelity/support/reproducibility and synthetic-not-actual semantics are already explicit | parent + §5 row + `FUNC-006/010/013/030` |
| `FOP-D04` | [`ARCH-MAP-024`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-024) | `PARENT + TABLE` | integrity/support/approval intersection is covered by capability parent | parent + §5 row + `FUNC-010/023/030` |
| `FOP-E01` | [`ARCH-MAP-019`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-019) / [`021`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-021) / [`022`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-022) | `PARENT + TABLE` | actual-fill, non-trade and accounting boundaries are split across three focused parents without ambiguity | parents + §5 row + `FUNC-002/017/019/020/027` |
| `FOP-E02` | [`ARCH-MAP-019`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-019) | `PARENT + TABLE` | pure reachability proposal and absent-path rejection are complete in parent/table | parent + §5 row + `FUNC-003/011/030` |
| `FOP-E03` | [`ARCH-MAP-019`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-019) | `PARENT + TABLE` | pure terminal bands/exit/OOD decision is explicit before Sizing | parent + §5 row + `FUNC-011/013/030` |
| `FOP-E04` | [`ARCH-MAP-019`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-019) | `DETAIL MAP 031` | non-monotonic validated set, exact-q search, stale result and proposal-only boundary | child map + §5 row + `FUNC-011/012/030/031` |
| `FOP-E05` | [`ARCH-MAP-019`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-019) / [`020`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-020) | `PARENT + TABLE` | shared-resource proposal is covered before atomic Reservation; Later-V1 remains gated | parents + §5 row + `FUNC-012/024` |
| `FOP-E06` | [`ARCH-MAP-019`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-019) / [`022`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-022) / [`024`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-024) | `PARENT + TABLE` | Future MOVE/STAY proposal has no initial effect/permission path | parents + §5 row + `FUNC-020/024/030` |
| `FOP-F01` | [`ARCH-MAP-020`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-020) | `DETAIL MAP 032` | immutable snapshot, preliminary/full gates, action/TTL and unresolved compatibility mapping | child map + §5 row + `FUNC-003/013/030` |
| `FOP-F02` | [`ARCH-MAP-020`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-020) | `DETAIL MAP 033` | atomic shared claims, field-level open schema, UNKNOWN retention and proof-based release | child map + §5 row + `FUNC-012/015/017` |
| `FOP-F03` | [`ARCH-MAP-020`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-020) | `DETAIL MAP 034` | five machines, event distinctions, actual-fill continuation, UNKNOWN and Recovery signal | child map + §5 row + `FUNC-003/014..018/026` |
| `FOP-F04` | [`ARCH-MAP-020`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-020) | `DETAIL MAP 035` | mode-correct external effect, possible transmission, asynchronous response and no blind retry | child map + §5 row + `FUNC-014..016/026` |
| `FOP-F05` | [`ARCH-MAP-021`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-021) | `DETAIL MAP 036` | current-exposure planning, Risk/Reservation, bounded retries, partial/UNKNOWN and failed Recovery | child map + §5 row + `FUNC-017/018` |
| `FOP-F06` | [`ARCH-MAP-021`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-021) | `DETAIL MAP 037` | orders→fills→balances proof, crash points, claim retention and READY gate | child map + §5 row + `FUNC-015/019/032` |
| `FOP-G01` | [`ARCH-MAP-022`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-022) | `PARENT + TABLE` | parent is already an operation-level exact-once/classification diagram | parent + §5 row + `FUNC-020/027` |
| `FOP-G02` | [`ARCH-MAP-024`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-024) | `PARENT + TABLE` | exact-scope evidence/approval intersection already forms parent decision spine | parent + §5 row + `FUNC-023/024/030` |
| `FOP-G03` | [`ARCH-MAP-024`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-024) | `PARENT + TABLE` | observe/alert/runbook without economic ownership; no additional complex branch | parent + §5 row + `FUNC-021/023/032` |
| `FOP-G04` | [`ARCH-MAP-020`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-020) / [`023`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-023) / [`024`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-024) | `PARENT + TABLE` | health classification effects are already visible at Risk/Recorder/readiness consumers | parents + §5 row + `FUNC-013/021/032` |
| `FOP-G05` | [`ARCH-MAP-024`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-024) | `PARENT + TABLE` | startup/readiness/one-owner path is complete; detailed concurrency belongs to later authorized mission | parent + §5 row + `FUNC-023/026/032` |
| `FOP-G06` | [`ARCH-MAP-024`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-024) | `PARENT + TABLE` | license is one operand of authority intersection and preserves safety paths | parent + §5 row + `FUNC-023/026/032` |
| `FOP-G07` | [`ARCH-MAP-023`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-023) / [`024`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-024) | `PARENT + TABLE` | manifest/trace closure and promotion boundary are already explicit across both parents | parents + §5 row + `FUNC-022/023/025/031` |

Assessment result: **13 `DETAIL MAP` + 33 `PARENT + TABLE` = 46/46 operations**. No Rust
symbol, serialized field, numeric policy, QF formula, Risk rule or Execution transition was added.

### 8.2 Added detailed-operation maps

| Child map | Selected operation | Parent link | Primary complexity | ARCH / QF / FUNC test anchor | Documentary status |
|---|---|---|---|---|---|
| [`ARCH-MAP-025`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-025) | `FOP-A06` Ordered Event Coordinator | [`ARCH-MAP-015`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-015) | ordered commit, stale results, async effects | ARCH-002/004/016; QF N/A; `FUNC-002/025/031` | specified; runtime test absent |
| [`ARCH-MAP-026`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-026) | `FOP-A07` Recorder | [`ARCH-MAP-023`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-023) | priority/backpressure, persistence, crash/durability | ARCH-001/018/019/021; QF N/A; `FUNC-021/028` | specified; ARCH-019/test open |
| [`ARCH-MAP-027`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-027) | `FOP-A08` Replay | [`ARCH-MAP-023`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-023) | isolation, Clock/RNG/order, hash divergence | ARCH-003/011/020/021; shared QF; `FUNC-022/025` | specified; determinism test absent |
| [`ARCH-MAP-028`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-028) | `FOP-B01` Book reducer | [`ARCH-MAP-015`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-015) | canonical mutation, gap/resync/readiness | ARCH-002/014/017; QF-001–013 downstream; `FUNC-001/004/008` | specified; reducer test absent |
| [`ARCH-MAP-029`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-029) | `FOP-B05` Graph generation | [`ARCH-MAP-016`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-016) | off-side build, atomic publication, stale completion | ARCH-003/009/015/022; QF N/A; `FUNC-005/029/031` | specified; atomicity test absent |
| [`ARCH-MAP-030`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-030) | `FOP-C02` NetConvert | [`ARCH-MAP-017`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-017) | exact units/depth/fees/precision/numerical failure | ARCH-007/014; QF-007–010/014–016; `FUNC-006/008/009` | formula unchanged; parity test absent |
| [`ARCH-MAP-031`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-031) | `FOP-E04` Position Sizer | [`ARCH-MAP-019`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-019) | non-monotonic set/search, shared limits, stale proposal | ARCH-008/009/024; QF-027/073–077; `FUNC-011/012/030/031` | specified; calibration/test absent |
| [`ARCH-MAP-032`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-032) | `FOP-F01` Risk | [`ARCH-MAP-020`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-020) | snapshot/actions/TTL/revalidation and open compatibility | ARCH-006/009/026; QF-056–078 applicable; `FUNC-003/013/030` | specified; ARCH-026 open |
| [`ARCH-MAP-033`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-033) | `FOP-F02` Reservation | [`ARCH-MAP-020`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-020) | atomic claims, UNKNOWN retention, proven release | ARCH-006/009/027; QF-073/074; `FUNC-012/015/017` | specified; ARCH-027 open |
| [`ARCH-MAP-034`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-034) | `FOP-F03` Execution Coordinator | [`ARCH-MAP-020`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-020) | five machines, actual-fill continuation, UNKNOWN/Recovery | ARCH-004/005/006/010; owner QFs; `FUNC-003/014..018/026` | specified; state-machine tests absent |
| [`ARCH-MAP-035`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-035) | `FOP-F04` Execution Transport | [`ARCH-MAP-020`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-020) | external effect, mode isolation, possible-send ambiguity | ARCH-005/006/010; QF N/A; `FUNC-014..016/026` | specified; API/runtime proof absent |
| [`ARCH-MAP-036`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-036) | `FOP-F05` Recovery | [`ARCH-MAP-021`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-021) | current exposure, bounded replan, partial/UNKNOWN/failure | ARCH-005/006/010; QF-079/080; `FUNC-017/018` | specified; calibration/test absent |
| [`ARCH-MAP-037`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-037) | `FOP-F06` Reconciliation | [`ARCH-MAP-021`](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md#arch-map-021) | proof order, crash consistency, claims/readiness | ARCH-005/010/019; QF-073/074; `FUNC-015/019/032` | specified; external/runtime proof absent |

Remaining gap: all 13 children are documentary specifications. The 33 operations without a child
remain completely traceable through parent+table, but must be reconsidered if implementation adds
new internal branches, mutable state, concurrency, effects or failure semantics.

## 9. Eight explanatory walkthroughs

All values and names below are illustrative documentary fixtures. They are not market facts,
calibrated thresholds, executable recommendations or evidence of profitability.

### 9.1 Example 1 — Book update

| Required element | Walkthrough |
|---|---|
| Initial state | Market `M` has ready `BookVersion=b17`; routes `r2/r9` are listed in the current `pair_to_routes` generation. |
| Input | A new Hyperliquid L2 payload arrives with source connection, exchange/capture time and sequence provenance. |
| Operations | `FOP-A01` captures RAW evidence; `FOP-A04` validates and normalizes; `FOP-A06` orders the event; `FOP-B01` applies it; `FOP-B07` locates `r2/r9`; economics are recomputed through `FOP-B06/C02/C03`. |
| Intermediate result | A valid update produces `BookVersion=b18` and an affected-route set. A missing sequence, invalid price/size or crossed/stale result instead marks only the affected market non-ready and emits rejection/gap evidence. |
| Versions | RAW/schema/source cursor, `MetadataVersion`, `BookVersion`, Graph/Route/index generation and Formula/Fee/Precision versions remain linked. |
| Decision/output | Valid coherent snapshot: publish `BookSnapshot b18` and schedule `r2/r9`. Invalid/stale snapshot: no canonical valid Book publication and no route authorization. Reconnect alone does not restore tradability; required snapshot/readiness conditions do. |
| State owner | Book Engine alone writes Book state; adapter/normalizer/worker do not. |
| Failure/test | Unknown event becomes typed rejection; stale worker completion cannot commit. `FUNC-001`, `FUNC-004`, `FUNC-031`. |

### 9.2 Example 2 — OWA economics

| Required element | Walkthrough |
|---|---|
| Initial state | One structural candidate `A→X→B` and an executable direct comparator `A→B` exist in one coherent route generation. No profitable outcome is presumed. |
| Input | Illustrative size `q`, side-correct full L2 snapshots, point-in-time fee/precision rules and FormulaVersion. |
| Operations | `FOP-B06` confirms structural OWA classification; `FOP-C02` walks bids for base→quote and asks for quote→base, consuming depth; each leg carries gross output, fee asset/units, net output and quantization into the next leg; the same exact semantics evaluate the direct comparator. `FOP-C03` compares size-specific executable results. |
| Intermediate result | Route and comparator results are bound to the same compatible economic snapshot. Shared units are never collapsed, and FastL1/BBO-C2 may only return a parity-safe result, prove rejection, or fall back to full L2. |
| Versions | Graph/Route/index generation, each BookVersion, Metadata/Fee/Precision and FormulaVersion, plus q. |
| Decision/output | Emit Opportunity only if source-owned OWA and economic criteria pass; otherwise emit a typed RejectEpisode such as invalid comparator, insufficient depth, unknown fee/precision or incompatible generation. Neither output grants permission. |
| State owner | Formula is pure; Opportunity owns only opportunity evidence. Risk/Execution state is untouched. |
| Failure/test | Missing executable direct comparator rejects OWA classification; depth exhaustion cannot invent liquidity. `FUNC-006..009`. |

### 9.3 Example 3 — shared L2 depth

| Required element | Walkthrough |
|---|---|
| Initial state | Candidates `c1` and `c2` are each profitable-looking in isolation but both consume the same price levels on market `M`. |
| Input | Exact per-level consumption from both q-specific `RouteEconomics` plus current balance, book and Risk capacities. |
| Operations | `FOP-C02` records standalone depth use; `FOP-E05` or baseline shared-resource arbitration exposes overlap; `FOP-F01` checks aggregate constraints; `FOP-F02` atomically claims capacity for the winning compatible proposal. |
| Intermediate result | The first committed Reservation reduces available shared capacity. The second candidate must be recomputed/down-sized or rejected against the post-claim state. |
| Versions | BookVersion, candidate/q versions, dependency map, RiskDecision TTL/version and Reservation lifecycle. |
| Decision/output | At most the capacity actually available may be reserved. Two standalone calculations never imply two simultaneous claims. |
| State owner | Reservation Engine alone writes claims; Sizer/Allocator only propose. |
| Failure/test | Atomic conflict returns rejection/no order effect; no double reservation. `FUNC-012`. |

### 9.4 Example 4 — Risk refuses positive expected economics

| Required element | Walkthrough |
|---|---|
| Initial state | Candidate economics are positive under the illustrative comparator, but a current constitutional exposure/health/capability limit is violated. |
| Input | Compatible q proposal, current Inventory/claims/health/capability, immutable economic/model snapshots. |
| Operations | `FOP-F01` applies the source-owned hard rule after preliminary/full ordering; positive expected economics cannot override it. |
| Intermediate result | Typed `RiskDecision` rejection records the rule/provenance at the semantic level; the unresolved ARCH-026 field mapping is not invented. |
| Versions | all economic and account snapshots, Risk config/action/capability and TTL. |
| Decision/output | Reject/HALT/recovery-only as defined by the Risk owner; no Reservation, ExecutionPlan, OrderIntent or production transport effect is created. |
| State owner | Risk alone owns the decision; Opportunity, Simulator and Sizer remain proposal/evidence producers. |
| Failure/test | Any path producing a new order effect after the hard reject fails. `FUNC-013`. |

### 9.5 Example 5 — partial TT

| Required element | Walkthrough |
|---|---|
| Initial state | A TT plan expected an intermediate net output of `20` units; reservations and plan versions reflect that expectation. |
| Input | Unique proven FillLedger evidence shows actual net fill `13.7` units after applicable actual fee treatment. |
| Operations | `FOP-F03` records the partial-fill transition; `FOP-E01` applies only `13.7` actual units; `FOP-F02` updates/retains claims per lifecycle; `FOP-E02/E03/E04` recompute feasible continuation from current state; `FOP-F01` reauthorizes; `FOP-F03` creates a new versioned continuation plan or `FOP-F05` enters Recovery. |
| Intermediate result | The earlier `20` is preserved as expected/planned evidence, never used as actual Inventory or forced later-leg quantity. |
| Versions | Fill ID/cursor, Inventory/Reservation, current Book/Graph/rules, new q, RiskDecision and continuation plan. |
| Decision/output | Continue only with an authorized feasible quantity derived from `13.7` and current conditions; otherwise Recovery/stop. |
| State owner | FillLedger is actual evidence; Inventory owns exposure; Reservation owns claims; Execution owns lifecycle. |
| Failure/test | Duplicate fill is idempotent; stale continuation plan cannot send. `FUNC-017/018`. |

### 9.6 Example 6 — UNKNOWN order

| Required element | Walkthrough |
|---|---|
| Initial state | An authorized Submit effect may have reached the exchange; no definitive response has arrived before timeout. |
| Input | Intent/request identity, transport timeout observation, retained balance/book/Risk claims and journal evidence. |
| Operations | `FOP-F04` emits ambiguity rather than a fabricated reject; `FOP-F03` enters UNKNOWN; `FOP-F02` retains relevant claims; `FOP-F06` queries and reconciles orders→fills→balances; `FOP-F05` proposes safe current-exposure recovery where required. |
| Intermediate result | New overlapping risk remains blocked while order existence/fills are unresolved. No blind resend uses the same economic assumption. |
| Versions | intent/request/external identity, Reservation lifecycle, account/fill/reconciliation cursors and recovery dependencies. |
| Decision/output | Proven no-order, live-order, fill or mismatch evidence determines the next state/action; unresolved ambiguity remains locked/escalated. |
| State owner | Execution owns UNKNOWN; Reservation owns claims; Reconciliation owns consistency proof. |
| Failure/test | A retry before proof or early release of claims fails. `FUNC-015/019`. |

### 9.7 Example 7 — non-trade balance change

| Required element | Walkthrough |
|---|---|
| Initial state | Account balance is reconciled at a known cursor with no associated strategy fill. |
| Input | Proven deposit observation with account provenance and classification evidence. |
| Operations | `FOP-A02` captures the observation; `FOP-F06` reconciles it; `FOP-E01` updates actual available Inventory under the non-trade class; `FOP-G01` creates a capital-flow accounting record separate from StrategyPnL. |
| Intermediate result | Actual units/availability may change, but no trade fill, execution success or expected-economic result is fabricated. |
| Versions | account/reconciliation cursor, InventoryVersion, accounting entry/valuation/classification. |
| Decision/output | Deposit/capital-flow record and reconciled Inventory update; StrategyPnL unchanged. |
| State owner | Inventory owns exposure; Accounting owns classification/record; neither duplicates the other. |
| Failure/test | Ambiguous/unclassified balance delta locks affected scope until reconciled. `FUNC-020/027`. |

### 9.8 Example 8 — optional model unavailable

| Required element | Walkthrough |
|---|---|
| Initial state | The advanced Participant artifact is missing, corrupt, OOD or unsupported for the current q/horizon. |
| Input | FeatureSnapshot, requested capability scope and current CapabilityManifest/artifact registry. |
| Operations | `FOP-D04` rejects unavailable/unsupported artifact use; `FOP-D01` emits no valid forecast. `FOP-G02` checks whether the exact capability declares that forecast required. |
| Intermediate result | Branch A: an advanced capability requiring the model fails closed. Branch B: the conservative baseline whose contract does not require it follows the documented no-model path and remains only functionally eligible. |
| Versions | feature/model/support/q/horizon/capability/build/config. |
| Decision/output | Branch A produces typed unsupported/missing dependency rejection. Branch B may continue to preliminary Risk, exact economics, Terminal/Sizing, full Risk and Reservations; it gains no automatic permission. |
| State owner | Artifact Manager owns artifact state; Capability owns scope; Risk owns permission. |
| Failure/test | Treating the missing forecast as zero, silently substituting an unapproved artifact or making it universal fails. `FUNC-010/024/030`. |

## 10. Functional acceptance scenarios

These stable local scenarios supplement the existing project scenarios; they do not renumber or
replace them. `Expected mutation` names the only permitted state effect. `Expected non-mutation`
is equally normative. No row below is reported as a runtime PASS.

| ID | Preconditions / trigger | Expected events | Expected mutation | Expected non-mutation | Rejection / exception | Source / modules | ARCH / existing scenarios | Suitable test | Current evidence |
|---|---|---|---|---|---|---|---|---|---|
| `FUNC-001` | captured payload is unknown, malformed or has invalid price/size | RAW outcome then typed rejection/gap in canonical order | rejection/readiness evidence only; market scope may become non-ready | no valid event, Book or account/economic mutation | explicit reason/provenance; never guessed data | `11`, data-02/09; Adapter, Normalizer, Book | ARCH-001/002/014/017; A-01; RAW-ORDER-02/03 | schema/property/fault test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-002` | two producers/readers attempt to write one canonical state | ordered command/event reaches named owner | only the sole owner commits one version | second module/callback/worker cannot mutate | reject/report ownership violation | `00`, PASS13 ownership; Core/all state owners | ARCH-012/027–029; A-02 | architecture lint + concurrency test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-003` | proposal combines old Book/Graph/rules/model/account version with newer state | version mismatch/revalidation event | rejection/trace or fresh recomputation only | no Risk authorization, claim or effect from mixed snapshot | typed stale/incompatible result | `00`, `03`, `09`–`11`; Graph/Risk/Execution | ARCH-009/013–018/022/026–029; A-07/A-17 | version-skew/race test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-004` | connection is up after start/reconnect but Book snapshot is missing, gapped or stale | connection event plus readiness transition | connection/market readiness state only | no tradable Book assertion or route authorization | market remains non-ready until restoration contract passes | `03`, `11`; Feed, Book, Route | ARCH-013–017; A-01/A-07 | reconnect/gap state-machine test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-005` | metadata structural change or graph worker completion occurs | generation candidate, compatibility check, atomic publication | Graph/Route/index switch as one coherent generation | readers never observe mixed old/new generation | stale/incomplete generation withheld | `03`, graph-01/04/11; Metadata/Graph/Route | ARCH-003/009/015/022; A-03/A-07/A-16 | generation-race/property test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-006` | identical typed QF inputs run in Replay/Paper/Shadow/Live semantics or optimized/baseline path | Formula call/result evidence | none; pure result only | no mode-specific equation, units or rounding drift | mismatch is nonconformance; reject invalid domain | `04`; Formula/NetConvert/FastL1 | ARCH-007/008/014; A-09/A-20 | golden/property/differential test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-007` | route is proposed as OWA | route/direct comparator evaluations | Opportunity/RejectEpisode evidence only | no OWA classification or permission without executable valid direct comparator | missing/invalid comparator rejects classification | `03`, graph-05; Route/Opportunity | ARCH-003/007/014; A-07/A-20 | worked golden/property test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-008` | q exceeds available side-correct L2 depth on any leg | per-level consumption then depth exhaustion | rejection evidence only | no fabricated fill/output/liquidity/Inventory | insufficient-depth typed reject or bounded q | `03`, `04`; Book/NetConvert/Opportunity | ARCH-007/009/014; A-19/A-20 | depth property/boundary test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-009` | conversion charges fee in a particular asset/unit and applies precision | gross, fee, net and quantization results remain typed | economic result/evidence only | fee units never collapse into output silently; no actual ledger entry | unknown fee/precision rejects economics | `04`, `05`, `11`; Fee/Precision/Formula/Accounting | ARCH-007/014/015/025; A-07/A-20 | unit/golden/rounding test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-010` | optional model is absent, corrupt, OOD or unsupported for q/horizon | artifact/support check and capability-dependency decision | typed rejection for dependent capability or documented baseline path | missing value is not zero; no universal dependency/promotion | only requiring scope fails closed | `06`, `07`, `16`; Models/Participants/Simulator/Capability | ARCH-002/021/022/024/025; A-08/A-14 | capability/support matrix test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-011` | Terminal/Sizer finds one or more feasible q candidates | proposal/trace emitted to Risk | candidate proposal state/evidence only | no permission, Reservation, order or Inventory mutation | no feasible q means no action | `08`, inv-02/06; Terminal/Sizer/Risk | ARCH-008/009/024; A-05/A-18 | search/property/negative test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-012` | candidates overlap balance, L2 or Risk capacity | shared-dependency evaluation and atomic reserve command | one compatible Reservation lifecycle commit | no double claim or send before claim | conflicting/stale second claim rejects/recomputes | `08`, `10`, exec-04; Allocator/Reservation | ARCH-006/012/019/027; A-18/A-19 | atomicity/concurrency/property test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-013` | economics are favorable but hard Risk/health/capability constraint fails | typed Risk rejection/HALT/recovery-only event | Risk state/trace only | no Reservation, new plan, OrderIntent or new production effect | hard decision cannot be overridden downstream | `09`, risk-02/05/06; Risk/all proposal producers | ARCH-006/009/024/026; A-05/A-12 | policy table/integration/negative test | `SPECIFIED — TEST NOT EXECUTED`; ARCH-026 fields open |
| `FUNC-014` | authorized intent is submitted and transport returns ACK before fill | Intent, effect request, ACK, later status/fill as separate ordered observations | Execution lifecycle transitions only at each proven event | ACK cannot mutate Inventory or prove fill | reject/timeout follows own transition; no state collapse | `10`, exec-01/11; Execution/Transport/Inventory | ARCH-004–006/010; A-04/A-05 | state-machine/model test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-015` | Submit may have reached exchange but response is indefinite | timeout→UNKNOWN→query/reconciliation observations | UNKNOWN state and retained relevant Reservations | no blind resend, release or assumed fill/reject | unresolved remains locked/escalated | `10`, exec-04/10/11; Execution/Reservation/Reconciliation | ARCH-005/006/010/019/027; A-05/A-17 | fault-injection/state-machine test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-016` | cancel request races fill/status | cancel intent/request and external fill/cancel confirmation arrive in either order | only ordered proven observations transition execution/fill state | request/ACK alone cannot declare terminal cancellation | reconcile ambiguous/conflicting order | `10`, exec-01/10/11; Execution/Transport/Reconciliation | ARCH-004/005/010/016; A-03/A-17 | permutation/model test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-017` | planned intermediate output differs from unique actual partial fill | fill evidence→FillLedger→Inventory/claim updates→continuation command | actual quantity only updates FillLedger/Inventory/Reservations | planned/forecast quantity never becomes actual exposure | stale/duplicate/incompatible fill rejected or idempotent | `08`, `10`, `11`; FillLedger/Inventory/Execution | ARCH-005/008/009/027–029; A-02/A-11 | partial-fill/idempotency test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-018` | continuation is infeasible or exposure becomes unsafe after partial/failed leg | current-state recompute→Risk→Recovery transition | Recovery state/current-exposure proposal only, then gated effects | no loyalty to original route and no Risk bypass | no safe plan/exhaustion fails/escalates | `09`, `10`, exec-09; Recovery/Risk/Execution | ARCH-005/006/010; A-05/A-17 | fault/scenario/state-machine test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-019` | startup/restart/UNKNOWN has inconsistent external and local evidence | query orders→apply unique fills→compare balances→report | Reconciliation state; actual owners update only proven facts | no readiness/new risk while unresolved; claims retained | mismatch remains explicit and scoped | `10`, exec-10; Reconciliation/Account/Inventory | ARCH-005/010/019; A-15/A-17 | restart/fault/reconciliation test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-020` | unique fill, expected PnL, MTM and/or capital flow is observed | classified accounting inputs with provenance | Accounting records; Inventory only from actual facts | expected/MTM not actual units; deposit not StrategyPnL; Accounting not Inventory writer | duplicate/conflict reconciles; ambiguous class held | `04`, `08`, inv-10; Accounting/Inventory | ARCH-008/025/028/029; A-02/A-11 | ledger invariant/property test | `SPECIFIED — TEST NOT EXECUTED`; serialized schema open |
| `FUNC-021` | Recorder slows, disk fills or P0 handoff/persistence is threatened | health/degradation/gap and stop-new-risk signal | Recorder/Infra/Risk health states and explicit evidence gap | no silent P0 loss or false durability claim; no indefinite Core disk wait | stop new risk; preserve safety/reconcile | `12`, `13`, recorder-01/03/05; Recorder/Infra/Risk | ARCH-001/018–021; A-15/A-24; RAW-ORDER-05/07 | disk-pressure/crash/torn-write test | `SPECIFIED — TEST NOT EXECUTED`; ARCH-019 open proof |
| `FUNC-022` | historical dataset replays while Live exists | isolated Replay ingress/timers/commits/DecisionTrace | Replay-only canonical states and report | no Live C0/state/Transport/balance mutation | missing manifest/divergence invalidates evidence | `12`, recorder-06/07; Replay/Data/Core | ARCH-003/004/011/020/021; A-09; REPLAY-ISO-01..04 | isolation/equivalence/determinism test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-023` | scientific/technical evidence says GO but exact human/capital approval is absent | validation evidence and disposition only | evidence/candidate capability state as authorized by owner | no Live capability, order permission or capital allocation | missing approval/scope fails closed | `16`, roadmaps; Validation/Capability/Deployment/Risk | ARCH-022–024; A-23/A-24 | governance/manifest negative test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-024` | Future/optional module exists or produces output without activated exact capability | support/capability intersection | research/evidence state only or explicitly enabled scoped state | no universal baseline dependency or silent Live activation | disabled/out-of-scope result ignored/rejected | `00`, `06`–`08`, `16`; models/Bridge/Allocator/HWC | ARCH-002/021–025; A-08/A-10/A-14 | feature/capability matrix test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-025` | same ordered fixture includes timer/deadline events under reference and replay executions | explicit `TimerEvent`s and identical ordered inputs | equivalent isolated canonical transitions/trace | no hidden wall-clock or callback ordering mutation | first divergence reported with versions | `11`, `12`, arch-14; Clock/Core/Replay | ARCH-003/010/011/016/020; A-03/A-09; RAW-ORDER-06 | deterministic schedule/permutation test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-026` | same plan is evaluated in Replay, Paper, Shadow, MicroLive or Live | mode-correct transport selection and effect evidence | isolated mode state; production effect only if exact Live scope permits | Replay/Shadow cannot reach production transport or mutate production balance | unsupported mode/capability rejects | `00`, `10`, `16`; RunMode/Execution/Transport | ARCH-002–004/006/024/025; A-04/A-10; REPLAY-ISO-04 | transport-spy/isolation test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-027` | proven deposit/withdrawal/transfer has no strategy fill | account observation→reconciliation→Inventory classification→Accounting capital flow | actual Inventory and non-trade accounting class as proven | no StrategyPnL, fake fill or execution-success mutation | ambiguous delta locks scope pending proof | `08`, `10`, inv-10; Account/Inventory/Accounting | ARCH-005/008/025/028/029; A-11 | ledger/reconciliation invariant test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-028` | process crashes after sequence assignment but before Recorder durability | restart detects missing durable evidence/cursor gap | gap/health/reconciliation state only | no claim of complete dataset/recovery or invented event | fail incomplete evidence; stop risk/reconcile | `11`, `12`, recorder-03/05; Data/Recorder/Reconciliation | ARCH-001/019/021; A-15/A-24; RAW-ORDER-07 | crash-point/fsync/restart test | `SPECIFIED — TEST NOT EXECUTED`; physical boundary open |
| `FUNC-029` | effective fee changes but topology/market availability/precision does not | FeeVersion/invalidation event | FeeState/economic cache invalidation only | no unnecessary Graph topology/RouteDefinition generation rebuild | incompatible old economic result rejected | `03`, `04`, `11`; Metadata/Fee/Graph/Route | ARCH-007/014/015; A-07/A-16 | change-classification/cache test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-030` | requested q/horizon/model/fidelity falls outside validated support or `Q_validated` has a hole | support check and typed unsupported/OOD result | rejection/trace or bounded recomputation only | no extrapolated authorization, hidden interpolation or missing-as-zero | reject/narrow dependent capability | `06`–`09`, `16`; Models/Simulator/Sizer/Risk/Capability | ARCH-009/021–026; A-08/A-14/A-16/A-23 | boundary/fuzz/capability test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-031` | worker started on generation N completes after generation N+1 or deadline | completion event with captured dependencies | rejection/trace; optionally fresh work scheduled | stale result cannot publish graph/feature/model/size or authorize | discard/recompute; observable deadline result | `00`, `03`, `11`; Core/workers/Graph/Features/Sizer | ARCH-003/009–011/016/020/022; A-03/A-16/A-17 | controlled-scheduler/permutation test | `SPECIFIED — TEST NOT EXECUTED` |
| `FUNC-032` | safe update/restart occurs while runtime/account state may be active | stop-new-risk→drain/preserve safety paths→single-owner transition→startup reconciliation/readiness | deployment/reconciliation/readiness states only until proven | no dual active owner, orphan claim or premature new risk | ambiguous owner/state prevents start and escalates | `10`, `14`, deploy-06/08/10/11; Deployment/Execution/Reconciliation | ARCH-005/017/019/023; A-15/A-24 | restart/lease/split-brain fault test | `SPECIFIED — TEST NOT EXECUTED` |

Exact text for the additional human-audit corpora 2A–2F, 3A–3G, 4A–4H, 5A–5F and 6A–6F was
not present in the supplied repository/prompt. Those scenarios were not invented; their future
cross-reference remains a named missing input.

## 11. Remaining decisions and implementation dependencies

### 11.1 Open decisions and evidence boundaries

| Boundary | Known invariant | Missing decision/evidence | Owner / next treatment | Blocked scope |
|---|---|---|---|---|
| ARCH-016 ingress arbitration | one immutable canonical post-admission order; source/provenance retained | pre-assignment source-priority/arbitration policy for concurrent ingress | Data + human architecture decision; temporal mission must model alternatives without selecting one | precise multi-source schedule/replay proof |
| ARCH-019 P0 durability | P0 loss cannot be silent; Recorder threat stops new risk; Core cannot wait indefinitely on ordinary disk I/O | exact persistence/durability acknowledgment/crash-gap mechanism plus crash/disk-full/torn-write proof | Data/Recorder/Infra; design + fault test | claim of physical durability and complete restart recovery |
| ARCH-026 Risk action fields | `allowed` alone cannot authorize Submit; structured action/reasons/bounds/TTL and current compatibility are required | exact `allowed`/`action` compatibility truth table and field-level Data/Risk contract | Risk + Data + human decision | frozen decoder/validator and Submit compatibility test |
| ARCH-027 Reservation schema | one Reservation owner/lifecycle; atomic claims precede new effects; UNKNOWN retains them | exact serialized fields and compatibility/version rules | Execution + Data + Inventory + human decision | wire schema, persistence migration and exhaustive concurrency tests |
| Accounting interface | actual/expected and trading/non-trading records remain disjoint; Accounting is not Inventory | frozen serialized record fields, versioning and migration | Accounting semantics + Data schema decision | implementation API and ledger serialization tests |
| Route BATCH_SELECT/EARLY_COMMIT | no mixed generation or stale publication | exact policy where still open in owner register | Graph/Data human decision | optimized selection/commit implementation |
| Calibrated constants | semantics and failure policy are fixed; arbitrary thresholds are not | queue sizes, deadlines, batch/fan-out, q search grid, retry bounds, model thresholds | domain owner + Validation benchmarks | production performance/configuration |
| External exchange behavior | unknown rules/API behavior fails closed | current primary Hyperliquid confirmation for API, fee, precision, transport/error semantics | external revalidation before implementation | adapter/transport conformance |
| Human scenario corpora | available `A-*`, RAW and Replay scenario texts are preserved | exact 2A–2F, 3A–3G, 4A–4H, 5A–5F, 6A–6F texts | human audit input | final cross-corpus scenario consolidation |
| Implementation evidence | M0 contracts specify intended behavior | Rust symbols, runtime tests, benchmarks, fault drills and deployment evidence | future implementation/Validation missions | M1–M5 and any capital/trading authority |

### 11.2 Deduplicated functional backlog

| Category | Deduplicated items | Status / exit evidence |
|---|---|---|
| Documentary corrections completed | reconcile Graph §17 stage ordering and optional models; enrich all 31 live interfaces; add ten module maps; assess 46/46 FOPs and add 13 selected operation children; retain complete parent+table coverage for 33; preserve 32 scenarios | review delta; quality checks in §12 |
| Documentary corrections blocked | ARCH-016 arbitration, ARCH-026 mapping, ARCH-027 fields, Accounting serialized schema, any unavailable human scenario text | owner/human decision required; no placeholder schema/truth table |
| Implementation gaps | all 46 FOP mappings to actual Rust; reducers/writers/transports/artifact/capability/deployment mechanisms; exact Data schemas | implementation review and symbol-level traceability required |
| Tests required | `FUNC-001..032`; operation-child expectations in `ARCH-MAP-025..037`; exact-once/idempotency; generation races; version skew; state machines; UNKNOWN/cancel/partial-fill/restart; Replay determinism; Recorder crash/disk | automated results with immutable EvidenceIds required; documentary specification is not PASS |
| Benchmarks required | C0–C5 allocation, queue/batch/fan-out/deadlines, Formula/FastL1 parity and performance, q search, inference/simulator bounds | workload and hardware-scoped benchmark evidence |
| External verification | current Hyperliquid API/WS/account/order/error, fee and precision semantics | dated primary-source evidence in External Revalidation Register |
| Future deferred functions | F4, complex portfolio allocator/Bridge activation, maker modes, optional nodes, distributed research/advanced model dependencies | remain disabled until separate maturity, capability and human approval |

No item in this backlog grants implementation, technical maturity, capital or trading authority.

## 12. Non-regression results

Only checks actually executed in this working tree are reported here. “PASS” for a documentary
check does not mean implementation, runtime, scientific, maturity or capital validation.

| Check actually executed | Result |
|---|---|
| branch / HEAD / tree / upstream | `PASS` — `audit-corrections-p1`; `377e500dfe1d776ea4a57745c9d48c5882f58be8`; tree `910f5fd9e280f3ec52c609396fc5999031dd942f`; `origin/audit-corrections-p1` equals HEAD before this uncommitted delta |
| working-tree scope | `PASS` — exactly two task files under `docs_v2/`; unrelated untracked `.DS_Store` excluded; no production source modified |
| `git diff --check` | `PASS` — no whitespace error in the current two-file delta |
| full changed-file review | `PASS` at documentary level — the complete atlas/report delta was inspected; no domain owner, production file or historical conclusion was edited |
| Markdown internal links and fragments | `PASS` — local-target and fragment checkers resolved links across both modified files, including every parent/child map anchor |
| Markdown tables | `PASS` — column-count parser accepted every table across both modified files |
| Mermaid syntax/render | `PASS` — cached local Mermaid CLI `12.2.0` rendered all `37/37` blocks in the maintained atlas; Chromium execution required the permitted local out-of-sandbox run |
| component inventory | `PASS` — canonical catalog `42/42`; report matrix `42/42` |
| interface inventory | `PASS` — maintained catalog `31/31`; report matrix `31/31` |
| function-level diagram assessment | `PASS` — all `46/46` unique `FOP-*` rows have one explicit disposition: `13` detailed child maps and `33` parent-plus-contract-table dispositions |
| function/scenario/map identifiers | `PASS` — 46 unique `FOP-*`; contiguous `FUNC-001..032`; contiguous `ARCH-MAP-001..037`, preserving `001..014`; explicit parent/child anchors cover `015..037` |
| preserved architecture/invariant inventories | `PASS` — `ARCH-001..029`, QF-001..110, INV-001..030, SI-001..029, HDC-001..100 and `PREC-P01..P19` present and contiguous in their governing inventories |
| preserved roadmaps/maturity/priority | `PASS` — Formula, Risk, Execution, Data, Recorder, Validation and roadmap owner files are unchanged; therefore the five ESMs, 26 technical phases, 21 evidence stages, M0–M5, P0–P3 and `DELTA_RECERTIFICATION_REQUIRED` were not edited |
| state-writer uniqueness | `PASS` documentary review — 42-row component matrix, PASS13 ownership and new maps compared; no second canonical writer introduced |
| Command / Event / Effect ownership | `PASS` documentary review — intent, ordered observation, external effect, ACK, fill and cancel confirmation remain distinct; Transport is the effect boundary |
| producer/consumer compatibility | `PASS` documentary review — all 31 interfaces now expose producer, consumers, versions, validity/absence behavior and acceptance anchor |
| optional dependency search/review | `PASS` — Graph §17 and maps explicitly make Participants/Simulator capability-dependent; conservative baseline is not made universally dependent on them |
| Risk/Reservation bypass search/review | `PASS` documentary review — proposal → full Risk → atomic Reservation → immutable plan → pre-send → mode transport; no new effect bypass found |
| actual-versus-forecast mutation search/review | `PASS` documentary review — Simulator/forecast outputs cannot mutate FillLedger/Account/Inventory; only unique proven actual facts do |
| Replay isolation search/review | `PASS` documentary review — isolated ingress/Clock/C0/state and emulator/disabled effect path; no Replay arrow to Live mutable state/Transport |
| RAW/rejection/sequence provenance | `PASS` documentary review — RAW identity, `source_raw_event_id`, `recorder_seq`, typed rejection and sequence-before-durability gap remain explicit |
| formula/Risk/ESM semantic authority | `PASS` — `04_FORMULA_BOOK.md`, `09_RISK_CONSTITUTION.md` and `10_EXECUTION_STATE_MACHINE.md` have no Prompt-2 diff; no QF, Risk rule or state machine changed |
| runtime/unit/integration/fault/benchmark/scientific tests | `NOT EXECUTED` — no implementation exists in the audited scope; all `FUNC-*` rows remain specifications |
| current external Hyperliquid verification | `NOT EXECUTED` — mutable external facts remain in the existing revalidation boundary |

No check above closes ARCH-016, ARCH-019, ARCH-026, ARCH-027, Accounting serialization,
calibration, implementation or human approval.

## 13. Modified-file ledger

| Path | Diff vs HEAD | Current deepening delta | Authority role | Scope guard |
|---|---:|---|---|---|
| `docs_v2/deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md` | `+535/-2` | added `ARCH-MAP-025..037`, stable parent anchors, navigation contract and operation-level contract tables | maintained navigation atlas | maps consume domain authorities; `001..024` identities preserved; no algorithm or implementation claim added |
| `docs_v2/_analysis/f2_final_integration/PROMPT2_FUNCTIONAL_ARCHITECTURE_CORRECTION_REPORT.md` | `+117/-31` | added the 46/46 selection matrix, 13-map coverage, remaining gaps and current non-regression evidence | non-authoritative audit artifact | records disposition and evidence only; no owner contract or prior conclusion replaced |

The prior five-file Prompt-2 completion is preserved in commit
`377e500dfe1d776ea4a57745c9d48c5882f58be8`. The current complete two-file deepening patch is
inspectable with `git diff --` followed by the two paths above. `.DS_Store` is unrelated/excluded,
and no historical PASS, legacy `/docs`, domain-owner or production file changed.

## 14. Prompt 3/6 handoff

Prompt 3 must consume, not reinterpret, the following functional baseline. This is an input
contract only; no temporal/concurrency design is begun here.

### 14.1 Producer/consumer and canonical-writer inputs

| Temporal input | Prompt-2 baseline to preserve |
|---|---|
| Functional producer/consumer map | the 31-row maintained Domain Interface Catalog and §4; every absence/failure is explicit |
| Detailed operation map | `ARCH-MAP-025..037` expose the selected C0/C2/C3/C4, state, version, effect and failure paths; the other 33 FOPs remain governed by parent+§5 table |
| Canonical writers | Book, Metadata, Fee, Precision, Graph, Route generation, Feature, Atlas, Inventory, Risk, Reservation, Execution-family, Recovery, Reconciliation, Accounting, Recorder, artifact, capability, infra, deployment and license states each retain their named single writer; readers/workers never commit directly |
| Commands/events/effects | command expresses intent to owner; event is ordered evidence/observation; external effect is executed only by mode-correct Execution Transport after current Risk/Reservation/plan gates; ACK/cancel request are not fill/terminal proof |
| Snapshot requirements | immutable inputs carry Book/Graph/Route/index/Metadata/Fee/Precision/Feature/Inventory/account/model/formula/config/capability and time identities as applicable; incompatible or expired combinations reject/recompute |
| RunMode boundary | equivalent functional semantics, separate mutable state/ingress/clock/transport; Replay and Shadow cannot touch production transport/state |
| Recorder handoff | bounded priority-aware handoff is distinct from persistence and physical durability; P0 threat stops new risk; crash gap and reconciliation remain explicit |

### 14.2 Timing, worker and failure inputs

| Area | Required Prompt-3 treatment |
|---|---|
| C0 | define the one canonical ordered commit boundary per isolated run and how timer/account/market/worker-completion events enter it without a second coordinator |
| C1–C5 | map existing timing classes to bounded pure calculations, I/O/effects, persistence/operations and scientific/background work; do not silently reclassify safety-critical semantics |
| Workers | capture immutable dependency versions at dispatch; completion is an event/candidate, never a commit; owner validates deadline/currentness before atomic publication |
| Stale results | exercise `FUNC-003`, `005`, `016`, `025`, `029`, `030`, `031`; stale/late/mixed result is rejected or recomputed and cannot authorize an effect |
| Shared capacity | exercise `FUNC-012`, `015`, `017`, `019`, `032`; model Reservation atomicity, UNKNOWN retention, fill-driven release/update and restart reconciliation |
| Recorder | carry P0–P3 priority, bounded enqueue, quality state, stop-new-risk and incomplete-durability behavior into schedules; do not equate queue acceptance with disk durability |
| Effects | prove pre-send/later-leg current revalidation and exact RunMode transport; no worker/model/dashboard/callback may directly send |
| Recovery/restart | schedule cancellation, late fills, UNKNOWN query, orders→fills→balances reconciliation and single active deployment owner without inventing terminal facts |

### 14.3 Decisions and tests Prompt 3 must not hide

- Keep ARCH-016 OPEN while modeling concurrent source admission and deterministic post-admission
  order; do not choose an ingress priority rule implicitly.
- Keep ARCH-019 OPEN until a physical persistence/durability design and crash proof exist; temporal
  diagrams must show the possible sequence-to-durability gap.
- Keep ARCH-026/027 field decisions outside concurrency design while enforcing their known
  fail-closed/atomic lifecycle invariants.
- Use `FUNC-001..032` as temporal test inputs, with particular focus on event permutations,
  deadlines, worker staleness, generation publication, UNKNOWN/cancel races, partial fills,
  Recorder pressure/crash, Replay schedule equivalence and restart/split-brain behavior.
- Reuse `ARCH-MAP-015..024` as module navigation and `ARCH-MAP-025..037` as detailed operation
  inputs, then link temporal claims to owning contracts and future verified symbols. Do not create
  a second functional authority or treat these documentary maps as Prompt-3 completion.

Prompt 3 must report decisions it needs rather than treating this M0 functional completion as
runtime proof or human approval.

`PROMPT 2/6 — FUNCTIONAL ARCHITECTURE DOCUMENTARY CORRECTION COMPLETE — HUMAN REVIEW REQUIRED`
