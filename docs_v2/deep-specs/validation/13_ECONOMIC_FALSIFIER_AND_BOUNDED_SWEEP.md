# 13 — Economic Falsifier and Bounded Falsifier Sweep

`DOCUMENTATION STATUS: F2 PART 1 / INTERMEDIATE DOCUMENTARY WORK / AWAITING HUMAN REVIEW`

This specification defines a documentation-only scientific validation method. It implements no
application code, exchange connection, order, signer, worker, database or dashboard. It grants no
implementation, Shadow, Micro-live, Live, capital, promotion or switchover authority.

## 1. Purpose and scientific question

The Hyperliquid Arbitrage Falsifier asks:

> Does a same-venue Hyperliquid spot arbitrage structure possess a genuinely executable economic
> edge after realistic fees, observed depth, precision, latency, partial fills, failed legs,
> exposure, inventory and Recovery?

Its bounded secondary question is:

> Within a predeclared defensible parameter space, where does that edge survive robustly?

The Falsifier is designed to reject unsupported claims early. Historical positive PnL, one winning
point or a favorable simulation path is never proof of future profitability. A surviving result is
only a candidate for the next existing evidence review.

## 2. Authority and non-authority

The Falsifier owns the experiment protocol, tier progression, pre-registration, bounded evaluation
matrix, robustness summary and diagnostic disposition. It does not own any of the truths it tests.

| Subject | Canonical owner consumed by the Falsifier | Falsifier boundary |
|---|---|---|
| Directed conversions, route structures and fair OWA comparator | [Market Graph and Routes](../../03_MARKET_GRAPH_AND_ROUTES.md) | reference only; no route enum or classification inference |
| QF-001–QF-110, `NetConvert`, economics and units | [Formula Book](../../04_FORMULA_BOOK.md) | execute/reference exact version; no competing formula |
| Market features and honest snapshot-derived proxies | [Market Microstructure](../../05_MARKET_MICROSTRUCTURE.md) | consume versioned inputs; no invented event-level truth |
| Survival, maker and response forecasts | [Participants](../../06_MARKET_PARTICIPANTS.md) | optional supported inputs; no participant identity claim |
| Counterfactual mechanics and `Pi_exec(q,state)` | [Counterfactual Simulator](../../07_COUNTERFACTUAL_SIMULATOR.md) | request declared scenarios; no second Simulator |
| Inventory, capital intent, accounting and `Q_validated` | [Inventory and Capital](../../08_INVENTORY_AND_CAPITAL.md) | report consequences; no capacity or ledger authority |
| Safe action set and hard gates | [Risk Constitution](../../09_RISK_CONSTITUTION.md) | cannot tune, waive or authorize |
| Orders, fills, partials, UNKNOWN, Recovery and Reconciliation | [Execution State Machine](../../10_EXECUTION_STATE_MACHINE.md) | reuse semantics; no sixth state machine |
| IDs, versions, lineage and point-in-time truth | [Data Contracts](../../11_DATA_CONTRACTS.md) | link existing identities; do not expand frozen manifests ad hoc |
| RAW, Replay, deterministic order and evidence quality | [Recorder and Replay](../../12_RECORDER_AND_REPLAY.md) | consume admissible evidence; never repair RAW |
| Evidence sufficiency and maturity | [Validation Matrix](../../16_VALIDATION_MATRIX.md) | Falsifier is subordinate; no promotion authority |
| Implementation and evidence sequencing | [Roadmaps](../../17_IMPLEMENTATION_ROADMAP.md), [evidence journey](../../19_BUILD_VALIDATE_SCALE_ROADMAP.md) | Prompt 1 changes no phase or evidence-stage definition |
| Future generalized research/search | [Strategy Research](../strategy-research/README.md) | remains deferred and inactive |

The exact authority order is Formula/Risk/Execution/Data masters and their deep specs, then
Simulator/Recorder/Validation, then this protocol. If a Falsifier result conflicts with canonical
state or an owning contract, the result is invalid; it cannot redefine the owner.

## 3. Mandatory audit disposition

The requirement audit uses these exact labels:

- `EXACT_REUSE`: the existing contract is used unchanged;
- `CROSS_LINK_ONLY`: this specification only makes the owner easier to find;
- `NEW_REQUIREMENT`: a genuinely new documentary experiment/report contract;
- `SEMANTIC_CHANGE`: would alter an existing owner and is forbidden in Prompt 1;
- `CONFLICT`: incompatible requirements; none is accepted silently;
- `HUMAN_DECISION_REQUIRED`: a calibrated/policy choice cannot be invented;
- `DEFERRED`: explicitly owned by a later controlled prompt or capability gate.

| Requirement family | Disposition | Existing authority / treatment |
|---|---|---|
| Same-venue Hyperliquid spot; Direct/Route2/Cycle3 structures | `EXACT_REUSE` | Graph V1 scope and structures |
| OWA, Triangle, Bridge, Recovery, Rebalance boundaries | `EXACT_REUSE` | Graph plus Inventory/Capital and Accounting |
| TT first, separately gated TTT, later MT/MTT, disabled TM/MM | `EXACT_REUSE` | Execution and canonical roadmaps |
| Exact L2, fees, precision, rounding, minima and sequential output | `EXACT_REUSE` | QF-007–QF-027 |
| Partial/zero/full, UNKNOWN, cancel race, actual-output propagation | `EXACT_REUSE` | Execution deep specs |
| Deterministic Replay, no lookahead and immutable RAW | `EXACT_REUSE` | Data and Recorder/Replay |
| F/P/R/X distribution, tails and exact-once costs | `EXACT_REUSE` | Simulator plus QF-056–QF-063 and dependency audit |
| `ValidatedQSet` holes and scalar `Q_validated` supremum | `EXACT_REUSE` | QF-076 and Validation |
| `FALSIFIER_T0`, `FALSIFIER_T1`, `FALSIFIER_T2` | `NEW_REQUIREMENT` | namespaced validation tiers; not Simulator fidelity or Risk checkpoints |
| Bounded Falsifier Sweep | `NEW_REQUIREMENT` | restricted validation protocol, not generalized Parameter Search |
| Robustness Map / Candidate Region | `NEW_REQUIREMENT` | diagnostic evidence artifact; no capability or strategy status |
| Five Falsifier documentary contract outlines | `NEW_REQUIREMENT` | linked artifacts using existing identities |
| Universal robustness, sample or GO threshold | `HUMAN_DECISION_REQUIRED` | method is specified; numeric values remain calibrated and predeclared |
| Final serialized fields/enums/storage | `HUMAN_DECISION_REQUIRED` | Data/Validation integration review required before implementation |
| Formula, Risk, ESM, accounting or roadmap redefinition | `SEMANTIC_CHANGE` | prohibited; Prompt 1 records no such change |
| Future generalized Parameter Search or Strategy Discovery activation | `DEFERRED` | Prompt 2; baseline gate unchanged |
| Roadmap/authority/HDC/final-review reconciliation | `DEFERRED` | Prompt 3 |
| External Hyperliquid fee/API/feed/order facts | `DEFERRED` | dated primary-source revalidation before any consuming implementation |

No accepted `CONFLICT` was found. The apparent overlap with future Parameter Search is resolved by
the scope boundary in section 8. The apparent overlap with Simulator `F0–F4` and Risk `T0–T5` is
resolved by always storing and displaying the fully qualified `FALSIFIER_T*` names.

## 4. Scope and fixed initial baseline

Initial falsification scope is intentionally narrow:

- Hyperliquid spot on one venue;
- `DirectRoute` as a valid comparator/reference when applicable;
- OWA using `Route2Leg` only when the fair direct comparator exists;
- Triangle using a closed `Cycle3Leg`;
- protected taker execution as the first operational validation path;
- TT first, then TTT only through its own evidence gates;
- MT and MTT retained as later, independently validated capabilities;
- TM/MM future and disabled;
- Bridge distinct, later and outside initial strategy falsification.

Cross-exchange execution, perpetual hedging, adaptive strategy invention, participant intelligence,
advanced maker queue optimization and a distributed Research Factory are outside this initial
capability. Their absence does not weaken the validity of a narrow negative finding.

## 5. Orthogonal economic taxonomy

Every experiment freezes all four axes independently:

| Axis | Required value |
|---|---|
| Structural route | `DirectRoute`, `Route2Leg` or `Cycle3Leg` |
| Economic classification | OWA, Triangle, Bridge, Recovery or Rebalance as applicable |
| Execution mode | TT, TTT, MT, MTT or a later separately permitted mode |
| Accounting/capital intent | Strategy, Bridge, Recovery, Rebalance, Inventory or Infrastructure |

`A -> X -> B` is OWA only when compared fairly against executable `A -> B` for matching starting
quantity, terminal asset, information set, deadline and Risk scope. A missing direct comparator
invalidates OWA classification; it does not by itself create Bridge. Bridge requires intentional
capital relocation for expected future utility. Rebalance remains a separate accounting intent.

## 6. End-to-end architecture

```text
INPUTS                 VALIDATION LAYER                     OUTPUT
------                 ----------------                     ------
Route structure  --->  HYP-* fixed hypothesis
Economic class   --->  EXP-* frozen protocol
Dataset/versions --->  Data admissibility gate
                              |
                              v
                    +---------------------+
                    | FALSIFIER_T0        |--invalid------> STOP / diagnostic
                    | math + economics    |
                    +----------+----------+
                               |
                               v
                    +---------------------+
                    | FALSIFIER_T1        |--unsupported--> INCONCLUSIVE
                    | execution realism   |
                    +----------+----------+
                               |
                               v
                    +---------------------+
                    | BOUNDED SWEEP       |--no region----> NO_ROBUST_REGION
                    | candidate regions   |
                    +----------+----------+
                               |
                               v
                    +---------------------+
                    | FALSIFIER_T2        |--fragile------> ADVERSARIAL_FRAGILE
                    | predeclared attacks |
                    +----------+----------+
                               |
                Validation / walk-forward / final holdout
                               |
                               v
                    FalsifierDispositionReport
                    (evidence, never authorization)
```

Contract — **In:** fixed structure/class/mode/intent and versioned evidence. **Does:** applies
admissibility, the three namespaced tiers, bounded region analysis and temporal confirmation.
**Out:** diagnostic evidence and a scientific disposition. **Truth owners:** Graph, Formula,
Simulator, Execution, Data and Validation. **Stop:** invalid math/data, unavailable T1 mechanics or
failed predeclared criteria. **Available:** T0 after Formula/Data/Replay dependencies; full T1/T2
only when their existing technical dependencies are evidenced. No tier grants runtime permission.

## 7. Falsifier tiers

### 7.1 `FALSIFIER_T0` — Economic and mathematical sanity

T0 evaluates:

- canonical QF-016 `NetConvert` and route formulas;
- correct bid/ask direction;
- full executable observed L2 depth for the tested quantity;
- point-in-time account/market/role/time fee state and fee-debit assets;
- precision, rounding, minimum-trade and quantity constraints;
- fair OWA comparator;
- quantity-specific route feasibility and sequential output;
- correct cycle/conversion accounting;
- no lookahead and exact-once cost ownership.

T0 rejects stale/unknown/invalid inputs rather than coercing them to zero. It may establish that a
claim is structurally invalid or has no edge under observed-book economics. It cannot establish
that the route would have completed at those prices.

### 7.2 `FALSIFIER_T1` — Mechanical execution realism

T1 consumes the canonical Replay, Simulator and execution semantics to evaluate:

- the order book and information actually available at decision time;
- decision-to-arrival timing and arrival-book state;
- sequential TT/TTT execution;
- IOC zero, partial and full outcomes;
- actual available quantity after each simulated fill;
- intermediate exposure and later-leg failure;
- reservations, account/capital and inventory constraints;
- Recovery paths, costs, tails and residual exposure;
- execution uncertainty and limits of evidential support.

T1 is the principal mechanical economic test. It is not a second ESM and does not claim actual
exchange fills. It cannot become fully available before deterministic Replay, Account/Inventory,
Reservations, Risk, ESM, Recovery/Reconciliation, Sizing and the applicable Simulator fidelity
exist at the evidence level required by their owners.

### 7.3 `FALSIFIER_T2` — Adversarial falsification

T2 applies predeclared plausible adverse scenarios without retuning the candidate:

- higher latency and unfavorable latency tails;
- book deterioration, stale/unavailable information and missing-data sensitivity;
- partial/zero fills and second/third-leg failure;
- adverse market movement and recovery-tail outcomes;
- constrained inventory liquidation;
- regime change;
- when maker is separately eligible, pessimistic and calibrated queue/fill scenarios.

T2 tries to invalidate an already frozen candidate region. Observed events, modeled scenarios and
unidentifiable counterfactuals are reported separately. T2 cannot optimize scenario severity or
candidate parameters to produce survival.

## 8. Bounded Falsifier Sweep

The Bounded Falsifier Sweep is a restricted validation method for one already-declared economic
hypothesis and fixed strategy family. It exists to determine whether neighboring admissible
configurations show stable behavior. It is not the future generalized `Parameter Search`.

| Boundary | Bounded Falsifier Sweep | Future Parameter Search |
|---|---|---|
| Owner/status | Validation protocol in this spec; documentary only | deferred Strategy Research; inactive |
| Input | one fixed `HYP-*`, route/economic class and fixed family | versioned `StrategySpec` candidates |
| Purpose | falsify and map a narrow declared claim | compare broader bounded strategy versions |
| Dimensions | small predeclared validation axes | governed parameter schema and later search methods |
| Method | bounded grid/enumeration or declared deterministic policy | manual/grid/random/LHS/Bayesian/evolutionary progression |
| Output | Robustness Map / Candidate Region | candidate strategy set and search report |
| Authority | none; diagnostic only | none directly; later OOS/Shadow/Micro-live gates |
| Activation | only as dependencies become available | forbidden before complete baseline gate |

The Sweep also differs from QF-077 Sizing Search. QF-077 selects a feasible audited q for an
eligible opportunity. The Sweep evaluates a frozen hypothesis over multiple candidate q and other
declared dimensions to test robustness. It does not select live size and cannot raise
`Q_validated`.

### 8.1 Frozen pre-registration

Before any run, freeze:

1. hypothesis, causal/economic rationale and explicit falsification criteria;
2. structure, economic classification, execution mode and accounting intent;
3. target routes/markets and supported/unsupported scope;
4. dimensions, types, units, defensible domains and exact candidate generation policy;
5. locked Formula/Risk/exchange-truth/safety constants;
6. discovery, validation and final untouched holdout `DatasetId`s/intervals;
7. objective vector, guardrails and exact-once cost map;
8. trial/evaluation budget, resolution and deterministic/adaptive policy;
9. RNG seed/stream policy where stochastic;
10. invalid, unsupported, failed, duplicate and censored-run policy;
11. stopping rule;
12. neighborhood and robustness methodology;
13. multiple-testing family and limits on inference;
14. predeclared T2 scenarios;
15. final-holdout access policy and one-evaluation decision family.

Any material change creates a new immutable `EXP-*` version and may require a new untouched
evaluation period. It never overwrites the prior attempt.

### 8.2 Permitted, locked and scenario axes

| Class | Initial examples | Rule |
|---|---|---|
| Candidate dimension | candidate q values; minimum required economic edge; predeclared eligible route/market subset; defensible strategy filter; depth participation; optional stricter strategy data-age filter | may vary only inside declared defensible support |
| Locked truth/safety | QF semantics; exchange fees/precision/metadata; Risk limits; kill switches; reconciliation; ActualFill; UNKNOWN/reservations; Recovery safety; mandatory freshness; capital/authorization; `Q_validated`; execution-mode gate | cannot be optimized or weakened |
| Environment/scenario | latency; degraded liquidity; fill uncertainty; failure severity; missingness; regime | stress axis, never represented as controllable strategy magic |

Optional stricter strategy-specific data-age filtering may reduce the eligible population. It may
not weaken the canonical freshness gate.

### 8.3 Sweep pipeline

```text
FROZEN INPUTS
HYP-* + EXP-* + DatasetIds + versions + q grid + edge grid + scenarios
                              |
                              v
                    deterministic job plan
                    (complete Cartesian subset or
                     predeclared bounded policy)
                              |
             +----------------+----------------+
             |                |                |
             v                v                v
        Eval job 001     Eval job 002     Eval job ...N
        exact config     exact config     exact config
             |                |                |
             v                v                v
          RunId(s)          RunId(s)          RunId(s)
        valid/invalid/     failed/censored/  duplicate retained
        unsupported        negative retained with lineage
             +----------------+----------------+
                              |
                              v
                   immutable run population
                              |
                              v
             robustness surfaces + candidate regions
                              |
                              v
                    EvidenceId + disposition
```

Contract — **In:** frozen experiment and bounded job plan. **Does:** evaluates every planned point
through canonical mechanics and retains every outcome. **Out:** complete run population and
robustness surfaces. **Truth owners:** Data IDs, Replay, Simulator and Formula. **Stop:** budget
exhaustion, invalid lineage, unreproducible result or predeclared stopping rule. **Available:** only
for tiers whose dependencies are present; absent jobs are missing evidence, never favorable cells.

### 8.4 Illustrative q × edge-threshold grid

```text
ILLUSTRATIVE / NOT REAL RESULTS / NO VALIDATED q

minimum required edge (bps)
              3       5       7       9
q =  10      [P]     [P]     [F]     [F]
q =  25      [P]     [P]     [P]     [F]
q =  50      [F]     [P]     [P]     [F]
q = 100      [I]     [I]     [F]     [F]

P = illustrative passing cell under the declared metric vector
F = illustrative failing cell
I = invalid/unsupported; never converted to failure or pass
```

Contract — **In:** discrete candidate q and edge thresholds. **Does:** visualizes evaluated cells
without interpolation. **Out:** a descriptive surface only. **Truth owner:** individual immutable
run results. **Stop:** missing/invalid cells prevent a continuous-region claim. **Available:** after
the applicable tier; the symbols above are pedagogical and contain no market, profit or capacity
evidence.

Candidate simulation q values are experimental inputs, not `ValidatedQSet` membership. The grid
must preserve holes. Neither a pass at 100 nor `Q_validated = 100` implies 10–99 are valid.

## 9. Sequential taker and maker mechanics

### 9.1 Protected taker TT/TTT

```text
Observed state -> arrival timing -> protected IOC LEG 1
                                      |
                     +----------------+----------------+
                     |                |                |
                  zero fill       partial fill      full fill
                     |                |                |
                   abort       actual output q1    actual output q1
                                    |                |
                                    +-------+--------+
                                            |
                          Inventory + reservations updated
                                            |
                          fresh book / economics / Risk
                                            |
                          continue LEG 2 or Recovery
                                            |
                    TT terminal <-----------+----------> TTT LEG 3
                                            |
                               reconcile residual exposure
```

Contract — **In:** decision-time state, arrival assumptions, protected intent and canonical plan.
**Does:** branches on simulated zero/partial/full outcomes and propagates only actual simulated
available quantized output. **Out:** complete TT/TTT path, exposure and Recovery evidence. **Truth
owners:** Simulator for counterfactual outcome; ESM/Inventory/Recovery semantics. **Stop:** stale or
unknown state, infeasible later leg, exhausted protection or unresolved exposure. **Available:**
TT after F1/T1 dependencies; TTT only after its own route and Recovery gates. No simulated fill is
an actual fill.

### 9.2 Later maker path

```text
Maker eligible? --no--> STOP (mode not available)
       |
      yes
       v
ALO intent -> RESTING -> reassess edge / Risk / age / queue uncertainty
       |                         |
       |                         +-- no longer permitted --> CANCEL_REQUESTED
       |                                                   |
       |                            +----------------------+
       |                            | cancel race: fill may still arrive
       v                            v
 zero fill / expiry       partial fill                full fill
       |                       |                          |
  reconciled cancel      real exposure now          real exposure now
                               |                          |
                         actual quantized output --------+
                               |
                   remaining-leg decision / Recovery
```

Contract — **In:** separately eligible maker mode, queue observability and current state. **Does:**
represents wait, zero/partial/full fill and cancel race without assuming a touched price is a fill.
**Out:** attempt-level and conditional-on-fill evidence. **Truth owners:** ESM for lifecycle,
Simulator/Participants for supported forecasts. **Stop:** missing maker gate, optimistic-only
viability, stale feed, UNKNOWN or unsupported queue. **Available:** only after maker evidence and
MT/MTT-specific gates; it is not an initial T1 dependency.

## 10. Evidence provenance and no-lookahead

```text
L0 immutable RAW
  |  checksum + recorder_seq + local receive clocks + gap/quality
  v
L1 normalized events --invalid/unknown--> quarantine / inadmissible region
  |
  v
L2 canonical book/account state (single writer, point in time)
  |
  v
canonical Replay + ReplayClock + explicit versions/seed
  |
  v
canonical Simulator (declared mode/fidelity/scenarios)
  |
  v
FalsifierRunRecord -> Robustness Map -> EvidenceId
                          |
                          v
                 human/AI interpretation
                 (cannot overwrite facts)
```

Contract — **In:** checksummed RAW and versioned interpretation. **Does:** reconstructs what was
knowable, then evaluates declared counterfactuals. **Out:** immutable facts, modeled results and
separate interpretation. **Truth owners:** Data and Recorder/Replay; Simulator owns only modeled
outcomes. **Stop:** gaps, ambiguous order, invalid books, unavailable point-in-time fee/metadata,
lookahead or missing seed/version. **Available:** progressively with Recorder, normalization,
Replay and Simulator dependencies; old low-quality snapshots cannot be retroactively repaired.

## 11. Exact-once economic cost ownership

```text
Observed L2 walk ---------> QF-009/010/016 ----+
Exchange fee/rebate ------> QF-014/015/016 ----+--> complete path cashflow
Partial/failure/Recovery --> QF-057/QF-080 -----+
Inventory preference -----> QF-065 -------------+--> QF-063 decision objective
Stranded/exit/idle -------> QF-068/069/105 -----+
Infrastructure cost ------> QF-090/106 ----------> global economic close

PROTECTION BARRIER:
if an effect is already inside path cashflow, it is not subtracted again downstream.
forecast penalties != realized accounting
```

Contract — **In:** disjoint cost/effect records with owner/version. **Does:** traces first canonical
entry and downstream consumption. **Out:** one reconciliable economic result plus component ledger.
**Truth owners:** Formula dependency audit and Accounting authority. **Stop:** ambiguous overlap,
unreconciled side-asset fees, non-exclusive scenarios or double subtraction. **Available:** T0 uses
deterministic ownership; T1/T2 add path distributions. No Falsifier-specific PnL formula is created.

## 12. Failure/rejection funnel

```text
planned observations
   |
   +-- data inadmissible ----------------------> DATA_INSUFFICIENT
   |
   +-- route/comparator/math invalid ----------> STRUCTURAL_INVALID
   |
   +-- T0 valid but no net edge ---------------> ECONOMIC_NO_EDGE
   |
   +-- T1 machinery/support unavailable -------> INCONCLUSIVE
   |
   +-- T1 mechanics destroy edge --------------> MECHANICAL_NO_EDGE
   |
   +-- Sweep has isolated wins only -----------> NO_ROBUST_REGION
   |
   +-- independent validation fails -----------> OOS_FAILURE
   |
   +-- T2 invalidates frozen region -----------> ADVERSARIAL_FRAGILE
   |
   `-- survives declared gates ----------------> ROBUST_CANDIDATE
                                                   |
                                                   `-> later review only
```

Contract — **In:** the complete eligible population, including negative, failed, invalid and
censored observations. **Does:** assigns the narrowest supported diagnostic reason without hiding
earlier failures. **Out:** scientific NO-GO/INCONCLUSIVE/candidate reasoning. **Truth owner:**
Validation. **Stop:** unresolved coverage or incompatible evidence prevents `ROBUST_CANDIDATE`.
**Available:** as each tier completes; every disposition is non-authorizing.

## 13. Experimental sequence

The mandatory sequence is:

1. define `HYP-*` and `EXP-*`, rationale, falsifier and protocol;
2. validate `DataAdmissibilityReport` and `FALSIFIER_T0`;
3. prove the required `FALSIFIER_T1` machinery is available for the claim;
4. pre-register parameter space, budget, selection, robustness and T2 protocols;
5. run bounded Discovery experiments;
6. produce surfaces and candidate regions, retaining all attempts;
7. evaluate independent Validation windows under the frozen walk-forward policy;
8. freeze candidates and run T2 without consulting final holdout;
9. lock every selection, assumption and decision rule;
10. evaluate the untouched final temporal holdout once for the declared decision family;
11. issue a scientific `GO`, `NO-GO` or `INCONCLUSIVE` conclusion plus diagnostic disposition;
12. if warranted, propose a candidate for later authorization review—never direct trading.

`GO` means only that the declared evidence supports forwarding the candidate to the next existing
review. `NO-GO` rejects the declared claim/scope. `INCONCLUSIVE` means the evidence cannot decide.
None is a `RiskDecision`, capability state or authorization.

A failed final holdout is not retuned on that holdout. A material new hypothesis, dimension,
selection rule or dataset policy creates new lineage and requires a new untouched evaluation
period. Purging and embargo are mandatory where labels, episodes, rolling windows or position
horizons overlap.

## 14. Documentary contract outlines

These are M0 outlines, not implemented schemas. They link existing identities and do not add fields
to the frozen `RunManifest`.

### 14.1 `FalsifierExperimentSpec`

Required semantic fields:

- documentary `experiment_id: EXP-*`, immutable version, `hypothesis_ids: HYP-*` and optional
  fixed `strategy_id: STRAT-*` reference;
- scientific question, falsifier, null/alternative claim wording and claim limits;
- structure/economic class/execution mode/accounting intent;
- market/route scope and fair-comparator contract;
- tier target and dependency-availability declaration;
- parameter dimensions/units/domains, locked constants and scenario axes;
- Discovery/Validation/final holdout `DatasetId` references and leakage policy;
- objective vector, guardrails, cost-owner map, run budget and stopping rule;
- seed, invalid/censored/duplicate policy and multiplicity family;
- robustness methodology, T2 protocol and final-holdout access rule;
- author/reviewer, status, hashes, supersession and explicit non-authorization.

### 14.2 `FalsifierRunRecord`

Required semantic fields:

- canonical `RunId`/`RunManifest` reference, `EXP-*`/`HYP-*` linkage and evaluation-cell identity;
- exact resolved configuration and dataset/code/build hashes;
- Formula/Fee/Metadata/Book/Graph/Simulator/model/config/infra versions;
- RunMode, ReplayMode, SimulationMode, fidelity and fully qualified Falsifier tier;
- scenario assumptions, seed/stream where active and decision-time lineage;
- result status, invalid/censored/failure reason and missingness;
- economics, path distribution, exposure/capital time and tail diagnostics;
- immutable artifact hashes and linked `EvidenceId` when packaged;
- provenance class: actual reconciled, replay reconstruction, simulated/counterfactual, model
  prediction, human/AI interpretation or authorized decision.

### 14.3 `DataAdmissibilityReport`

Required semantic fields:

- `DatasetId`, intended experiment/tier/use and point-in-time interval;
- RAW chunk/checksum resolution, source/feed capability profile and subscription/depth context;
- recorder order, clock quality, exchange/local timestamps and sequence guarantees/limitations;
- gaps, reconnects, invalid/low-fidelity regions, missing markets and book reconstruction result;
- historical point-in-time metadata, fee, precision and feature availability;
- lookahead/leakage checks, selection filters, missingness and censoring policy;
- admissible/limited/rejected scopes with machine-readable reasons;
- report version, artifacts, reviewer and `EvidenceId` linkage.

`RobustnessRegion` and `FalsifierDispositionReport` are specified in
[14 — Robust Region and Candidate Lifecycle](14_ROBUST_REGION_AND_CANDIDATE_LIFECYCLE.md).

## 15. Result provenance classes

Every result and claim is labeled as exactly one primary provenance class:

| Class | Meaning | May substitute for actual fill/account truth? |
|---|---|---:|
| Actual reconciled execution fact | unique exchange/account event reconciled through canonical owners | yes, for its exact actual scope |
| Replay reconstruction | same Core over recorded ordered evidence | no |
| Simulated/counterfactual result | declared Simulator branch/scenario | no |
| Model prediction | point-in-time forecast with support/version | no |
| Human/AI interpretation | explanation over immutable facts | no |
| Authorized decision | separate valid DecisionRecord from the owning governance process | only within that record; never created here |

No simulated fill is serialized or described as actual fill truth. A later actual observation does
not rewrite the original prediction; it joins it as new evidence.

## 16. Rate-limit and API-capacity boundary

Experiments preserve exchange request, order and cancel budget semantics, including protected
capacity for exposure management. A strategy opportunity can never consume capacity reserved for
cancel, query, reconciliation or Recovery. Exact current Hyperliquid limits, endpoint behavior,
priority rules and `expiresAfter` semantics require dated primary-source revalidation before any
implementation or experiment that depends on them.

## 17. Prompt 1 stop boundary

This specification does not:

- activate Strategy Research, Parameter Search, Monte Carlo workers or AI discovery;
- create a new technical phase or evidence stage;
- modify QF-001–QF-110, the SI set, Risk, ESM, capital gates or maturity semantics;
- update HDC ledgers, final review decision forms or switchover authorization;
- authorize implementation, Shadow, Micro-live, Live, strategy promotion or capital.

Prompt 2 owns later Strategy Research/Registry/Workers/Dragonfly/Structure Discovery work. Prompt 3
owns roadmap and authority reconciliation, HDC/human review and final F2 integration. Until those
controlled steps occur, these contracts remain intermediate documentary proposals.
