# F2 Architecture Diagram Atlas

`DOCUMENTATION STATUS: PROPOSED F2 NAVIGATION — AWAITING HUMAN REVIEW`

Authority level: L3 pedagogical navigation. These maps explain existing and proposed documentary
contracts. They are not generated-code diagrams, implementation evidence, capability activation or
capital authorization. Function-level and worked operational drill-downs are maintained in the
[Architecture Visual Atlas](../../deep-specs/architecture/15_ARCHITECTURE_VISUAL_ATLAS.md); owning
Masters and deep specs remain authoritative when a diagram is simplified.

### Atlas authority boundary

This file owns only the five-map **F2 review-snapshot presentation** required for the exact F2
candidate. It is corrected here so the snapshot does not preserve misleading arrows, but it is not
the evolving catalog for future diagrams. New cross-domain diagrams and later operational
walkthroughs receive stable `ARCH-MAP-*` identities only in the maintained Architecture Visual
Atlas. Neither atlas owns domain semantics: the named Master/deep contract remains authoritative.
Once an exact corrected F2 snapshot is selected, later atlas evolution does not silently rewrite
that historical review subject; a material change creates a new candidate/delta review.

## Map 1 — Global architecture and first-baseline boundary

```mermaid
flowchart TB
    HL["Hyperliquid market account and metadata interfaces"] -->|observations| AD["Adapters and live Normalizer"]
    AD -->|typed ingress| IN["Ordered ingress and recorder_seq"]
    IN -->|canonical events| C0["Ordered Canonical Core"]
    AD -.->|immutable capture envelope| RAW["L0 RAW capture"]
    C0 -.->|bounded evidence handoff| REC["Recorder C4 background persistence"]
    RAW -.-> REC

    C0 -->|owned reductions| TR["Book Graph Fee Precision Inventory Account"]
    TR -->|versioned snapshots| DEC["Formula Opportunity Sizing Risk Reservations Execution"]
    DEC -->|effect intent| EX["Transport effect executor"]
    EX -->|ACK status fill timeout| C0
    C0 -->|actual fills and observations| RR["Recovery Reconciliation Accounting"]

    REC -->|ordered evidence| RP["Deterministic Replay"]
    RP -->|same isolated Core semantics| C0R["Replay Core context"]
    RP -->|dataset and manifests| FS["Falsifier and finite Bounded Sweep"]
    FS -->|robustness validation T2 holdout| SC["DRAFT scientific candidate"]
    SC -->|separate reviewed gates| VG["Replay Shadow authorized Micro-live validation"]
    VG -->|only if earned| BL["Bounded validated baseline"]
    BL -.->|later activation review| RF["FUTURE Research Factory"]
    RF -.->|proposal and evidence only| FS
```

| Required field | Map-1 meaning |
|---|---|
| Inputs | point-in-time market/account facts, rules, fixed hypothesis, frozen protocol |
| Operations | canonical reduction/economics; Replay/Simulator; falsification; separate capability validation |
| Outputs | immutable evidence, diagnostic region/disposition, possible DRAFT candidate, later bounded baseline |
| Canonical owner | domain Masters for truth; Validation for evidence; human/authorization records for permission |
| Dependencies | phases 1–20 as applicable; M0–M4 evidence; readiness, Risk and exact manifest |
| Failure / STOP | stale/unknown truth, invalid q, leakage, failed holdout, unmet maturity or missing authorization |
| Status | first path specified but unimplemented/unauthorized; Factory future and inactive |
| Related findings / scenarios | ARCH-001–005, ARCH-010, ARCH-018–020; A-03, A-08–A-16, A-24 |
| Drill-down | `ARCH-MAP-001`, `003`, `008`, `010` in the maintained visual atlas |

The first DRAFT candidate and its separately gated validation path do not depend on activating the
Factory. Conversely, no scientific result skips a technical dependency or permission gate.

## Map 2 — Functional ownership map

```mermaid
flowchart TB
    subgraph V1["Current V1 canonical computation"]
        FA["FeedAdapter"] -->|typed observations| OC["Ordered Core"]
        FA -.->|capture evidence| RE["Recorder"]
        OC --> BK["Book Metadata Fee Precision"]
        BK --> GR["Graph Routes and dependency indexes"]
        GR --> FO["Formula Features Opportunity"]
        FO --> PE["Risk preliminary eligibility"]
        PE --> SZ["Inventory Terminal Sizing Allocation"]
        SZ --> FR["Risk full authorization"]
        FR --> RS["Atomic Reservations"]
        RS --> ES["Execution Coordinator"]
        ES -->|effect intent| TP["Transport"]
        TP -->|observed result| OC
        OC --> IR["Inventory Recovery Reconciliation Accounting owners"]
    end

    FO -.->|optional promoted dependency| PA["Participants"]
    PA -.->|optional supported forecast| SI["Simulator"]
    SI -.->|versioned ExecutionForecast| SZ

    subgraph SCI["Scientific analysis with no trading authority"]
        HY["Fixed Hypothesis"] --> FL["Falsifier"]
        FL --> SW["Finite Sweep"]
        SW --> RM["Robustness Map"]
        RM --> SS["StrategySpec candidate"]
        EM["Experiment Manager"] -->|bounded jobs| WK["Scientific workers"]
        WK -->|idempotent evidence| RG["Immutable Experiment Registry"]
    end

    subgraph FUT["Future Research only"]
        RF["Research Factory"] --> CH["Challenger proposals"]
        RF --> DS["Optional distributed workers and cache"]
        RF --> ST["StructureHypothesis"]
        ST --> AR["Human Architecture Review"]
    end

    SS -->|evidence| VA["Validation review"]
    VA -->|exact-scope candidate| HA["Human authorization"]
    HA -->|permission input only| FR
```

| Required field | Map-2 meaning |
|---|---|
| Inputs | exchange facts, immutable snapshots, canonical versions, hypothesis/protocol |
| Operations | truth reconstruction, economics, scenario evaluation, deterministic job execution, indexing/presentation |
| Outputs | canonical state, proposals, reports and evidence links; workers/dashboard never output permission |
| Canonical owner | Adapter/Data/Formula/Execution/Risk owners for facts; Research only for protocols/orchestration |
| Dependencies | each analyzer inherits every canonical engine and evidence dependency it consumes |
| Failure / STOP | invented data/fills, mutable registry, stale worker result, coordinator treated as truth, authority leakage |
| Status | Core contracts canonical; Falsifier/Registry specified; Manager/workers unimplemented; Factory/distribution future |
| Related findings / scenarios | ARCH-002, ARCH-005–008, ARCH-010, ARCH-012, ARCH-023–028; A-01–A-08, A-11–A-14, A-18–A-23 |
| Drill-down | `ARCH-MAP-002`, `009`, `011`, `012`, `013` in the maintained visual atlas |

DragonflyDB, if ever selected, may hold transient research queue/lease/cache/progress state only.
It cannot hold canonical Inventory, ESM, Risk, Recovery, Reconciliation, capital, signer/nonce or
Live configuration truth.

## Map 3 — Temporal runtime and experiment boundaries

```mermaid
flowchart TB
    C3I["C3 external market account IO"] -->|observations| IA["Ingress arbitration"]
    IA -->|assign recorder_seq| C0["C0 ordered canonical commit"]
    C0 -->|bounded deterministic work| C1["C1 inline hot path"]
    C0 -->|immutable snapshot versions deadline| C2["C2 runtime workers"]
    C2 -->|proposal tagged with inputs| VR{"Current version and deadline valid"}
    VR -->|yes deterministic policy| C0
    VR -->|no| DROP["Discard or recompute stale result"]
    C0 -->|effect intent| C3O["C3 order cancel query executor"]
    C3O -->|normalized result event| IA
    C0 -.->|bounded handoff| C4["C4 Recorder durability health maintenance"]
    C4 -->|quality health event| IA

    C5["C5 offline scientific workers"] -->|append-only evidence| PR["Pre-registered T0 T1 Sweep validation T2 holdout"]
    PR -->|scientific disposition only| REV["Separate Validation and human review"]
    REV -.->|reviewed artifact version only| C0
```

| Required field | Map-3 meaning |
|---|---|
| Inputs | concurrent observations; immutable runtime snapshots; pre-registered scientific datasets/protocols |
| Operations | ingress sequencing; ordered commits; bounded runtime proposals; async effects/durability; isolated scientific work |
| Outputs | canonical versions, accepted/rejected proposals, effect observations and append-only scientific evidence |
| Canonical owner | ordered domain reducers for runtime; Validation/Data for scientific evidence; no worker owns economic truth |
| Dependencies | versioned ingress policy, bounded queues/deadlines, current-version revalidation, no-lookahead experiment protocol |
| Failure / STOP | C2 completion order cannot decide; stale results drop; C4 cannot block indefinitely; C5 cannot mutate Live state |
| Status | C0–C5 semantics documented; queue sizes, ingress tie policy and fanout policy require evidence/decision |
| Related findings / scenarios | ARCH-003, ARCH-010, ARCH-011, ARCH-016, ARCH-018–021; A-03, A-07, A-09, A-15–A-17, A-20 |
| Drill-down | `ARCH-MAP-003`, `008`, `010` in the maintained visual atlas |

`ROBUST_CANDIDATE` is not `SHADOW_CANDIDATE`, M3, a Strategy promotion or capital permission.

## Map 4 — Risks and failure containment

```mermaid
flowchart TB
    F["Feed disconnect gap unknown event stale data or invalid rules"] --> SCOPE{"Affected scope proven"}
    SCOPE -->|market known| MK["Invalidate market Book and dependent routes"]
    SCOPE -->|scope unknown| BD["Conservative source or venue containment"]
    SCOPE -->|independent scope proven| KEEP["Independent ready markets may continue"]
    MK --> NR["Block affected new risk"]
    BD --> NR

    TX["Order may have been transmitted"] --> UNK["Execution UNKNOWN"]
    UNK --> LOCK["Retain reservations and known exposure"]
    LOCK --> QR["Query orders fills balances"]
    QR --> RR{"Reconciled truth"}
    RR -->|actual fill| INV["Inventory and Accounting exact-once update"]
    RR -->|terminal no fill| REL["Release proven remainder"]
    RR -->|unresolved| SAFE["Remain stopped and escalate"]

    P0["P0 durability threatened"] --> NR
    P0 --> CONT["Continue fill handling cancel Recovery Reconciliation"]
    SCI["T0 T1 T2 holdout or support failure"] --> NOGO["Reject invalidate or remain inconclusive"]
    NOGO -.->|never trading action| NR
```

| Required field | Map-4 meaning |
|---|---|
| Inputs | data/rules/q, experimental cells, actual order/fill events, worker/registry/coordinator health |
| Operations | fail-closed validation, scope containment, reconciliation, evidence invalidation and safe demotion |
| Outputs | rejected/invalid scientific claim, locked reservation, current exposure, incident/evidence records |
| Canonical owner | Data/Formula/Validation for scientific validity; Execution/Risk/Reconciliation for trading safety |
| Dependencies | exact provenance, current versions, unique fills, bounded jobs, durable evidence and stop rules |
| Failure / STOP | unresolved ownership/account truth broadens STOP; research failure never triggers a trading action |
| Status | failure rules specified; no runtime implementation or passed drill claimed |
| Related findings / scenarios | ARCH-009, ARCH-013–017, ARCH-019–021, ARCH-025–029; A-01, A-05, A-07, A-11, A-15–A-19, A-24 |
| Drill-down | `ARCH-MAP-004`, `006`–`009`, `012`, `013` in the maintained visual atlas |

Scientific rejection answers whether a claim survives evidence. Trading safety answers what may
happen to real state. A rejected cell cannot directly cancel an order; a worker success cannot
unlock a reservation.

## Map 5 — State ownership, evidence and authorization

```mermaid
flowchart TB
    EV["Ordered canonical events"] --> BW["Book writer"]
    EV --> AW["Account writer"]
    EV --> IW["Inventory writer"]
    EV --> RW["Reservation writer"]
    EV --> GW["Graph and Route generation writer"]
    EV --> EW["Execution writer"]
    EV --> CW["Recovery Reconciliation writers"]
    EV --> TW["Accounting writer"]
    EV -.-> RCW["Recorder state writer"]

    BW -->|immutable BookSnapshot| READ["Read-only Formula Opportunity Sizing consumers"]
    GW -->|compatible Graph Route Index generation| READ
    AW -->|AccountSnapshot| READ
    IW -->|InventorySnapshot| READ
    RW -->|ReservationSnapshot| RISK["Risk authority"]
    READ --> RISK
    RISK -->|RiskDecision action and bounds| EW
    EW -->|effect intent| TP["Transport executor"]
    TP -->|external observation| EV
    RCW -->|chunks manifests quality| RP["Replay Validation audit readers"]

    SCI["Scientific and validation evidence"] --> VAL["Validation maturity assessment"]
    VAL -->|exact scope evidence| HUM["Separate human authorization"]
    HUM --> CAP["Signed CapabilityManifest"]
    SUP["Compiled support configuration release license"] --> INT{"Runtime authority intersection"}
    CAP --> INT
    RDY["Current readiness"] --> INT
    RISK --> INT
    INT -->|all valid| EW
    SCI -.->|no direct permission| EW

    DOC["Exact documentation candidate SHA tree branch"] --> DR["DocumentationDecision"]
    DR -->|only if approved| SW["Separate switchover decision"]
    SW -->|future Commit B and acceptance| P1["Separate future Phase 1 decision"]
```

| Required field | Map-5 meaning |
|---|---|
| Inputs | provenance-typed evidence, current earned maturity and a proposed next scoped activity; exact candidate commit/tree/branch in external records |
| Operations | immutable indexing; Validation assesses current earned maturity; exact prerequisites and separate prior authorization are checked for the proposed activity; only the authorized scope executes; new evidence returns to Validation review |
| Outputs | evidence disposition or decision record; never implicit next-gate approval |
| Canonical owner | Data/Registry for evidence lineage; Validation for maturity; named human authority for decisions; Risk at runtime |
| Dependencies | complete exact snapshot, current evidence, applicable SI set, traceability and non-stale prerequisites; exact CapabilityManifest, readiness, Risk and applicable capital/order authorization before any capital/order effect |
| Failure / STOP | mixed evidence classes, moving-HEAD identity, stale certificate, approve-with-changes, failed prerequisite, denied authorization or activity outside the authorized scope |
| Status | proposed F2 review package pending; no documentation approval, switchover, B, Phase 1 or capital authority |
| Related findings / scenarios | ARCH-006, ARCH-012, ARCH-024–029; A-02, A-04, A-05, A-10–A-12, A-18, A-23, A-24 |
| Drill-down | `ARCH-MAP-002`, `005`, `009`, `010`, `011`, `013` in the maintained visual atlas |

Maturity records evidence already earned; authorization permits only a separately reviewed future
scope. The following rules therefore apply:

- M0 is documentation maturity, not execution permission.
- M1/M2 evidence does not automatically authorize Shadow.
- Shadow requires prior authorization; successful evidence may subsequently establish M3.
- Micro-live requires separate prior authorization and applicable capital controls; successful
  evidence may establish M4.
- Live requires its own prior authorization; M5 is earned only from valid scoped Live evidence.
- Every capital/order effect requires the exact CapabilityManifest, readiness, Risk and applicable
  capital/order authorization.
- A failed prerequisite or denied authorization prevents the next risk-increasing activity.
- Existing exposure remains governed by canonical Risk, Recovery and Reconciliation.
- No stage promotes itself or another stage.

The final F2 commit SHA/tree are deliberately absent from its own corpus. A reviewer records them
externally after the commit exists. Any material post-selection change creates another candidate
and restarts exact-snapshot review.

## Specialized map links

- [First baseline and later Challenger lineage](../../deep-specs/strategy-research/03_STRATEGY_SPEC_AND_LINEAGE.md#d1--first-owatt-baseline-path-and-later-challengers)
- [Falsifier end-to-end architecture](../../deep-specs/validation/13_ECONOMIC_FALSIFIER_AND_BOUNDED_SWEEP.md)
- [Robust region lifecycle](../../deep-specs/validation/14_ROBUST_REGION_AND_CANDIDATE_LIFECYCLE.md)
- [Research orchestration and workers](../../deep-specs/strategy-research/11_RESEARCH_ORCHESTRATION_AND_WORKERS.md)
- [Experiment Registry and Analytics](../../deep-specs/strategy-research/09_REPORTING_AND_KNOWLEDGE_BASE.md)
