# F2 Architecture Diagram Atlas

`DOCUMENTATION STATUS: PROPOSED F2 NAVIGATION — AWAITING HUMAN REVIEW`

Authority level: L3 pedagogical navigation. These text maps explain existing and proposed
documentary contracts. They are not generated-code diagrams, implementation evidence, capability
activation or capital authorization.

## Map 1 — Global architecture and first-baseline boundary

```text
Hyperliquid market/account facts
              |
              v
Adapters -> immutable RAW -> ordered Canonical Core
              |                    |
              |                    +-> Book / Graph / Fee / NetConvert
              |                    +-> Inventory / Risk / ESM / Recovery / Reconciliation
              v
       deterministic Replay <-> canonical Simulator
              |
              v
  fixed OWA/TT hypothesis -> Falsifier + finite Bounded Sweep
              |
              v
 robustness + temporal validation + frozen T2 + final holdout
              |
              v
      DRAFT Strategy Candidate (documentary only)
              |
              v
 separate gates: Replay -> Shadow -> authorized Micro-live
              |
              v
       bounded validated baseline, if earned
              |
              v
 FUTURE Research Factory -> new hypotheses / Challengers
              |
              +-- never direct to Risk, orders, Live or capital
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

The first DRAFT candidate and its separately gated validation path do not depend on activating the
Factory. Conversely, no scientific result skips a technical dependency or permission gate.

## Map 2 — Functional ownership map

```text
TRUTH / CANONICAL COMPUTATION
FeedAdapter -> Recorder/RAW -> BookEngine -> Graph/Routes -> FeeEngine
                                      \-------> NetConvert <------/
                                                   |
                                                   v
                           Replay <---------- Canonical Core ----------> Simulator
                                                   |
                                                   v
                          Inventory <-> Risk <-> ESM -> Recovery -> Reconciliation

SCIENTIFIC ANALYSIS (NO TRADING AUTHORITY)
fixed Hypothesis -> Falsifier -> finite Sweep -> Robustness Map -> StrategySpec
                         |             |
                         v             v
                    Experiment Manager -> bounded Workers
                              |
                              v
                    immutable Experiment Registry -> Analytics/Dashboard

FUTURE RESEARCH
validated baseline -> Research Factory -> Challenger proposals
                         |
                         +-> optional distributed workers / optional Dragonfly candidate
                         +-> StructureHypothesis -> human Architecture Review

GOVERNANCE BOUNDARY
scientific evidence -> Validation review -> exact-scope human authorization
                     -> runtime readiness AND Risk -> possible effect
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

DragonflyDB, if ever selected, may hold transient research queue/lease/cache/progress state only.
It cannot hold canonical Inventory, ESM, Risk, Recovery, Reconciliation, capital, signer/nonce or
Live configuration truth.

## Map 3 — Temporal experiment map

```text
Fixed hypothesis and decision family
                |
                v
Pre-registration: data, axes, budget, metrics, stops, multiplicity, holdout
                |
                v
T0 mathematical/economic sanity
                |
                v
T1 supported mechanics + finite discovery Sweep
                |
                v
Discovery Region (diagnostic, not permission)
                |
                v
Independent temporal validation / walk-forward / sensitivity
                |
                v
T2 adversarial falsification of the frozen candidate
                |
                v
FINAL UNTOUCHED HOLDOUT — evaluate once; no optimization
                |
                v
Scientific disposition: NO-GO / INCONCLUSIVE / ROBUST_CANDIDATE
                |
                v
Separate documentary and capability review
```

| Required field | Map-3 meaning |
|---|---|
| Inputs | one fixed family, admissible temporal datasets, locked canonical versions, predeclared uncertainty rules |
| Operations | T0, supported T1, finite discovery, independent validation, frozen T2, one-time holdout |
| Outputs | append-only runs, regions, sensitivity/uncertainty, final scientific disposition |
| Canonical owner | Validation/Data; Simulator/Replay own supported mechanics, not disposition permission |
| Dependencies | pre-registration before data-dependent T0; T1 fidelity before T2; all temporal/no-lookahead controls |
| Failure / STOP | protocol changed after seeing results, unsupported T1, overfit, T2 after holdout, holdout reuse/retuning |
| Status | specified methodology; no experiment result or candidate is claimed validated |

`ROBUST_CANDIDATE` is not `SHADOW_CANDIDATE`, M3, a Strategy promotion or capital permission.

## Map 4 — Risks and failure containment

```text
INPUT / TRUTH FAILURES               SCIENTIFIC FAILURES
stale data ----------> invalidate     T0 reject ----------> reject cell/scope
unknown fees --------> fail closed    unsupported T1 -----> no mechanical claim
invalid/unsupported q -> exclude      isolated optimum ----> no robust region
invented depth ------> invalid        overfit/leakage ------> invalidate family
                                      holdout failure ------> NO-GO; no retune

TRADING-SAFETY FAILURES               RESEARCH-INFRA FAILURES
maker partial fill --> actual Inventory + re-Risk
cancel requested ----> still live until terminal fact
UNKNOWN -------------> reservations stay locked + reconcile
worker crash --------> retry/idempotent result or experiment incomplete
registry corruption -> evidence invalid; no promotion
coordinator failure -> local durable truth retained; no production effect
drift/version invalid -> contract/disable/demote; never auto-resume/promote
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

Scientific rejection answers whether a claim survives evidence. Trading safety answers what may
happen to real state. A rejected cell cannot directly cancel an order; a worker success cannot
unlock a reservation.

## Map 5 — Evidence, governance and F2 identity

```text
ACTUAL / REPLAY / SIMULATED EVIDENCE
                  |
                  v
          Immutable Registry
       (provenance explicitly typed)
                  |
                  v
      Validation assesses CURRENT
      earned maturity level M0–M5
                  |
                  v
      Proposed NEXT scoped activity
      M1 Tests / M2 Replay /
      M3 Shadow / M4 Micro-live /
      M5 Live
                  |
                  v
      Check exact prerequisites
      + separate authorization
                  |
            +-----+-----+
            |           |
          DENIED      APPROVED
            |           |
            v           v
           STOP     Execute only
                    authorized scope
                         |
                         v
                    New Evidence
                         |
                         v
                 Validation Review
                         |
                         v
                 Earned Maturity
                         |
                         v
               Next separate gate
              (never automatic)

DOCUMENTATION GOVERNANCE (SEPARATE CHAIN)
historical Final Review Candidate F
                         |
                         v
proposed exact F2 commit selected externally by SHA/tree/branch
                         |
                         v
DocumentationDecision(F2): APPROVE / REQUEST_CHANGES / REJECT
                         |
                         v
separate SwitchoverAuthorization(F2), only if approved
                         |
                         v
future deterministic Commit B -> separate acceptance -> STOP
                         |
                         v
future separate Phase1Authorization(B), if ever granted
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
