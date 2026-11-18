# Architecture Visual Atlas

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

This atlas is the maintained visual entry point for understanding how the system is intended to
work across domain, temporal, failure, evidence and operational boundaries. It supplements the
[Master Architecture](../../00_MASTER_ARCHITECTURE.md) and the owning domain contracts; it never
overrides them.

The diagrams describe documentary contracts. They are not implementation evidence, passed tests,
capability activation, Live permission or capital authorization.

## Atlas authority boundary

This is the sole **maintained cross-domain visual catalog**. It owns stable `ARCH-MAP-*`
identifiers, navigation and current explanatory renderings, but never the underlying domain
semantics. Masters and owning deep contracts remain authoritative. The F2 five-map atlas is a
candidate-specific review snapshot: it may link here for drill-down, but future diagrams are not
duplicated there and changes here do not retroactively certify or rewrite a selected F2 snapshot.

## 1. How to extend this atlas

Future architecture diagrams belong here when they explain a cross-domain flow or provide a
navigation view that is useful beyond one analysis pass.

1. Give each diagram a stable `ARCH-MAP-NNN` identifier and never renumber an existing map.
2. Add it to the catalog before adding the Mermaid source.
3. State its inputs, outputs, owner, dependencies, exceptional paths, authority and status.
4. Link to the owning contract instead of restating or silently changing domain truth.
5. Keep every arrow meaningful: data, event, command, effect, proposal, evidence or permission.
6. Keep optional, Later V1, Future and Research paths visually distinct from current V1.
7. Validate Mermaid syntax before merge when a compiler is available.

If a diagram and an owning contract disagree, the contract wins and the diagram must be corrected.
A semantic change to ownership, ordering, Risk, Execution truth or authorization still requires the
normal architecture and human-review process.

## 2. Map catalog

| Map ID | View | Primary authority | Scope |
|---|---|---|---|
| `ARCH-MAP-001` | Global system | Master Architecture; PASS 13 ownership contracts | Current V1 orientation |
| `ARCH-MAP-002` | Functional domains and state ownership | State and component ownership matrices | Current V1 orientation |
| `ARCH-MAP-003` | C0-C5 temporal architecture | Async concurrency and ordered commit | Current V1 plus isolated Research |
| `ARCH-MAP-004` | Failure propagation and containment | Risk, Recorder, Execution, Recovery/Reconciliation | Current V1 safety behavior |
| `ARCH-MAP-005` | Scientific maturity and operational authorization | Validation, Capability and F2 contracts | Evidence and permission boundary |
| `ARCH-MAP-006` | Book reconnect walkthrough | Data, Book, Graph, Capability and Risk | Operational walkthrough |
| `ARCH-MAP-007` | Graph generation change walkthrough | Graph/Routes and stale-result contracts | Operational walkthrough |
| `ARCH-MAP-008` | Recorder P0 failure walkthrough | Recorder, Risk and Reconciliation | Operational walkthrough |
| `ARCH-MAP-009` | Partial TT execution walkthrough | Execution, Inventory, Reservations and Accounting | Operational walkthrough |
| `ARCH-MAP-010` | Scientific candidate walkthrough | Falsifier, Validation and Capability | Scientific walkthrough |
| `ARCH-MAP-011` | Risk and Execution pipeline | Risk, Sizing, Reservations and Execution | Operational walkthrough |
| `ARCH-MAP-012` | Shared L2 liquidity and atomic capacity | Book, Sizing, Allocation and Reservations | Capacity walkthrough |
| `ARCH-MAP-013` | Favorable Simulator output refused by Risk | Simulator, Risk and Execution | Authorization walkthrough |
| `ARCH-MAP-014` | RAW identity, normalization outcome and ordered evidence | Data, Recorder, Async and Replay | Ingestion/evidence walkthrough |

## 3. `ARCH-MAP-001` — Global system

```mermaid
flowchart TB
    subgraph LIVE["Live run context"]
        EX["Exchange APIs and WebSockets"] -->|observations| AD["Live adapters and Normalizer"]
        AD --> OUT["RAW-linked valid or rejected outcome"]
        OUT -->|admissible typed event| LI["Live ordered ingress"]
        LI --> OC["Live C0 ordered commit"]
        OUT -->|invalid or unknown; no canonical mutation| RJ["Typed rejection evidence"]
        OC -->|market events| BK["Live Book and Metadata"]
        BK -->|immutable snapshots| GR["Graph and Routes"]
        GR -->|eligible routes| OP["Opportunity and Formula"]
        OP -->|candidate| SZ["Sizer and Allocator"]
        SZ -->|proposal| RK["Risk"]
        RK -->|authorized action| RS["Reservations"]
        RS -->|reserved plan| EC["Execution Coordinator"]
        EC -->|OrderIntent| TR["Authorized production Transport"]
        TR -->|ACK status fill timeout observations| AD
        OC -->|unique actual fills| IV["Live Inventory"]
        OC -->|order transitions| EC
        EC -->|unresolved exposure| RC["Recovery and Reconciliation"]
        RC -->|observed truth| OC
        IV -->|unique economic events| AC["Live Accounting"]
    end

    OUT -.->|bounded RAW and outcome enqueue| RE["C4 Recorder"]
    OC -.->|bounded canonical evidence enqueue| RE
    RE -->|chunks checksums gaps| DS["Immutable Dataset and RunManifest"]

    subgraph REPLAY["Independent Replay run context"]
        DS -->|recorded order and ReplayClock| RI["Replay ordered ingress"]
        RI --> ROC["Isolated Replay C0 instance"]
        ROC --> RST["Replay-only Book Account Inventory Risk Execution state"]
        ROC -->|simulated intent only| RTX["ReplayTransport emulator or disabled effects"]
        RTX -->|Replay AccountEvents only| RI
    end

    SH["Shared contracts reducers formulas versions and state transitions"] -.-> OC
    SH -.-> ROC
    DS --> SCI["Offline scientific evidence"]
    SCI --> VG["Validation human review and promotion"]
    VG --> PA["Admitted immutable artifact or configuration version"]
    PA -.->|Live resolves version; no Replay state injection| OC
```

| Field | Meaning |
|---|---|
| Inputs | Exchange market, metadata, account, order and fill observations |
| Outputs | Live canonical/economic state, isolated Replay state, effect intents and durable evidence |
| Owner | Ordered domain reducers; the ordered boundary sequences commits but is not a second writer |
| Dependencies | Data versions, Book readiness, Graph generation, Formula, Risk, Reservations and Capability |
| Exceptional paths | Stale/unknown state stops affected new risk; transport results return as events; Recorder handoff stays bounded; Replay cannot target Live state/Transport |
| Authority | [Master Architecture](../../00_MASTER_ARCHITECTURE.md), [state ownership](../../_analysis/pass13_master_architecture/STATE_OWNERSHIP_MATRIX.md), [command/event ownership](../../_analysis/pass13_master_architecture/EVENT_AND_COMMAND_OWNERSHIP_MATRIX.md) |
| Status | Intended current V1 architecture; implementation not verified |

No adapter, transport callback, Recorder, model or operator command may directly mutate economic
truth owned by another reducer. Live and Replay reuse the same implementation semantics but never
the same mutable Account, Inventory, Reservation, Execution or Risk state.

## 4. `ARCH-MAP-002` — Functional domains and state ownership

```mermaid
flowchart TB
    O["Ordered event boundary"]
    O --> BW["Book writer"]
    O --> AW["Account writer"]
    O --> IW["Inventory writer"]
    O --> RW["Reservation writer"]
    O --> KW["Risk writer"]
    O --> EW["Execution writer"]
    O --> CW["Recovery and Reconciliation writers"]
    O --> TW["Accounting writer"]
    O -.-> RCW["Recorder state writer"]

    BW -->|BookSnapshot| G["Graph and Route writer"]
    G -->|GraphRouteGeneration| C["Formula Opportunity Capital readers"]
    AW -->|AccountSnapshot| RW
    IW -->|InventorySnapshot| KW
    RW -->|ReservationSnapshot| KW
    KW -->|RiskDecision| EW
    EW -->|effect intent| X["Transport effect executor"]
    X -->|observation event| O
    CW -->|reconciled observations| O
    IW -->|unique fills and fees| TW
    RCW -->|chunks manifests quality| EA["Replay Validation and audit readers"]
```

| Field | Meaning |
|---|---|
| Inputs | Ordered observations, bounded capture/health events and immutable versioned snapshots |
| Outputs | One canonical state version per logical owner |
| Owner | Each named domain is sole logical writer for its state family |
| Dependencies | Ordered event boundary, exact versions and authoritative return events |
| Exceptional paths | Stale or contradictory input is rejected, revalidated or fails closed |
| Authority | [Architecture ownership deep spec](03_STATE_OWNERSHIP_EVENTS_COMMANDS_AND_EFFECTS.md), [component ownership](../../_analysis/pass13_master_architecture/COMPONENT_OWNERSHIP_MATRIX.md) |
| Status | Ownership contract documented; implementation not verified |

Accounting consumes unique actual economic events. It does not write Inventory, and Inventory does
not write Accounting records.

## 5. `ARCH-MAP-003` — Temporal architecture and C0-C5 boundaries

```mermaid
flowchart LR
    C3I["C3 external market and account IO"] -->|observations| C0["C0 ordered canonical commit"]
    C0 -->|cheap deterministic work| C1["C1 inline bounded hot path"]
    C0 -->|immutable snapshot and versions| C2["C2 snapshot parallel compute"]
    C2 -->|proposal with versions| C0
    C0 -->|effect intent| C3O["C3 order cancel query executor"]
    C3O -->|normalized result| C0
    C0 -.->|bounded handoff| C4["C4 durability health and maintenance"]
    C4 -->|quality or health event| C0
    C5["C5 offline research"] -->|versioned artifact candidate| VG["Validation and promotion gate"]
    VG -->|reviewed exact scope only| PA["Promoted artifact or configuration admission"]
    PA -.->|read at explicit Live version boundary; no state injection| C0
```

| Field | Meaning |
|---|---|
| Inputs | External observations, immutable snapshots, effect intents and research artifacts |
| Outputs | Ordered commits, bounded proposals, effect results, evidence and reviewed artifacts |
| Owner | C0 domain owners commit; C1-C5 do not create independent economic truth |
| Dependencies | Bounded queues, version checks, deadlines, stale-result rejection and explicit promotion |
| Exceptional paths | First-worker-wins, direct worker mutation, research-to-order and indefinite disk/network waits are forbidden |
| Authority | [Async Concurrency and Ordered Commit](14_ASYNC_CONCURRENCY_AND_ORDERED_COMMIT.md), [async system map](../../_analysis/async_concurrency_architecture/ASYNC_SYSTEM_MAP.md) |
| Status | Responsibility classes specified; runtime scheduling and capacity remain implementation/calibration work |

The governing rule is: **parallel to calculate, ordered to decide, single-writer to commit**.

## 6. `ARCH-MAP-004` — Failure propagation and containment

```mermaid
flowchart TB
    F["Gap stale data transport timeout or durability failure"]
    F --> Q{"Failure class"}
    Q -->|market data| BNR["Book not ready"]
    BNR --> RI["Dependent routes ineligible"]
    RI --> RSK["Risk blocks new affected exposure"]

    Q -->|P0 durability| P0["Durability condition false"]
    P0 --> RSK

    Q -->|possibly transmitted order| UNK["Order UNKNOWN"]
    UNK --> HOLD["Retain reservations"]
    HOLD --> REC["Query and reconcile"]
    REC --> OBS{"Observed exchange truth"}
    OBS -->|fill| ACT["Commit fill inventory and accounting"]
    OBS -->|terminal no fill| REL["Release reservation"]
    OBS -->|still unknown| STOP["Remain stopped and explicit"]

    Q -->|stale worker result| REJ["Reject incompatible proposal"]
```

| Field | Meaning |
|---|---|
| Inputs | Data gaps, stale versions, durability loss, timeouts and worker completions |
| Outputs | Scoped non-readiness, blocked new risk, retained reservations, reconciliation or explicit unresolved state |
| Owner | Data/Book for readiness, Risk for permission, Execution for order lifecycle, Reconciliation for observed truth |
| Dependencies | Current state versions, unique fills, P0 evidence and recoverable query paths |
| Exceptional paths | Stopping new risk never suppresses an already observed fill or disables safe Recovery/Reconciliation |
| Authority | [Failure containment](11_FAILURE_CONTAINMENT_AND_DEGRADATION_ARCHITECTURE.md), [Risk](../../09_RISK_CONSTITUTION.md), [Execution](../../10_EXECUTION_STATE_MACHINE.md) |
| Status | Safety behavior specified; implementation and fault-injection evidence absent |

## 7. `ARCH-MAP-005` — Scientific maturity and operational authorization

```mermaid
flowchart LR
    H["Frozen hypothesis"] --> T01["T0 and T1"]
    T01 --> SW["Bounded sweep"]
    SW --> VW["Validation and walk forward"]
    VW --> T2["Frozen adverse T2"]
    T2 --> HO["Untouched final holdout"]
    HO --> SC["Scientific candidate"]

    SC --> TV["Technical validation"]
    TV --> HM["Exact scope human approval"]
    HM --> CM["Signed CapabilityManifest"]

    SUP["Compiled support and configuration"] --> INT{"Authority intersection"}
    LIC["Release and license scope"] --> INT
    CM --> INT
    RDY["Current readiness"] --> INT
    RSK["Current RiskDecision"] --> INT

    INT -->|all satisfied| ORD["Execution may accept intent"]
    SC -.->|never directly authorizes| ORD
```

| Field | Meaning |
|---|---|
| Inputs | Frozen hypothesis, point-in-time evidence, technical evidence, manifest and current runtime state |
| Outputs | Scientific disposition, exact-scope capability evidence, or runtime ineligibility |
| Owner | Validation owns evidence; human authority owns approval; Capability owns manifest; Risk owns current permission |
| Dependencies | No-lookahead protocol, maturity evidence, support/config/license/readiness and current Risk |
| Exceptional paths | Scientific success cannot directly create an order, validated q, capital permission or Live promotion |
| Authority | [RunModes and capability](09_RUNMODES_CAPABILITY_ACTIVATION_AND_VALIDATION.md), [Build/Validate/Scale](../../19_BUILD_VALIDATE_SCALE_ROADMAP.md), [F2 lifecycle](../validation/14_ROBUST_REGION_AND_CANDIDATE_LIFECYCLE.md) |
| Status | F2 scientific path proposed; approval, implementation and capital remain separate |

## 8. `ARCH-MAP-006` — Book reconnect walkthrough

```mermaid
sequenceDiagram
    participant WS as WebSocket
    participant AD as Adapter
    participant OC as Ordered Commit
    participant BK as Book
    participant GR as Graph Routes
    participant CP as Capability Risk

    WS-->>AD: connection closes
    AD->>OC: connection lost event
    OC->>BK: mark source unusable
    BK->>GR: BookState not ready
    GR->>CP: dependent routes ineligible
    Note over CP: Existing exposure remains known

    WS-->>AD: connection restored
    AD->>WS: resubscribe
    WS-->>AD: usable source snapshot
    AD->>OC: normalized snapshot event
    OC->>BK: reconstruct and validate
    BK->>GR: fresh consistent BookSnapshot
    GR->>CP: recompute eligibility
    CP->>CP: reassess capability and Risk
    Note over CP: Readiness returns only if every gate passes
```

Ordinary path: a valid snapshot restores the Book before route eligibility and safety gates are
reassessed. Failure path: a connected socket without a usable snapshot remains non-ready.

State owners: Adapter owns connection observations; Book owns `BookState`; Graph owns route
eligibility; Capability and Risk own their respective gates.

Authority: [Data Contracts](../../11_DATA_CONTRACTS.md), [Recorder/Replay](../../12_RECORDER_AND_REPLAY.md),
[Market-to-decision pipeline](05_MARKET_TO_DECISION_PIPELINE.md).

## 9. `ARCH-MAP-007` — Graph generation change walkthrough

```mermaid
sequenceDiagram
    participant MD as Metadata
    participant GB as Graph Builder
    participant GC as Graph Commit
    participant R1 as Existing Reader
    participant WK as Worker
    participant R2 as New Reader

    MD->>GB: metadata version changes
    GB->>GB: build graph routes and reverse indexes
    GB->>GC: complete generation N plus 1
    GC->>GC: validate and publish atomically
    R1->>R1: continue immutable generation N
    R2->>GC: acquire current generation
    GC-->>R2: generation N plus 1
    WK-->>GC: result tagged generation N
    GC-->>WK: reject stale incompatible result
```

Ordinary path: topology, route definitions and reverse indexes become reader-visible as one
compatible immutable generation. Failure path: an incomplete or incompatible build is not
published; readers continue using the previous generation.

State owner: Graph/Route writer only. Workers build proposals and never publish independently.

Authority: [Graph and Routes](../../03_MARKET_GRAPH_AND_ROUTES.md), [route precomputation](../market-graph/04_ROUTE_PRECOMPUTATION_PAIR_TO_ROUTES_AND_INVALIDATION.md),
[stale-result contract](../../_analysis/async_concurrency_architecture/STALE_RESULT_AND_VERSIONING_CONTRACT.md).

## 10. `ARCH-MAP-008` — Recorder P0 failure walkthrough

```mermaid
sequenceDiagram
    participant EX as Execution
    participant RR as Risk Reservations
    participant RC as Recorder
    participant OC as Ordered Commit
    participant IV as Inventory
    participant RE as Reconciliation

    EX->>RR: authorized reserved OrderIntent
    EX-->>RC: bounded P0 evidence enqueue
    RC-->>OC: durability condition failed
    OC->>RR: stop new risk
    Note over OC: C0 does not wait indefinitely for disk

    OC->>IV: commit every received actual fill
    OC->>RR: retain UNKNOWN reservations
    RE->>RE: restart and query exchange truth
    RE->>OC: proven order fill balance observations
    Note over RC,RE: Unavailable evidence remains explicitly missing
```

Specified behavior: Recorder handoff is bounded; failure of required durability stops new risk;
received fills still update actual economic state; UNKNOWN retains reservations; restart uses
reconciliation rather than invented evidence.

Implementation details still requiring design or calibration include acknowledgment semantics,
emergency buffers, flush/fsync policy, deadlines, queue capacity and crash consistency.

Authority: [Recorder/Replay](../../12_RECORDER_AND_REPLAY.md), [Recorder priority matrix](../../_analysis/pass06_data_recorder_replay/RECORDER_PRIORITY_AND_BACKPRESSURE_MATRIX.md),
[Execution/Recovery pipeline](06_EXECUTION_RECOVERY_AND_RECONCILIATION_PIPELINE.md).

## 11. `ARCH-MAP-009` — Partial TT execution walkthrough

```mermaid
sequenceDiagram
    participant PL as Immutable Plan
    participant EX as Execution
    participant IV as Inventory
    participant RS as Reservations
    participant SZ as Sizer Formula
    participant RK as Risk
    participant RC as Recovery
    participant AC as Accounting

    Note over PL: Planned first-leg output is 20 units
    EX->>IV: actual unique fill output is 13.7 units
    IV->>IV: update actual InventoryState
    EX->>RS: adjust consumed and retained reservations
    IV->>SZ: current feasible state uses 13.7 units
    SZ->>RK: continuation proposal with current versions
    RK-->>EX: new RiskDecision
    EX->>EX: create a new immutable continuation plan if allowed
    alt continuation is safe
        EX->>EX: continue next leg
    else continuation is unsafe
        EX->>RC: begin Recovery
    end
    EX->>AC: unique fills fees and action attribution
    RC->>AC: Recovery attribution when used
    AC->>AC: exact-once reconciliation without double count
```

The original plan remains immutable evidence. Actual 13.7-unit state, not planned 20-unit output,
drives the next sizing, Risk and Execution decision. Recovery cannot bypass Risk, and Accounting
cannot fabricate or duplicate exposure.

Authority: [Execution State Machine](../../10_EXECUTION_STATE_MACHINE.md), [Inventory and Capital](../../08_INVENTORY_AND_CAPITAL.md),
[Risk](../../09_RISK_CONSTITUTION.md), [accounting reconciliation](../../_analysis/corr05_economic_integration/ACCOUNTING_RECONCILIATION_MAP.md).

## 12. `ARCH-MAP-010` — Scientific candidate walkthrough

```mermaid
flowchart LR
    H["1 Fixed hypothesis"] --> F["2 Frozen experiment"]
    F --> T01["3 T0 and T1"]
    T01 --> S["4 Bounded sweep"]
    S --> V["5 Validation and walk forward"]
    V --> T2["6 Frozen adverse T2"]
    T2 --> HO["7 Untouched holdout"]
    HO --> C["8 Scientific candidate"]
    C --> TV["9 Separate technical validation"]
    TV --> HA["10 Exact scope human approval"]
    HA --> I["11 Capability readiness and Risk intersection"]
    I --> O["Execution eligibility"]
    C -.->|no direct authority| O
```

Failure at any scientific stage produces a negative, inconclusive or invalid result that remains in
the evidence record. Holdout success does not grant implementation, Shadow, Live, capital or order
permission.

Research/Validation own experiments and candidate evidence; Capability owns the exact manifest;
Risk owns current permission; Execution alone creates `OrderIntent` after every gate is satisfied.

Authority: [Economic Falsifier](../validation/13_ECONOMIC_FALSIFIER_AND_BOUNDED_SWEEP.md), [candidate lifecycle](../validation/14_ROBUST_REGION_AND_CANDIDATE_LIFECYCLE.md),
[Validation Matrix](../../16_VALIDATION_MATRIX.md).

## 13. `ARCH-MAP-011` — Risk and Execution pipeline

```mermaid
flowchart LR
    OP["Opportunity with immutable dependency versions"] --> PE{"Risk preliminary eligibility"}
    PE -->|ineligible or unsupported| RJ["Reject with reason and no reservation"]
    PE -->|safe candidate domain| SZ["Supported Sizing and Allocation"]
    SZ -->|no feasible q| RJ
    SZ -->|bounded q proposal| FR{"Risk full authorization"}
    FR -->|reject expired or recovery-only for new risk| RJ
    FR -->|current bounded action| AR{"Atomic shared-capacity reservation"}
    AR -->|conflict or insufficient capacity| RJ
    AR -->|reservation committed| EP["Immutable ExecutionPlan"]
    EP --> PS{"Pre-send versions readiness action and bounds valid"}
    PS -->|stale expired or incompatible| RL["Do not submit and reconcile or release proven remainder"]
    PS -->|valid| OI["OrderIntent"]
    OI --> TX["Transport external effect"]
    TX -->|ACK reject fill status or timeout| EV["Ordered ExecutionEvent"]
    EV -->|possibly transmitted unresolved| UN["UNKNOWN retain reservations and reconcile"]
    EV -->|proven terminal result| UP["Inventory Execution and Accounting owners update from actual events"]
```

| Field | Meaning |
|---|---|
| Purpose | Show the single Risk authority at preliminary and full checkpoints without treating either checkpoint as a Submit command |
| Inputs | Versioned Opportunity, Book/Graph/Account/Inventory snapshots, supported model outputs and current capability/readiness |
| Outputs | Reject reason, bounded `RiskDecision`, reservation, immutable plan, `OrderIntent` or ordered result event |
| Owner | Risk owns both Risk checkpoints; Sizing proposes q; Reservations own claims; Execution owns plan/order lifecycle; Transport performs effects |
| Decisions / errors | Unsupported model, no feasible q, Risk rejection, reservation conflict, expiry/staleness and `UNKNOWN` all fail closed for new risk |
| Version / freshness | Full authorization and pre-send checks require current compatible versions; an early eligibility check never substitutes for them |
| Authority | [Risk](../../09_RISK_CONSTITUTION.md), [Execution](../../10_EXECUTION_STATE_MACHINE.md), [decision pipeline](../../_analysis/pass13_master_architecture/DECISION_PIPELINE_MAP.md) |
| Related | `ARCH-006`, `ARCH-009`, `ARCH-024`, `ARCH-026`, `ARCH-027`; A-05, A-07, A-16–A-18, A-23 |
| Status | Documentary ordering clarified; exact `allowed`/`action` compatibility and field-level `RiskReservation` schema remain OPEN human/source decisions; implementation not verified |

## 14. `ARCH-MAP-012` — Two routes share L2 liquidity

```mermaid
flowchart TB
    BS["One immutable BookSnapshot generation"] --> R1["Route A candidate walk"]
    BS --> R2["Route B candidate walk"]
    R1 --> D1["Claimed market level slices and asset deltas"]
    R2 --> D2["Claimed market level slices and asset deltas"]
    D1 --> JO["Joint Sizing and Allocation constraints"]
    D2 --> JO
    JO --> OV{"Any overlapping L2 capacity"}
    OV -->|yes| ONCE["Count shared executable liquidity once"]
    OV -->|no| INDEP["Keep proven independent capacity"]
    ONCE --> RS{"Atomic Book Capacity Balance and Risk reservations"}
    INDEP --> RS
    RS -->|both fit current shared state| COM["Commit compatible reservation set"]
    RS -->|conflict state change or insufficient depth| REJ["Reject reduce or recompute before any plan"]
```

Illustrative example: two apparent opportunities reference the same executable book level. Their
standalone quantities may each look feasible, but the common units are available only once. The
Allocator and Reservation owners must compare both against one current shared-capacity state; no
sum of standalone simulations may manufacture extra depth.

| Field | Meaning |
|---|---|
| Purpose | Make A-19 and the no-double-reservation rule visible |
| Inputs | Immutable Book versions, per-route depth dependencies, candidate q and existing reservations |
| Outputs | Compatible atomic reservation set, reduced/recomputed candidates or rejection |
| Owner | Book owns observed depth; Sizing/Allocation owns joint proposal; Reservations own the atomic capacity claim |
| Decisions / errors | Overlap, stale generation, competing claim or insufficient observed depth prevents double use |
| Version / freshness | Every claim carries compatible Book/Graph/route/account/risk versions and is revalidated before effect |
| Authority | [Graph and Routes](../../03_MARKET_GRAPH_AND_ROUTES.md), [Inventory and Capital](../../08_INVENTORY_AND_CAPITAL.md), [Execution](../../10_EXECUTION_STATE_MACHINE.md) |
| Related | `ARCH-009`, `ARCH-014`, `ARCH-018`, `ARCH-023`, `ARCH-027`; A-07, A-18, A-19 |
| Status | Documentary capacity semantics; numerical allocator/search policy and implementation tests remain unverified |

## 15. `ARCH-MAP-013` — Simulator says profitable, Risk refuses

```mermaid
flowchart LR
    C["Supported candidate and current snapshots"] --> SI["Simulator ExecutionForecast"]
    SI -->|illustrative favorable expected outcome| EC["Economic comparison"]
    EC --> RG{"Risk hard gates model support OOD limits readiness"}
    RG -->|any gate fails| NO["REJECT or scoped HALT no reservation no Submit"]
    RG -->|all applicable gates pass| BD["Bounded RiskDecision subject to action size TTL and versions"]
    BD --> RV{"Reservation and pre-send revalidation"}
    RV -->|conflict stale or expired| NO
    RV -->|valid| EX["Execution may accept the bounded intent"]
    SI -.->|forecast is evidence not permission| NOAUTH["No direct authority"]
```

Illustrative example: a forecast can show positive expected economics while a hard inventory
limit, unsupported q band, OOD model state, stale dependency or readiness failure causes Risk to
refuse new exposure. Positive model output is never converted into permission or capital.

| Field | Meaning |
|---|---|
| Purpose | Separate model/economic evidence from Risk sovereignty and effect authorization |
| Inputs | `ExecutionForecast`, economic output, model support/OOD evidence, current snapshots, readiness and capability |
| Outputs | Reject/halt reason or a bounded current `RiskDecision`; never a direct Simulator order |
| Owner | Simulator owns forecast; Formula owns economics; Risk owns permission; Reservations/Execution own later stages |
| Decisions / errors | Unsupported/OOD model, hard-gate failure, stale decision, reservation conflict or pre-send mismatch prevents Submit |
| Version / freshness | Forecast support, q band, state/config/model versions, TTL and pre-send state must remain compatible |
| Authority | [Simulator](../../07_COUNTERFACTUAL_SIMULATOR.md), [Risk](../../09_RISK_CONSTITUTION.md), [model execution risk](../risk/04_MODEL_EXECUTION_AND_TAIL_RISK.md) |
| Related | `ARCH-002`, `ARCH-006`, `ARCH-024`–`ARCH-027`; A-05, A-08, A-11, A-12, A-14, A-23 |
| Status | Documentary refusal path clarified; model calibration, support evidence and implementation remain unverified |

## 16. `ARCH-MAP-014` — RAW identity, normalization outcome and ordered evidence

```mermaid
flowchart TB
    AR["Adapter reception"] -->|copy original bytes and receive metadata| PC["Provisional capture: payload_bytes source connection local clocks"]
    AR -->|bounded work may execute before or overlap ingress| NM["Live normalization attempt"]

    PC --> ARB["Pre-assignment ingress arbitration: exact policy OPEN ARCH-016"]
    ARB -->|one admitted capture event| SQ["Assign recorder_seq once and finalize canonical RawEvent identity"]
    NM -->|valid event or typed invalid/unknown reason| JO["Associate normalization outcome with source_raw_event_id"]
    SQ --> JO

    JO --> OK{"Admissible NormalizedEvent"}
    OK -->|yes| EV["Versioned typed event"]
    EV -->|assigned recorder_seq position| C0["Ordered canonical reducer"]
    C0 --> ST["Canonical domain state"]
    OK -->|no| RJ["Retain RAW plus rejection provenance"]
    RJ -->|forbidden| NO["No Book Account Inventory or permission mutation"]

    SQ -.->|canonical RAW envelope| BH["Bounded evidence handoff"]
    JO -.->|valid or rejected outcome| BH
    BH --> WR["C4 background writer compression checksum"]
    PR["P0-P3 retention and backpressure class"] -.->|storage behavior only; never event order| WR
    WR --> DS["Closed chunks Dataset RunManifest and explicit gaps"]

    SQ -.->|crash before durability| GP["ARCH-019 evidence gap: never claim completeness"]
    GP --> RR["Restart detection Recovery and Reconciliation as applicable"]

    DS -->|ascending recorder_seq within one capture context| RI["ReplayClock and Replay ordered ingress"]
    RI --> RC["Isolated Replay C0"]
    RC --> RS["Replay-owned canonical state and DecisionTrace"]
```

The arrows show required data dependencies and ownership, not a mandatory total physical schedule.
In particular, bounded normalization may run before or overlap ingress; the valid/rejected outcome
becomes usable only after association with the finalized RAW identity. What is fixed is one
`recorder_seq` assignment per admitted capture event, immutable post-assignment order, evidence for
both success and rejection, ordered application of valid events, and background persistence that
cannot create another sequence authority.

| Field | Meaning |
|---|---|
| Purpose | Explain how an invalid or unknown payload remains ordered RAW evidence even though no valid event reaches a reducer |
| Inputs | Original source bytes, source/connection identity, local receive clocks and versioned normalization rules |
| Outputs | Final `RawEvent`, valid `NormalizedEvent` or typed rejection, bounded persistence handoff, Dataset/RunManifest and isolated Replay input |
| Owner | Data owns schema/ordering; ingress assigns `recorder_seq`; domain reducers own state; Recorder owns durability; Replay owns its independent run state |
| Decisions / errors | Exact pre-assignment arbitration and cross-recorder merge remain OPEN; invalid/unknown input cannot mutate state or fabricate a type |
| Version / freshness | Capture context, RAW/normalization schema, source connection, dataset/run manifest and Replay versions remain explicit |
| Exceptional paths | Writer priority/completion never reorders; a crash after assignment creates an explicit gap and invokes the ARCH-019 safety/reconciliation boundary |
| Authority | [Data Contracts](../../11_DATA_CONTRACTS.md), [Recorder/Replay](../../12_RECORDER_AND_REPLAY.md), [Event Ordering](../../_analysis/pass06_data_recorder_replay/EVENT_ORDERING_CONTRACT.md), [Async map](../../_analysis/async_concurrency_architecture/ASYNC_SYSTEM_MAP.md) |
| Related | `ARCH-001`, `ARCH-003`, `ARCH-016`–`ARCH-021`; RAW-ORDER-01–07 and REPLAY-ISO-01–04 |
| Status | Documentary lifecycle specified; acceptance/runtime/durability tests NOT EXECUTED; implementation not verified |

## 17. Known open documentary boundaries

The atlas intentionally preserves these unresolved or review-scoped boundaries rather than drawing
an invented solution:

- the exact `RiskDecision.action` to compatibility-boolean mapping;
- the exact field-level `RiskReservation` schema;
- calibrated Recorder capacities, durability acknowledgment and failure deadlines;
- the ingress source-priority table and cross-recorder merge policy;
- implementation evidence for atomic Graph/Route generation publication;
- explicit Accounting record identity/version in the state-ownership inventory;
- current external exchange semantics, which require dated revalidation at implementation time.

These are inputs to future approved correction or implementation passes, not permissions created by
the diagrams.
