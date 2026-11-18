# Prompt 1/6 — Global Architecture Documentary Correction Report

`DOCUMENTATION STATUS: CORRECTED WORKING CANDIDATE — HUMAN REVIEW AND DELTA RECERTIFICATION REQUIRED`

This focused report records the source-backed architecture corrections requested after the F2
candidate was assembled. It is an analysis/disposition artifact, not a new Master, Formula, Risk,
Data or issue authority. Owning canonical documents continue to win.

## 1. Executive result and exact scope

- Correction base: commit `9edc8bb12f39e49f92bb594d265384de143ea849`, tree
  `1ee9b176e47ff8d1418e9bb0ea0fb125fd7c5dfa`.
- Correction branch: `audit-corrections-p1`, created from `f2-governance-p3` so the base remains a
  recoverable comparison point.
- Candidate identity: the correction working tree is intentionally uncommitted while this report
  is authored. Its eventual exact commit/tree must be selected and recorded externally; branch or
  moving `HEAD` is not an immutable review subject.
- Scope: documentary architecture, diagrams, navigation, dated external assumptions and review
  status only. No production source, formula, Risk semantic, order permission, capital permission
  or implementation status is changed.
- Result: the confirmed diagram/document conflicts are corrected. Existing conformant contracts
  are referenced instead of rewritten. Unresolved source/human decisions remain OPEN and cannot
  authorize dependent implementation.
- Implementation facts established: none. This repository snapshot contains documentation, not
  implementation evidence for the described engine.

## 2. Changed-file ledger

| File | Problem | Correction | Findings | Verification target |
|---|---|---|---|---|
| `docs_v2/00_MASTER_ARCHITECTURE.md` | linear overview implied Recorder blocking, one late Risk check and incomplete state ownership | separated ingress/Recorder, preliminary/full Risk, Sizing, Reservations, Transport, Replay/Research and Accounting ownership | 001–003, 006, 010, 012, 018, 024 | Mermaid compile, owner comparison |
| `docs_v2/11_DATA_CONTRACTS.md` | current public-book facts, reconnect readiness, containment, historical normalization and non-trade flows needed explicit closure | added dated exchange facts, five-step readiness, RAW rejection/containment, live/history split and balance-flow semantics | 013–017, 029 | official-source check, links |
| `docs_v2/_analysis/EXTERNAL_REVALIDATION_REGISTER.md` | exchange checks were not refreshed for this correction | recorded dated official public `l2Book`, depth and optional standalone-server constraints | 013, 014 | URL and date review |
| `docs_v2/_analysis/async_concurrency_architecture/RECORDER_BACKGROUND_IO_CONTRACT.md` | active secondary P0–P3 table conflicted with reviewed priority meaning | aligned P0 safety/economic, P1 protected incident, P2 general market and P3 optional diagnostic evidence | 019, 020 | terminology search |
| `docs_v2/12_RECORDER_AND_REPLAY.md` | P0 summary omitted several critical classes present in its authoritative PASS06 matrix | expanded P0 summary to orders/fills/account/fees/Risk/Reservations/Execution/Recovery/Reconciliation/journal | 019–021 | authority comparison |
| `docs_v2/_analysis/async_concurrency_architecture/ASYNC_QUEUE_AND_BACKPRESSURE_MATRIX.md` | P1 treated generic RAW as protected and P2/P3 were merged | split P1 protected windows, P2 general market and P3 derived/diagnostic behavior | 019, 020 | authority comparison |
| `docs_v2/_analysis/async_concurrency_architecture/FUNCTION_CONCURRENCY_MATRIX.md` | all RAW chunk writes were labeled P1 | split protected P1, general P2 and derived P3 Recorder functions | 019, 020 | authority comparison |
| `docs_v2/_analysis/corr02_hot_path_performance/LOCK_FREE_FAILURE_AND_BACKPRESSURE_MATRIX.md` | P0/P1 and P2/P3 were merged in ways that obscured distinct preservation semantics | restored four separate Recorder priority rows and P0 durability/UNKNOWN behavior | 019, 020 | authority comparison |
| `docs_v2/_analysis/f2_final_integration/F2_ARCHITECTURE_DIAGRAM_ATLAS.md` | five navigation maps had misleading arrows and insufficient depth links | replaced them with corrected Mermaid system, functional, temporal, containment and ownership/authorization views | 001–006, 010, 012, 015, 018, 022, 024–029 | Mermaid compile, owner comparison |
| `docs_v2/_analysis/pass08_graph_routes_quant/ROUTE_GENERATION_AND_INVALIDATION_MATRIX.md` | publication wording permitted mixed Graph/Route/index generations | made off-side build plus coherent immutable generation publication explicit | 022 | contradiction search |
| `docs_v2/_analysis/pass08_graph_routes_quant/ROUTE_ECONOMICS_PIPELINE.md` | active economics pipeline showed an ambiguous combined Participants/Simulator/Risk/Sizing tail | separated optional supported forecasts, preliminary Risk, Sizing, full Risk and atomic Reservations | 002, 006, 024–027 | contradiction and owner check |
| `docs_v2/_analysis/pass13_master_architecture/DOMAIN_INTERFACE_CATALOG.md` | Accounting output semantics were under-specified | linked stable identity, disjoint attribution and non-trade capital flow | 028, 029 | ownership comparison |
| `docs_v2/_analysis/pass13_master_architecture/STATE_OWNERSHIP_MATRIX.md` | Accounting was absent from the explicit state-owner inventory | added its sole writer/readers/version/persistence/replay row without a competing aggregate type | 012, 028, 029 | single-writer review |
| `docs_v2/_review/16_EXTERNAL_REVALIDATION_CHECKLIST.md` | reviewer checklist did not show the latest exchange refresh | recorded the dated snapshot/depth semantics and safe fallback | 013, 014 | URL/date review |
| `docs_v2/deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md` | deep operational coverage lacked Risk/Execution and two mandatory worked examples | added maps 011–013 and links from corrected F2 maps | 005, 006, 012, 019, 024–027 | Mermaid compile, link check |
| `docs_v2/deep-specs/market-graph/05_OPPORTUNITY_DETECTION_AND_SIZE_DEPENDENT_ECONOMICS.md` | active secondary pipeline showed unconditional Participants/Simulator and only one ambiguous Risk position | aligned optional model inputs and the preliminary Risk → supported Sizing → full Risk → Reservations ordering | 002, 006, 024–026 | contradiction and owner check |
| `docs_v2/deep-specs/market-microstructure/06_INCREMENTAL_FEATURE_ENGINE_AND_HOT_PATH_CONSTRAINTS.md` | ownership summary named only generic Risk eligibility before PASS07 sizing | clarified the same Risk owner's preliminary and full checkpoints around Sizing | 006, 024, 026 | owner check |
| `docs_v2/_analysis/corr05_economic_integration/ACCOUNTING_RECONCILIATION_MAP.md` | deposits, withdrawals, transfers and MTM were not fully separated from trading PnL/quantity | added owner-specific non-trade handling without inventing a new canonical bucket | 007, 028, 029 | accounting-owner review |
| `docs_v2/_analysis/f2_final_integration/F2_FINAL_HUMAN_REVIEW_HANDOFF.md` | old reading order/status did not include this material correction | adds this report and requires selection/recertification of the future exact corrected snapshot | cross-cutting | review-state check |
| `docs_v2/_review/00_REVIEW_START_HERE.md` | reviewer entry point could imply the old candidate covered later corrections | links this report and marks the changed snapshot for new differential review | cross-cutting | review-state check |
| `docs_v2/README.md` | no top-level route to the correction evidence | adds the focused correction report to review navigation | traceability | link check |
| this report | no suitable existing artifact could hold 29 auditable dispositions without rewriting history | adds a focused disposition, verification and Prompt-2 handoff record | 001–029 | completeness/count check |

## 3. ARCH disposition matrix

Each audit finding appears once in this matrix. “Corrected” means documentary correction only.

| ID | Source authority | Finding / class | Corrected or inspected files | Correction applied | Scenarios | Required outcome | Remaining proof / decision | Status |
|---|---|---|---|---|---|---|---|---|
| ARCH-001 | `12_RECORDER_AND_REPLAY.md`; async Recorder contracts | blocking Recorder arrow / `DIAGRAM_ERROR` | `00_MASTER_ARCHITECTURE.md`; F2 atlas; visual atlas; async Recorder matrices | reception, ordered ingress, capture, bounded handoff, disk and health are separate | A-03, A-15, A-16 | Core never waits indefinitely for disk; P0 failure remains observable and fail-safer | crash/backpressure/durability tests | `DIAGRAM_CORRECTED`; `IMPLEMENTATION_NOT_VERIFIED` |
| ARCH-002 | `06_MARKET_PARTICIPANTS.md`; `07_COUNTERFACTUAL_SIMULATOR.md`; Capability/Risk contracts | advanced models looked mandatory / `DIAGRAM_ERROR` | Master; both atlases; market-graph pipeline | optional/promoted model edges and fail-closed dependent capability are explicit | A-08, A-11, A-12, A-14 | conservative TT mechanics remain developable without every advanced model | support/capability tests and later activation review | `DIAGRAM_CORRECTED` |
| ARCH-003 | `12_RECORDER_AND_REPLAY.md`; validation contracts | Replay roles blurred / `DOC_AMBIGUITY` | F2 atlas; visual atlas | isolated reconstruction Core is distinct from experimental Replay datasets/validation | A-03, A-09, A-10 | no circular dependency from Replay into the Live Core | deterministic Replay equivalence | `DOCUMENTATION_CORRECTED` |
| ARCH-004 | `11_DATA_CONTRACTS.md`; `12_RECORDER_AND_REPLAY.md` | current Hyperliquid-only scope / `ALREADY_RESOLVED` | Data contract; external register/checklist inspected | venue-aware identity preserved without adding multi-venue V1 infrastructure | A-04, A-13 | V1 records Hyperliquid while contracts remain extensible | adapter/source conformance; future venue expansion separate | `DOCUMENTATION_ALREADY_CONFORMANT` |
| ARCH-005 | PASS13 component/interface/ownership catalogs | insufficient visual depth / `TRACEABILITY_GAP` | F2 atlas; visual atlas; this report | L0–L4 drill-down plus module/interface/error/contract navigation added | A-21, A-22, A-24 | reader can navigate system → contract/test without one unreadable map | align to implementation when it exists | `DOCUMENTATION_CORRECTED` |
| ARCH-006 | `09_RISK_CONSTITUTION.md`; `08_INVENTORY_AND_CAPITAL.md`; `10_EXECUTION_STATE_MACHINE.md` | inconsistent Risk/Sizing arrows / `DIAGRAM_ERROR` | Master; both atlases; route-economics and market-graph/microstructure pipelines | one Risk owner now performs preliminary eligibility, then supported Sizing, full authorization, Reservations and pre-send checks | A-05, A-07, A-16–A-18 | early filtering never replaces final Risk; no competing Risk owner | expiry/staleness/reservation tests; ARCH-026/027 remain open | `DIAGRAM_CORRECTED` |
| ARCH-007 | `04_FORMULA_BOOK.md` QF-016; Data/Accounting contracts | third-asset fee handling / `ALREADY_RESOLVED` | Formula/Data sources inspected; accounting map clarified | explicit multi-asset deltas retained; no universal valuation convention invented | A-07, A-20, A-23 | economic comparison declares valuation convention and never silently edits QF-016 | multi-asset fee/property tests | `DOCUMENTATION_ALREADY_CONFORMANT` |
| ARCH-008 | Formula Book FastL1/BBO contracts; Validation Matrix | optimization could look authoritative / `ALREADY_RESOLVED` | Formula/Book sources inspected; navigation linked | exact-parity/fallback and sufficient-proof boundaries preserved | A-07, A-20, A-22 | unsupported FastL1 falls back; BBO-C2 cannot replace full L2 universally | parity/fallback/bound tests | `DOCUMENTATION_ALREADY_CONFORMANT` |
| ARCH-009 | Data/Book/Graph/Risk/Execution version contracts | temporal coherence under-shown / `TRACEABILITY_GAP` | both atlases; Master | immutable version dependencies, freshness, stale rejection and pre-send revalidation shown | A-07, A-16, A-17 | compatible bounded changes may pass; incompatible stale combinations may not authorize | multi-market coherence/stale-result tests | `DOCUMENTATION_CORRECTED` |
| ARCH-010 | async C0–C5 contract | runtime/scientific workers conflated / `DIAGRAM_ERROR` | F2 atlas; visual atlas | C2 bounded proposals separated from C5 offline science | A-03, A-09, A-16, A-20 | C5 never becomes a hot-path or commit dependency | concurrency/permutation/capacity evidence | `DIAGRAM_CORRECTED` |
| ARCH-011 | route-fanout policy contract; async experiment matrix; HDC-093 | unsettled selection policy / `CALIBRATION_REQUIRED` | source contracts and this report inspected | both `BATCH_SELECT` and deterministic `EARLY_COMMIT` remain documented without selection | A-03, A-16, A-18–A-20 | common cohort, deterministic ties, deadlines and capacity checks for either policy | Replay + Shadow benchmark and human selection | `OPEN_HUMAN_DECISION` |
| ARCH-012 | PASS13 state/component/event ownership matrices | Accounting/Recorder ownership gap / `TRACEABILITY_GAP` | state matrix; interface catalog; both atlases | explicit writers/readers/versions/persistence/replay paths added without second authority | A-02, A-04–A-07 | one logical writer for Inventory, Risk, Execution, Account, Reservations, Graph, Recorder, Accounting | implementation single-writer/event tests | `DOCUMENTATION_CORRECTED` |
| ARCH-013 | `11_DATA_CONTRACTS.md`; official Hyperliquid docs; external register | exchange semantics mutable / `EXTERNAL_REVALIDATION` | Data contract; external register; external checklist | dated public snapshot semantics added; fabricated diffs/L3 forbidden | A-01, A-07, A-13, A-22 | adapter implements only verified snapshot/incremental semantics | captured conformance/reconnect tests and implementation-time refresh | `OPEN_EXTERNAL_REVALIDATION` |
| ARCH-014 | Book/Formula depth contracts; official public-feed limits | fixed depth could be misread as sufficient / `DOC_AMBIGUITY` | Data contract; external register/checklist; shared-depth map | observed depth and source limits distinguished from q sufficiency | A-07, A-16, A-17, A-20 | exact economics uses all supported observed levels and returns insufficient depth otherwise | truncation/depth exhaustion tests | `DOCUMENTATION_CORRECTED` |
| ARCH-015 | Data/Book/Capability readiness contracts | connection equated with readiness / `DIAGRAM_ERROR` | Data contract; F2 atlas; visual reconnect map | five evidence states from connection through market admissibility are explicit | A-01, A-07, A-15–A-17 | socket/subscription health alone never permits trading | reconnect/resync/readiness tests | `DIAGRAM_CORRECTED` |
| ARCH-016 | data time/ordering contract; PASS06 event-order contract | pre-sequence tie policy absent / `HUMAN_DECISION_REQUIRED` | F2 temporal map; visual atlas open-boundary list; this report | post-assignment order preserved and missing pre-assignment policy left explicit | A-03, A-07, A-16 | no invented tie-break; policy must be deterministic and versioned | concurrent-arrival evidence and Data/Architecture approval | `OPEN_HUMAN_DECISION` |
| ARCH-017 | Data/Normalizer/Recorder rejection contracts | rejection scope/provenance needed clarity / `DOC_AMBIGUITY` | Data contract; F2 failure map | RAW lineage, reason/context, scoped containment and non-mutation made explicit | A-01, A-07, A-13 | unknown events never become fabricated known events or mutate canonical state | invalid/unknown event corpus and mutation tests | `DOCUMENTATION_CORRECTED` |
| ARCH-018 | ordered-ingress and `recorder_seq` contracts | disk completion could look authoritative / `DIAGRAM_ERROR` | Master; both atlases | sequence assignment is at ordered ingress; writer completion is off the economic order path | A-03, A-07, A-15 | disk scheduling never creates a second canonical order | reorder/disk-delay tests | `DIAGRAM_CORRECTED` |
| ARCH-019 | Recorder master and authoritative priority matrix; Execution/Risk/Reconciliation | physical P0 durability unproved / `TEST_GAP` | Recorder master; four active async/backpressure matrices; both atlases | P0 classes aligned; intent/transmission/result/durability/UNKNOWN/restart/reconcile boundary shown | A-05, A-15–A-17, A-24 | no silent P0 loss and no indefinite Core disk wait; received fills still apply | fsync/ack design, disk-full, crash/torn-write/restart drills | `DOCUMENTATION_CORRECTED`; `TEST_NOT_IMPLEMENTED` |
| ARCH-020 | async queue/backpressure contracts | queue constants/lock-free choice unsettled / `CALIBRATION_REQUIRED` | async Recorder/background, queue, function and lock-free matrices | semantic bounds and four priority classes aligned; no mandatory lock-free claim | A-15, A-16, A-20, A-24 | bounded observable degradation without weakening canonical order/safety | workload benchmark, capacities/deadlines/batching | `DOCUMENTATION_CORRECTED`; `CALIBRATION_REQUIRED` |
| ARCH-021 | Recorder chunk/manifest/checkpoint contracts | crash ordering review / `ALREADY_RESOLVED` | Recorder source and active matrices inspected | write/check/finalize/manifest/archive/retention ordering retained; incomplete artifacts stay invalid | A-07, A-15, A-24 | checkpoint accelerates recovery but never becomes independent truth | torn-write/incomplete-manifest/recovery tests | `DOCUMENTATION_ALREADY_CONFORMANT` |
| ARCH-022 | Graph/Routes generation contracts | mixed generation visibility / `DOC_CONFLICT_CONFIRMED` | route-generation matrix; both atlases | off-side build plus coherent compatible generation publication replaces sequential exposure | A-03, A-07, A-16, A-17 | no new Graph with incompatible old route/index; no distributed transaction invented | generation race/stale-worker implementation tests | `DOCUMENTATION_CORRECTED`; `IMPLEMENTATION_NOT_VERIFIED` |
| ARCH-023 | Formula QF-026/027/076; Sizing contracts | finite samples could imply global optimum / `ALREADY_RESOLVED` | route-economics source and this report inspected | sampled, feasible, demonstrated and proven bounds remain distinct | A-16, A-19, A-20, A-23 | finite grid is not proof; search policy stays open where unsourced | property/bound tests, benchmark and possible human selection | `OPEN_HUMAN_DECISION` |
| ARCH-024 | technical roadmap phases 17/18; Risk/Capability contracts | provisional q looked tradable / `DIAGRAM_ERROR` | Master; both atlases; route/market pipelines | provisional sizing is followed by full Risk, Reservations and pre-send gates | A-05, A-11, A-14, A-18, A-23 | mechanics alone create no capital/order permission | bootstrap/no-authority tests and separate activation | `DIAGRAM_CORRECTED`; `IMPLEMENTATION_NOT_VERIFIED` |
| ARCH-025 | Simulator dependence/support/OOD contracts; Risk model gates | model dependence/support boundary / `ALREADY_RESOLVED` | Simulator/Risk sources inspected; refusal map added | favorable forecast is separated from hard gates, support and OOD refusal | A-08, A-11, A-12, A-14, A-20 | no unsupported q extrapolation or independence double count | joint-model calibration/OOD tests | `DOCUMENTATION_CORRECTED`; `CALIBRATION_REQUIRED` |
| ARCH-026 | Risk Constitution §17; deep Risk decision/transport contracts | boolean/action ambiguity / `HUMAN_DECISION_REQUIRED` | both atlases; this report; canonical Risk text preserved | `allowed` alone never authorizes; action/bounds/all gates required; no truth table invented | A-05, A-07, A-16, A-17, A-23 | contradictory/unresolved pairs fail closed for new risk | Data/Risk source decision then transport contradiction tests | `OPEN_HUMAN_DECISION` |
| ARCH-027 | Data/Risk/Execution reservation contracts | field-level schema absent / `HUMAN_DECISION_REQUIRED` | both atlases; ownership/interfaces inspected; this report | owner/lifecycle semantics retained without inventing fields | A-02, A-05, A-07, A-18, A-19, A-23 | one authoritative schema with versions/lifecycle before implementation | Data-owner schema decision and serialization/lifecycle tests | `OPEN_HUMAN_DECISION` |
| ARCH-028 | Inventory/Account/Accounting contracts; PASS13 ownership | apparent mutation cycle / `DOC_AMBIGUITY` | state matrix; interface catalog; accounting map; both atlases | balance, quantity and accounting-record authorities explicitly separated | A-02, A-07, A-11, A-22 | unique actual fills have one owner/attribution path; Accounting cannot mutate Inventory | exact-once fill/fee/reconciliation tests; record schema remains Data-owned | `DOCUMENTATION_CORRECTED` |
| ARCH-029 | Data account events; Inventory/Accounting contracts | non-trade changes under-specified / `DOC_AMBIGUITY` | Data contract; accounting map; ownership/interfaces | deposits/withdrawals/transfers treated as capital flows outside trading PnL; MTM changes value not quantity | A-01, A-02, A-07, A-22 | idempotent provenance/reconciliation without deposits as profit | capital-flow dedupe/reconciliation tests; declared valuation convention | `DOCUMENTATION_CORRECTED` |

## 4. Corrected and embedded diagrams

| Diagram | Location / level | Scope and authoritative source | Related findings | Syntax status |
|---|---|---|---|---|
| F2 Map 1 | F2 atlas, L0/L1 | global runtime, evidence and first baseline; Master/PASS13 | 001–005, 010, 018–020 | `PASS` — Mermaid CLI 12.2.0 |
| F2 Map 2 | F2 atlas, L1/L2 | functional owners, optional models and Risk stages; PASS13/domain Masters | 002, 005–008, 010, 012, 023–028 | `PASS` — Mermaid CLI 12.2.0 |
| F2 Map 3 | F2 atlas, L1/L2 | C0–C5 timing and stale rejection; Async contract | 003, 010, 011, 016, 018–021 | `PASS` — Mermaid CLI 12.2.0 |
| F2 Map 4 | F2 atlas, L1/L2 | scoped failure, P0, UNKNOWN and reconciliation; Data/Risk/Execution | 009, 013–017, 019–021, 025–029 | `PASS` — Mermaid CLI 12.2.0 |
| F2 Map 5 | F2 atlas, L1/L2 | state writers and permission intersection; PASS13/Capability/F2 | 006, 012, 024–029 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-001 | maintained atlas, L0 | end-to-end system; Master/PASS13 | 001–006, 010, 012 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-002 | maintained atlas, L1/L2 | state ownership; PASS13 | 012, 027–029 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-003 | maintained atlas, L1/L2 | C0–C5; Async contract | 010, 016, 018–020 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-004 | maintained atlas, L1/L2 | failure containment; Risk/Execution/Recorder | 013–021, 026–029 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-005 | maintained atlas, L1/L2 | evidence versus authorization; Validation/Capability | 002, 024–026 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-006 | maintained atlas, L3/L4 | connected-but-invalid Book; Data/Book/Graph | 009, 013–015 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-007 | maintained atlas, L3/L4 | coherent Graph/Routes generation; Graph | 022 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-008 | maintained atlas, L3/L4 | Recorder disk/P0 failure; Recorder/Risk/Reconciliation | 001, 019–021 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-009 | maintained atlas, L3/L4 | illustrative 20 → 13.7 partial TT; Execution/Inventory | 006, 025, 027–029 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-010 | maintained atlas, L2–L4 | scientific candidate cannot self-authorize; Validation/Capability | 002, 003, 010, 024 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-011 | maintained atlas, L2–L4 | Risk/Execution normal and failure paths; Risk/Execution | 006, 009, 024, 026, 027 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-012 | maintained atlas, L2–L4 | illustrative shared L2 capacity; Book/Allocation/Reservations | 009, 014, 018, 023, 027 | `PASS` — Mermaid CLI 12.2.0 |
| ARCH-MAP-013 | maintained atlas, L2–L4 | illustrative favorable forecast/Risk refusal; Simulator/Risk | 002, 006, 024–027 | `PASS` — Mermaid CLI 12.2.0 |

## 5. Deep component navigation

Names below come from the current interface and ownership catalogs; they are documentary
interfaces, not claims that functions are implemented.

| Module | Interface / operation | Input → output | State / version | Error or fallback | Owning contract | Scenarios |
|---|---|---|---|---|---|---|
| Adapter / Normalizer | `RawEvent` normalization | external payload → typed `MarketEvent` / `AccountEvent` / `EngineInputEvent` | source/schema/connection/`recorder_seq` lineage | retain RAW; reject invalid; contain proven scope | Data Contracts; data module contracts | A-01, A-04, A-07, A-13 |
| Book | `BookEngine(MarketEvent) → BookSnapshotRef` | ordered market events → immutable ready/invalid snapshot | `BookVersion`, freshness, gaps | invalidate/resync; connected is not ready | Data; Book/market pipeline | A-01, A-07, A-15–A-17 |
| Graph / Routes | `RouteEngine(BookSnapshotRefs, RouteDefinitions) → RouteEconomics` and generation publication | compatible Book/metadata → route generation/dependency indexes | Graph/Route/index generation | withhold incomplete generation; reject stale worker | Graph and Routes | A-03, A-07, A-16, A-17, A-19 |
| Formula / Opportunity | `NetConvert` and Opportunity evaluation | route, q, rule snapshots → economics / Opportunity or RejectEpisode | Formula, fee, precision, Book and route versions | fallback from unsupported FastL1; fail closed on invalid rules | Formula Book; Opportunity Master | A-01, A-07, A-20, A-22 |
| Participants / Simulator | forecast interfaces | feature/candidate/current state → model or `ExecutionForecast` | model/support/q-band versions | unavailable/OOD blocks only dependent capability; baseline remains | Participants; Simulator | A-08, A-11–A-14 |
| Sizing / Allocation | size curve and allocation proposal | candidate domain/shared constraints → bounded q proposal | validated q/support and dependency versions | no feasible q, overlap or stale capacity → reject/recompute | Inventory and Capital; Sizing deep specs | A-07, A-18, A-19, A-23 |
| Risk | `RiskEngine(RiskSnapshot, ExecutionForecast) → RiskDecision` | immutable snapshots/forecast → action, reasons, bounds, TTL | Risk/config/model/capability versions | reject/halt/recovery-only; contradictory unresolved pair cannot add risk | Risk Constitution | A-05, A-07, A-12, A-16, A-17, A-23 |
| Reservations | reserve/release lifecycle | allowed bounded proposal/current capacity → `ReservationState` | account/book/risk claims, owner, lifecycle | conflict rejects; `UNKNOWN` retains; only proven remainder releases | Execution; Inventory/Capital | A-02, A-05, A-18, A-19 |
| Execution / Transport | `ExecutionCoordinator(ExecutionPlan) → Effects/ExecutionEvents` | plan + current decision/reservations → `OrderIntent` → observations | plan/order/state/dependency versions | expiry/stale/no ACK → no blind retry; `UNKNOWN` + reconcile | Execution State Machine | A-04, A-05, A-07, A-16, A-17 |
| Inventory / Recovery | fill/balance reducers and continuation/recovery | unique actual events → actual exposure and recovery decision | Inventory/Execution/Account versions | partial/unknown uses actual fill, retains outstanding claims | Inventory; Execution; Risk | A-02, A-07, A-11, A-17, A-18 |
| Accounting | exact-once attribution | fills/fees/capital flows/valuations → disjoint accounting records | stable action/entry identity, ledger cursor, valuation version | dedupe/conflict → reconcile; deposits excluded from trading PnL | accounting map; Formula ownership | A-01, A-02, A-07, A-22 |
| Recorder / Replay | enqueue, persist, reconstruct | RAW/canonical/P0 evidence → chunk/journal/manifest → ordered Replay | capture context, `recorder_seq`, checksums/manifests | bounded handoff; P0 loss stops new risk; incomplete chunk invalid | Recorder and Replay; async Recorder contract | A-03, A-09, A-15, A-24 |

## 6. Conflict closure summary

| Conflict | Result |
|---|---|
| Recorder P0–P3 | active secondary table aligned: P0 critical safety/economic, P1 protected incident, P2 general market, P3 optional diagnostics; not IncidentSeverity |
| Recorder non-blocking versus P0 durability | bounded non-blocking Core handoff plus explicit stop-new-risk/UNKNOWN/reconciliation path; physical durability proof remains open |
| Live versus historical normalization | Live stays bounded before ordered ingress; historical re-normalization is offline and cannot create a second truth |
| Graph/Routes generation | one compatible immutable generation is validated and published; no mixed new Graph/old route index and no invented distributed transaction |
| Risk/Sizing | one Risk owner provides preliminary safe domain and final authorization around supported sizing; pre-send check remains mandatory |
| `RiskDecision.allowed/action` | fail-closed rule is clear; exact compatibility truth table remains an OPEN Data/Risk decision |
| Inventory/Accounting | actual balance, held quantity and accounting record owners are distinct; no mutual mutation cycle or second fill authority |
| Current/Future dependencies | conservative TT mechanics do not require every advanced model or Research Factory; unsupported dependent capabilities fail closed |
| Reconnect readiness | connection, subscription, first data, valid Book and market admissibility are separate states |
| F2 approval/recertification | corrections materially change the proposed corpus; earlier review selection cannot cover them, so a future exact snapshot and delta recertification are required |

## 7. Remaining decisions and evidence

| Owner | Precise open question | Source alternatives / why open | Affected scope | Evidence required | Approval |
|---|---|---|---|---|---|
| Data / Architecture | Which deterministic versioned policy arbitrates simultaneous ingress before `recorder_seq` assignment? | source priority/receive evidence may participate, but no exact tie table is frozen | Core/Replay order | permutation, clock-quality and multi-source scenarios | human architecture decision |
| Graph / Opportunity / Async | `BATCH_SELECT` or deterministic `EARLY_COMMIT` for the defined cohort? | both are documented; neither dominates without latency/quality evidence | route selection | common-cohort Replay + Shadow benchmark, deadline/fairness evidence | HDC-093/human decision |
| Data / Risk | What exact pairs of `allowed` and seven semantic actions are valid in each context? | `allowed` alone is insufficient and contradictory pairs fail closed; sources do not freeze the complete mapping | Transport and dependent tests | source reconciliation plus contradiction matrix | human/source decision required |
| Data / Risk / Reservations | What exact fields and version references form `RiskReservation`? | owner/lifecycle semantics exist, field-level schema does not | reservation serialization/lifecycle | authoritative schema review and lifecycle tests | human/source decision required |
| Recorder / Execution / Ops | What physical acknowledgement, fsync/journal, emergency-buffer and deadline design proves P0 durability without indefinite Core blocking? | async queue alone is not proof | order/fill/Risk evidence and restart | disk-full, crash, torn-write, restart/reconciliation drills | design review and calibrated approval |
| Async / Ops | What queue capacities, batch sizes and thresholds meet semantic bounds? | lock-free is optional; no workload evidence chooses numbers | runtime/Recorder workers | representative load/tail/pressure benchmark | calibration review |
| Formula / Sizing | What search policy establishes sampled, demonstrated or proven q bounds? | a finite grid is not a global proof | sizing/performance | property tests, bounds and benchmark | human review if canonical policy changes |
| Data / Adapter | Do implementation-time Hyperliquid public/account feeds still match the dated contracts? | exchange behavior is externally mutable | Book/reconnect/account | official-source refresh and captured adapter conformance | external revalidation gate |
| Data / Accounting | What exact serialized Accounting record schema/version is frozen? | ownership/identity semantics are clear; field-level record is not invented here | ledger/persistence/replay | Data schema review and exact-once tests | source-owner approval |
| Documentation governance | Which future exact corrected commit/tree is selected, and does its delta pass source/human review? | working branch/HEAD cannot self-certify | F2 candidate | link, inventory, source-delta and human review record | human review required |

## 8. Deduplicated backlog

### Documentary corrections completed

- corrected global/F2/operational arrows, ownership, current/Future boundaries and readiness;
- corrected active Recorder priority and Graph generation wording;
- clarified live/history normalization, unknown-event containment, public book semantics and
  non-trade accounting;
- added worked normal/failure paths for Recorder, Book, Graph, Risk/Execution, partial TT, shared
  depth, scientific candidate and Simulator/Risk refusal.

### Documentary corrections blocked

- exact boolean/action mapping, field-level `RiskReservation`, Accounting serialized record and
  pre-sequence arbitration cannot be authored without their named source owners.

### Tests / implementation verification required

- single-writer, stale-version, reconnect, unknown event, shared capacity, reservation, expiry,
  action compatibility, actual-fill, exact-once accounting and Replay equivalence;
- crash consistency, disk full, torn chunks, UNKNOWN restart and reconciliation;
- no production implementation or runtime test is present in this mission.

### Benchmarks required

- route selection policy, queues/backpressure, deadlines, worker pools and q search.

### External exchange checks

- public `l2Book`/depth facts were revalidated from official sources on 2026-11-18; account/private
  and implementation-specific assumptions still require point-of-implementation confirmation.

### Deferred future

- multi-venue Recorder infrastructure, distributed scientific workers/cache and Research Factory
  activation remain future and inactive.

## 9. Acceptance-scenario coverage

| ID | Scenario | Required outcome | Related ARCH | Modules / contracts | Current evidence status |
|---|---|---|---|---|---|
| A-01 | module receives invalid data | no unauthorized critical-state mutation | 013, 015, 017, 029 | Data/Normalizer, Book, Account; F2 Map 4 | documentary path corrected; mutation/fault tests not implemented |
| A-02 | two modules attempt to write the same state | one logical canonical owner | 012, 027–029 | PASS13 ownership, Reservations, Inventory/Accounting; F2 Map 5 | ownership documented; implementation not verified |
| A-03 | worker completion order changes | no arbitrary canonical decision change | 003, 010, 011, 016, 018, 022 | C0/C2, ingress order, Graph generation; F2 Map 3 | deterministic contract documented; permutation tests pending |
| A-04 | unauthorized direct Hyperliquid access | forbidden outside adapters/effects | 004, 012 | Adapter, Transport, command/event ownership | documentary boundary conformant; code conformance unavailable |
| A-05 | Strategy bypasses Risk/Reservations | Submit impossible | 006, 019, 024, 026, 027 | Risk, Reservations, ExecutionTransport; ARCH-MAP-011 | fail-closed contract documented; schema/mapping and transport tests pending |
| A-06 | forbidden circular dependency | identified and reported | 003, 010, 012, 022, 028 | dependency DAG, Replay isolation, worker/state ownership | documentary cycle review complete; implementation unavailable |
| A-07 | old version combined with newer state | reject or explicitly revalidate | 009, 013–018, 022, 026–029 | Book/Graph/Data/Risk/Execution versions | paths documented; stale-version tests pending |
| A-08 | optional module unavailable | only supported dependent capabilities remain active | 002, 024, 025 | Participants, Simulator, Capability, Risk | fallback boundary corrected; capability tests pending |
| A-09 | equivalent Replay and reference Core inputs | same canonical economic semantics | 003, 004, 018, 021 | Recorder/Replay, isolated canonical Core | semantics documented; equivalence test not executed |
| A-10 | Shadow identifies an opportunity | no exchange order or balance mutation | 002, 003, 024, 025 | RunMode, Capability, NullShadowTransport | authorization boundary documented; runtime test unavailable |
| A-11 | Simulator predicts a fill | actual balance unchanged | 002, 024, 025, 028 | Simulator, Account, Inventory, Accounting | actual-fill-only ownership documented; runtime test unavailable |
| A-12 | Participant model proposes an action | Risk remains sovereign | 002, 006, 025, 026 | Participants, Simulator, Risk | diagram/owner correction complete; integration tests pending |
| A-13 | speculative node data appears | not canonical exchange truth | 004, 013, 014 | source profiles, Data/Adapter, external register | dated source boundary documented; external/local conformance open |
| A-14 | advanced model unavailable | conservative baseline not artificially blocked | 002, 024, 025 | Master, Participants/Simulator support, Capability | fallback documented; baseline capability test pending |
| A-15 | Recorder becomes slow | Core bounded/non-blocking; degradation observable | 001, 018–021 | Recorder priority/backpressure, C4, Risk health | four-class contracts aligned; disk-pressure tests pending |
| A-16 | calculation exceeds deadline | stale result cannot authorize | 006, 009–011, 016, 020, 022–026 | C2, Graph, Sizing, Risk, Execution | rejection paths documented; deadline tests/benchmarks pending |
| A-17 | state changes during evaluation | version/validity checked before effect | 006, 009, 015, 022, 026 | Book/Graph/Risk/Execution pre-send | diagram corrected; race tests pending |
| A-18 | two opportunities use same capital | no double reservation | 006, 012, 019, 027 | Sizing/Allocation, Reservations, Risk | atomic-claim path documented; concurrency/schema tests pending |
| A-19 | two routes share L2 depth | shared liquidity counted once | 009, 012, 014, 022, 023, 027 | Book, Graph, Allocator, Reservations; ARCH-MAP-012 | worked path added; capacity/property tests pending |
| A-20 | optimized implementation replaces baseline | contract/parity/performance tests | 008, 010, 020, 023, 025 | FastL1, workers, search/model challengers | evidence gates documented; benchmark/runtime tests pending |
| A-21 | function absent from architecture diagram | traceability gap identified | 005, 012 | component/interface catalog and visual atlas | L0–L4/deep navigation added |
| A-22 | code contradicts canonical contract | nonconformance or reviewed change | 005, 013, 019, 022, 026–029 | all named domain owners and review gate | rule documented; no production code exists to inspect |
| A-23 | Codex proposes sensitive semantic change | human approval required | 006, 011, 016, 023, 026, 027 | open-decision register, Data/Risk/Architecture owners | decisions remain open; no schema/truth table invented |
| A-24 | technical phase declared complete | required tests, proofs and approvals | 005, 011, 013, 019, 020, 023, 025–027 | Validation Matrix, roadmaps, F2 handoff | inventories checked; runtime evidence and human review absent |

The additional human-audit scenario corpora 2A–2F, 3A–3G, 4A–4H, 5A–5F and 6A–6F were not
available as exact text in this correction input and were not fabricated. They remain a pending
input for final consolidation.

## 10. Non-regression and validation record

This table must report executed checks only; it is updated after the working-tree validation run.

| Check | Result |
|---|---|
| `git diff --check` | `PASS` |
| all changed files inspected | `PASS` — diff plus complete changed-atlas/report review |
| repository-local Markdown links | `PASS` — 933 relative targets checked, 0 broken |
| changed Mermaid blocks parsed/rendered | `PASS` — Mermaid CLI 12.2.0 compiled 23 charts across the three changed diagram-bearing files (19 corrected/new mission charts) |
| 29 matrix rows and A-01–A-24 references | `PASS` — 29 unique contiguous rows; 24/24 scenario IDs explicit |
| ARCH matrix shape | `PASS` — every row contains source, inspected/corrected file, correction, scenario, required outcome, remaining proof/decision and status |
| changed-file ledger versus Git scope | `PASS` — 22/22 documentary artifacts represented (21 modified tracked files plus this new report) |
| Recorder active P0–P3 references | `PASS` — Master and async queue/function/background/lock-free matrices align to the PASS06 authority; historical conflict records remain historical |
| F2 versus maintained-atlas role | `PASS` — F2 owns its five-map candidate snapshot; the visual atlas alone maintains stable evolving `ARCH-MAP-*` diagrams; domain contracts own semantics |
| QF-001..110 | `PASS` — 110 unique contiguous; hash `a2e271b27da3d550647c58bb6e3f9c125b304ac2461dce4f054f79d9de424110` |
| SI inventory | `PASS` — 29 unique contiguous; hash `02fd8b6450535dd81cece48fec313c46b7210585ecd4ad9f7859497f2806b60d` |
| HDC inventory | `PASS` — 100 unique contiguous; hash `8ec95ddaf6be694de77f9ef6fe84f142e96db58f8f1fa11d77a4f8b6a5254014` |
| PREC inventory | `PASS` — 19 unique contiguous |
| 26 phases / 21 stages / M0–M5 | `PASS` — exact `1..26`, legacy stage indices `0..20` / canonical ordinals `1..21`, and six levels |
| INV-001..030 | `PASS` — 30 unique contiguous; hash `d938254e11ce4e3173b62d9a58068bae52869bd0151875a3490966b0184d3024` |
| Formula/Risk/ESM/Validation/roadmap authorities | `PASS` — canonical files byte-unchanged relative to correction base; existing Execution machines and authorization ceilings preserved |
| exact-once ownership, first conservative baseline and inactive Factory | `PASS` — source comparison and corrected diagrams preserve all three; no formula or capital promotion added |
| F2 review status | `PASS` — corrected candidate explicitly remains `DELTA_RECERTIFICATION_REQUIRED`, unselected and unapproved |
| no production code / new authority / permission change | `PASS` — all mission changes are under `docs_v2/`; report is L3 analysis only |
| runtime or implementation tests | `NOT EXECUTED — documentation-only repository mission` |

## 11. Complete diff inspection

The fixed comparison base is
`9edc8bb12f39e49f92bb594d265384de143ea849`. The complete correction delta is the Git comparison
between that base and the exact candidate commit supplied externally after commit creation:

```bash
git diff --full-index --find-renames \
  9edc8bb12f39e49f92bb594d265384de143ea849..<exact-candidate-sha> -- docs_v2
```

Before commit creation the equivalent complete working comparison is:

```bash
git diff --full-index --find-renames \
  9edc8bb12f39e49f92bb594d265384de143ea849 -- docs_v2
```

No generated patch copy is embedded in `docs_v2`: that would duplicate the corpus and immediately
become stale/self-referential. The exact candidate SHA, diff hash/stat and remote comparison are
reported outside the candidate after commit/push. `.DS_Store` is unrelated, untracked and excluded.

## 12. Prompt 2/6 handoff

Prompt 2 must use these verified inputs after this report's validation table is finalized:

1. component/interface basis: PASS13 `COMPONENT_CATALOG.md`, `DOMAIN_INTERFACE_CATALOG.md`,
   ownership and event/command matrices;
2. corrected diagrams: F2 five-map atlas and maintained `ARCH-MAP-001..013`;
3. functional boundaries: ordered ingress owns sequence; domain reducers own state; workers propose;
   Transport performs effects; actual events return through ordered reducers;
4. Risk sequence: preliminary eligibility → supported Sizing/Allocation → full authorization →
   atomic Reservations → immutable plan → pre-send revalidation;
5. open inputs that Prompt 2 must not invent: ingress tie policy, route selection policy,
   boolean/action mapping, `RiskReservation` fields, Accounting record schema and calibrated
   runtime constants;
6. safety cases requiring deeper functional coverage: invalid/unknown input, stale version,
   reconnect, shared liquidity/capital, disk/P0 loss, `UNKNOWN`, partial fill and non-trade balance;
7. scientific/operational boundary: Simulator/Research/Validation evidence never directly mutates
   Live state or grants permission;
8. status ceiling: `DOCUMENTED — IMPLEMENTATION NOT VERIFIED`; no runtime test, approval,
   capability activation or capital authority may be inferred.

Prompt 2 must inspect the owning source files rather than treating this analysis report as a new
semantic authority.
