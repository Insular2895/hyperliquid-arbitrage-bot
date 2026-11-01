# 14 — Robust Region and Candidate Lifecycle

`DOCUMENTATION STATUS: F2 PART 1 / INTERMEDIATE DOCUMENTARY WORK / AWAITING HUMAN REVIEW`

This specification defines how a Bounded Falsifier Sweep is summarized, challenged and disposed.
It contains no real experiment result, validated quantity, profitable market, strategy promotion or
capital authorization.

## 1. Purpose and authority

The primary Discovery Sweep output is a **Discovery Robustness Map / Discovery Candidate Region**,
not the historically best point and not an independently confirmed region. This document owns the
documentary region method and candidate evidence lifecycle. It is subordinate to the same
authorities listed in
[13 — Economic Falsifier and Bounded Sweep](13_ECONOMIC_FALSIFIER_AND_BOUNDED_SWEEP.md): Formula
owns economics, Simulator owns counterfactual distributions, Data/Recorder owns provenance,
Execution/Inventory owns actual truth, Risk owns permission and Validation owns evidence maturity.

A `RobustnessRegion` is a diagnostic evidence artifact. It is not a `StrategySpec`,
`ValidatedCapability`, `CapabilityManifest`, `RiskDecision`, authorization or proof that every
interior q is valid.

## 2. What counts as a candidate region

During Discovery, a candidate region is a predeclared connected or neighborhood-supported set of
**evaluated valid cells** whose complete metric vector remains acceptable under the declared
Discovery method. It is a **DISCOVERY CANDIDATE REGION**: preliminary, exploratory and not
independently validated. Region construction must state:

- dimensions, scales, adjacency/neighborhood relation and distance method;
- which metrics are pass/fail guardrails and which are descriptive;
- minimum evidence/support method and uncertainty treatment;
- how invalid, missing, failed and censored cells affect connectivity;
- how discrete/categorical dimensions are separated;
- boundary handling and whether the region touches a search-domain edge;
- stability tests across period, regime, seed and predeclared scenarios;
- exact rules for merging or splitting regions;
- the rule for choosing zero, one or more frozen candidates from the region.

Independent temporal Validation and walk-forward may support, narrow or reject that preliminary
region under the frozen protocol. Only the surviving exact subset may be described as a
**VALIDATION-SUPPORTED REGION**. That label means independent temporal evidence exists; it does not
mean validated strategy, capability, `ValidatedQSet` membership, `Q_validated` increase or runtime
permission. `DISCOVERY CANDIDATE REGION` and `VALIDATION-SUPPORTED REGION` are documentary lifecycle
labels over the immutable `RobustnessRegion` evidence lineage, not new canonical IDs, runtime enums
or authorization states.

No universal numeric neighbor count, confidence level, sample minimum or robustness score is
invented here. Each value is `CALIBRATED / HUMAN_DECISION_REQUIRED`, predeclared before results,
and justified for the exact claim. Invalid cells are barriers or unknowns according to the frozen
method; they are never silently imputed as passes.

## 3. Candidate region versus isolated optimum

```text
ILLUSTRATIVE / NOT REAL RESULTS

minimum edge threshold  ->
q v        1     2     3     4     5     6     7
  10       .     .     +     +     +     .     .
  25       .     +    [C]    +     +     .     .
  50       .     +     +     +     .     .     *
 100       x     x     .     .     .     .     .

+ = neighboring Discovery-supported illustrative cells
[C] = one preliminary Discovery candidate, not necessarily peak PnL or independently confirmed
* = isolated illustrative historical optimum; fails neighborhood support
x = invalid/unsupported; does not certify or refute adjacent q
. = evaluated illustrative failure or no support as declared by the legend
```

Contract — **In:** complete evaluated grid and predeclared adjacency/support rules. **Does:**
distinguishes stable neighboring support from a sharp isolated optimum. **Out:** zero or more
preliminary Discovery candidate regions plus boundary/coverage warnings. **Truth owner:** immutable
run population; Validation owns the inference. **Stop:** invalid connectivity, unstable neighbors,
boundary attraction or insufficient coverage. **Available:** after the Bounded Discovery Sweep;
the diagram contains no real result, independent confirmation or `Q_validated` claim.

An isolated positive point is a red flag, not a region. A region touching a domain boundary is not
automatically invalid, but the report must state that the optimum may lie outside the declared
domain and must not expand the domain post hoc. Expanding the domain is a new experiment version.

## 4. Temporal separation and one-time final holdout

```text
time -------------------------------------------------------------------------->

[ BOUNDED DISCOVERY SWEEP USING T1 ]
                   |
                   v
      DISCOVERY ROBUSTNESS MAP / CANDIDATE REGION
               (preliminary only)
                   |
        gap/embargo v
[ INDEPENDENT TEMPORAL VALIDATION ]
                   |
                   v
             [ WALK-FORWARD ]
                   |
                   v
        VALIDATION-SUPPORTED REGION
        (non-authorizing evidence)
                   |
                   v
       freeze candidate / T2 protocol
                   |
                   v
      [ T2 PREDECLARED ADVERSE TESTS ]
                   |
                   v
       ADVERSARIALLY TESTED CANDIDATE
                   |
                   v
      lock final selection and decision rules
                   |
        gap/embargo v
         [ FINAL UNTOUCHED HOLDOUT ]
          evaluate once per decision family
                   |
                   v
  ROBUST_CANDIDATE or scoped NO-GO / INCONCLUSIVE

Final holdout cannot flow backward into Discovery, region shape, thresholds or T2 severity.
```

T2 scenarios and severity are predeclared in the frozen experimental protocol before Discovery;
the later freeze step binds the validation-supported candidate to that unchanged protocol. A final
holdout failure cannot trigger retuning or reselection on the same holdout.

Contract — **In:** chronologically ordered Dataset intervals with availability boundaries. **Does:**
separates preliminary exploration, independent confirmation, walk-forward, adversarial testing and
one-time final decision. **Out:** immutable stage-linked region evidence and one final disposition.
**Truth owners:** Data point-in-time lineage and Validation. **Stop:** repeated holdout access,
overlap without purge/embargo, future artifact leakage or post-result rule change. **Available:**
after admissible temporal datasets exist; Shadow and Micro-live remain later distinct gates.

The embargo width is evidence-justified from label/episode/position/rolling-feature overlap. It is
not a universal duration. Every walk-forward fold declares training/calibration/test boundaries,
warm-up, expanding/rolling policy, refit rule and aggregation before results are viewed. Missing or
failed folds remain in the summary.

## 5. Mandatory robustness measurements

Every map/region reports, by cell and appropriate region aggregate:

| Family | Required observations |
|---|---|
| Net economics | complete canonical net PnL/benefit definition, distribution, uncertainty and exact-once cost reconciliation |
| Population | opportunity, eligible, evaluated, attempted/simulated and resolved counts with denominators |
| Completion | zero/full/partial/failure/Recovery distributions and unresolved/censored coverage |
| Recovery | entry rate, incremental QF-080 loss, tails, time and remaining exposure |
| Risk/tails | drawdown, QF-059 positivity, loss quantiles/ES and worst supported slices as applicable |
| Exposure/capital | intermediate exposure duration/value, reservation time, inventory state and capital usage |
| Sensitivity | local q/threshold/filter sensitivity; holes and discontinuities preserved |
| Time/regime | Discovery/Validation/fold/period/regime dispersion and worst supported fold |
| Support | data fidelity, OOD, missingness, clock/order quality and model/Simulator confidence causes |
| Boundaries | attraction to minimum/maximum domain values and unavailable neighbors |
| Failure coverage | failed jobs, invalid/censored/duplicate/manual reruns and reason distribution |

Means alone are insufficient. Reports include counts, quantiles, tails, missing joins and coverage.
Opportunity count cannot be substituted for attempt count, and route completion cannot be
substituted for positive PnL.

## 6. Region construction rules

### 6.1 Cell validity precedes cell score

A cell enters region analysis only when its data, configuration, canonical formulas, lineage and
required tier result are valid. An unsupported cell is `INVALID_OR_UNSUPPORTED`, not a poor score.
This distinction prevents missing evidence from becoming a conservative-looking loss or a hidden
pass. A failed cell refutes only that cell unless sufficient declared-domain coverage or a canonical
scope-wide bound supports a broader conclusion.

### 6.2 Complete objective vector

The region criterion consumes the predeclared vector rather than a single scalar:

- net economics after canonical costs;
- completion/failure/Recovery behavior;
- tail and drawdown guardrails;
- exposure/capital usage;
- support, uncertainty and missingness;
- stability across neighbors and the periods/regimes available at the current evidence stage; T2
  sensitivity is appended only after the candidate and adverse protocol are frozen.

A scalar display score may summarize only if its construction is predeclared, decomposable and
cannot conceal a failed hard guardrail. No scalar may replace Risk.

### 6.3 Neighborhood support

Adjacency is defined in meaningful units. For q and threshold grids it may be orthogonal or include
declared diagonals; for categorical route subsets, categories are separate unless a scientifically
defensible adjacency exists. Unequal grid spacing must be reflected in distance. A parameter value
that changes strategy family, execution mode or hypothesis is not a neighbor; it is a new lineage.

### 6.4 Non-monotonic q

Region summaries retain the exact evaluated q membership. They never display a filled continuous
interval merely because the minimum and maximum q pass. `q <= Q_validated` is not a membership
test, and candidate simulation q cannot create or enlarge `ValidatedQSet`.

### 6.5 Negative controls and boundary tests

Where feasible, include negative controls that should remove the alleged edge, such as direction,
timing or comparator perturbations that remain economically meaningful and predeclared. A failure
to distinguish the hypothesis from its negative control lowers the claim. Boundary tests inspect
rounding/minimum discontinuities, first unsupported depth, threshold edges and missing-data
sensitivity without extending the search after results.

Independent Validation applies the frozen region rule to new temporal evidence. It may support the
Discovery region, narrow it to the exact independently supported subset or reject it; it may not
expand or repair it after seeing results. Any material post-result modification to dimensions,
thresholds, adjacency, selection, exclusions, dataset policy or T2 rules creates new experiment and
region lineage and requires an appropriate new untouched evaluation period.

## 7. Example Bounded Sweep

The following is a method example only.

```text
ILLUSTRATIVE PROTOCOL — NOT AN EXPERIMENT AND NOT REAL RESULTS

Hypothesis:
  HYP-DEMO: a declared same-venue OWA TT family retains positive matched-comparator
  economics under FALSIFIER_T1 for some supported q and edge-threshold neighborhood.

Frozen structure:
  Route2Leg A->X->B versus DirectRoute A->B
  Economic class OWA; execution mode TT; accounting intent Strategy

Candidate axes:
  q = {10, 25, 50, 100} abstract asset units
  minimum edge threshold = {3, 5, 7, 9} illustrative bps

Locked:
  QF semantics, fee/precision/metadata truth, mandatory freshness, Risk/Recovery rules,
  dataset splits, route set, budget, seed policy and cost ownership

Scenario axes (not tuned parameters):
  declared arrival-latency treatments, liquidity deterioration and later-leg failures

Discovery outputs:
  complete 4 x 4 cell population, invalid/missing cells, metric vectors,
  preliminary neighborhood-supported Discovery candidate regions

Later linked evidence (not produced by Discovery itself):
  independent Validation and walk-forward support/narrow/reject results,
  T2 fragility and final untouched holdout disposition
```

The example does not state that any q, threshold, asset, route or region passes. Its purpose is to
show that a Sweep is finite, predeclared and interpretable.

## 8. Candidate lifecycle

```text
Structure + HYP-* -> Data admissibility -> T0 per-cell prefilter
      |
      v
T1 machinery available -> frozen experimental protocol
      |
      v
BOUNDED DISCOVERY SWEEP USING T1
      |
      v
DISCOVERY CANDIDATE REGION
preliminary / exploratory / not independently validated
      |
      v
INDEPENDENT TEMPORAL VALIDATION
      |
      v
WALK-FORWARD
      |
      +---------------------------> OOS_FAILURE / INCONCLUSIVE
      v
VALIDATION-SUPPORTED REGION
independent temporal evidence / still not a validated strategy
      |
      v
FREEZE CANDIDATE / T2 PROTOCOL
      |
      v
FALSIFIER_T2 — PREDECLARED ADVERSARIAL TESTS
      |
      +---------------------------> ADVERSARIAL_FRAGILE
      v
ADVERSARIALLY TESTED CANDIDATE
      |
      v
LOCK FINAL SELECTION AND DECISION RULES
      |
      v
FINAL UNTOUCHED HOLDOUT ONCE
per declared decision family
      |
      +---------------------------> scoped NO-GO / INCONCLUSIVE
      v
ROBUST_CANDIDATE
      |
      v
LATER HUMAN/EVIDENCE REVIEW ONLY (separate owner/process)
```

The lifecycle never creates a Strategy or capability implicitly. A validation-supported region is
still non-authorizing, T2 may invalidate it, and `ROBUST_CANDIDATE` is issued only after all required
declared tests including the one-time untouched final holdout succeed. If a later process creates or
updates `STRAT-*`, that is separate lineage and must reference the immutable Falsifier evidence
without rewriting it. No stage automatically creates a `StrategySpec`, `ValidatedCapability`,
`ValidatedQSet` membership, `Q_validated` capacity or production permission.

## 9. Documentary contract outlines

These outlines are `NEW_REQUIREMENT` at M0. Final serialization, enum placement and storage are
`HUMAN_DECISION_REQUIRED` under Data/Validation authority.

### 9.1 `RobustnessRegion`

Required semantic fields:

- region identity/version and parent `EXP-*`/`HYP-*` references;
- exact included cell/run identities and excluded/invalid/missing cells;
- dimensions, units, domain, grid/policy and adjacency definition;
- dataset split/fold identities, tier, mode/fidelity and support scope;
- complete metric vector, uncertainty method and guardrail outcomes;
- neighborhood, stability, boundary and negative-control evidence;
- regime/period/seed/T2 sensitivity and worst supported slice, with Discovery and linked independent
  Validation/walk-forward evidence separated by lifecycle stage;
- q membership represented as an exact set/list, never inferred interval;
- limitations, unresolved thresholds, candidate selection rationale and artifact hashes;
- `EvidenceId`, author/reviewer, immutable status and supersession linkage;
- explicit `authorization_state: NONE` in the documentary meaning, not as a new runtime enum.

A Discovery region is never mutated in place to look independently confirmed. Validation support,
narrowing, rejection or any materially revised experiment is appended through immutable linked or
superseding lineage, preserving the original region and every excluded, invalid and missing cell.
The lifecycle labels are derived documentary descriptions of that evidence context; they require no
new `RobustnessRegion` identifier, serialized runtime enum or authorization state.

### 9.2 `FalsifierDispositionReport`

Required semantic fields:

- report identity/version, `EXP-*`, `HYP-*`, optional `STRAT-*` reference and EvidenceIds;
- question, scope, tier completion and dependency availability;
- Data Admissibility, T0, T1, Discovery Sweep, independent Validation, walk-forward, T2 and final
  holdout results in authoritative order;
- diagnostic disposition and scientific `GO`/`NO-GO`/`INCONCLUSIVE` conclusion;
- complete population counts, failures, invalidity, censoring and missingness;
- supported claims separated from unsupported claims and interpretation;
- Formula/Fee/Metadata/Book/Simulator/model/config/code/dataset versions by reference;
- uncertainty, multiplicity/selection limitations and holdout-access audit;
- negative findings, contradictions, deviations and superseded attempts;
- required external revalidation, human decisions and next allowed step;
- immutable artifacts/hashes, reviewer and explicit non-authorization statement.

## 10. Diagnostic dispositions and compatibility audit

The following values are local to `FalsifierDiagnosticDisposition`. They do not reuse or extend
`OrderState`, `EngineState`, `RiskDecision`, `RunMode`, maturity, strategy status or authorization.

| Disposition | Meaning | Compatibility |
|---|---|---|
| `DATA_INSUFFICIENT` | admissibility/support or declared-domain coverage cannot sustain the scoped claim | new namespaced diagnostic; consistent with invalid/low-fidelity data policies |
| `STRUCTURAL_INVALID` | route/class/comparator/math precondition fails for the stated cell or exact scope | new diagnostic; canonical reason remains owned by Graph/Formula |
| `ECONOMIC_NO_EDGE` | valid T0 economics fail for a cell by default; hypothesis-level only after sufficient domain coverage or a canonical scope-wide bound | new diagnostic; not a Risk reject and never an automatic structure-wide rejection |
| `MECHANICAL_NO_EDGE` | T1 path economics/failures remove the edge | new diagnostic; not an ESM status |
| `NO_ROBUST_REGION` | adequately covered scoped Discovery domain has no neighborhood-supported region under the frozen method | new diagnostic; insufficient coverage is instead `DATA_INSUFFICIENT`/`INCONCLUSIVE` |
| `OOS_FAILURE` | independent temporal Validation or walk-forward rejects the preliminary region | new diagnostic; does not overwrite Discovery or per-run facts |
| `ADVERSARIAL_FRAGILE` | frozen validation-supported candidate fails predeclared T2 | new diagnostic; scenario-specific evidence retained |
| `ROBUST_CANDIDATE` | survives independent Validation, walk-forward, T2 and the final untouched holdout inside stated support | new diagnostic; explicitly non-authorizing |
| `INCONCLUSIVE` | evidence cannot decide | exact generic term already used in evidence; namespaced context avoids collision |

The documentary labels `DISCOVERY CANDIDATE REGION`, `VALIDATION-SUPPORTED REGION` and
`ADVERSARIALLY TESTED CANDIDATE` describe evidence maturity; they are not additional values in this
disposition vocabulary. Every negative conclusion remains scoped to the declared hypothesis,
domain, markets/routes, period, q set and execution assumptions. Unsupported fidelity, untested
cells or incomplete coverage cannot silently become `ECONOMIC_NO_EDGE`, `NO_ROBUST_REGION` or a
scientific `NO-GO`.

Existing research reports use `PROMOTE`, `REJECT`, `HOLD` or `INCONCLUSIVE`, while hypothesis
indexes use `OPEN`, `SUPPORTED_WITHIN_SCOPE`, `NOT_SUPPORTED`, `INCONCLUSIVE`, `INVALIDATED` and
`SUPERSEDED`. Falsifier dispositions are intentionally not mapped automatically to those statuses.
Prompt 3 must decide whether they remain a report-local vocabulary or receive a Data-owned schema.

## 11. `PREC-P01` through `PREC-P19` coverage matrix

All 19 October 2026 precision requirements are integrated as documentary requirements. Their
historical source snapshot is not treated as current exchange truth.

| ID | Existing canonical authority | Added Falsifier detail | Deferred issue / conflict |
|---|---|---|---|
| `PREC-P01` | QF-007–016; Graph exact L2 pipeline | T0 rejects midpoint/BBO-only whole-route claims and binds every leg/q to observed support | current feed depth/capability requires dated revalidation; no conflict |
| `PREC-P02` | QF-014/015; Fee/Data versioning; Risk unknown-fee gate | `DataAdmissibilityReport` and runs bind account/market/role/time fee rules, modifiers, rebates and debit assets | current fee/API facts require primary-source revalidation |
| `PREC-P03` | Formula double-count audit; QF-056/057/063/090/106 | run/report cost-owner map; exclusive scenario population; invalid on ambiguous overlap | final serialized cost-lineage field is Prompt 3/Data-owned |
| `PREC-P04` | QF-026/076/077; prediction errors QF-097–099 | exact candidate-q grid, uncertainty and holes; never raises `Q_validated` or duplicates penalties | robustness/sample thresholds human-calibrated |
| `PREC-P05` | Risk safe set; QF-063/075; Recovery exception | objective vector separates new-route admission from defensive loss-taking | no Falsifier authorization; Risk remains owner |
| `PREC-P06` | Graph/Inventory taxonomy; QF-017–023/070–072 | every experiment freezes structure/class/intent; conversion benefit is not absolute profit | Bridge remains later; no conflict |
| `PREC-P07` | OWA comparator contract; QF-019/024/025 | matched decision-time information/deadline/Risk scope and route-vs-execution effects | deadline/comparator valuation conventions remain declared/calibrated |
| `PREC-P08` | Accounting authority; QF-106–108 | disposition report requires separate attributable buckets and exact-once reconciliation | Prompt 3 authority reconciliation only; no formula change |
| `PREC-P09` | Inventory/Capital; ESM partial exposure; QF-068 | T1 reports exposure duration/limits/residuals and conservative executable liquidation separately from accounting valuation | valuation method remains explicit per experiment, not universally invented |
| `PREC-P10` | Participant maker forecasts; ESM maker path; Recorder negative retention | later maker analysis reports conditional-on-fill and all-attempt populations, wait/reservations/cancel/Recovery/opportunity cost | maker capability remains gated and inactive |
| `PREC-P11` | Risk T5; ESM maker lifecycle/Recovery | maker diagram requires repeated remaining-leg economics/Risk through canonical decisions | no new cancel/continue policy; later maker evidence required |
| `PREC-P12` | FillLedger, ESM partial algorithm, actual-fill invariant | T1 propagates only actual simulated available quantized output; actual runs remain unique-fill truth | no conflict |
| `PREC-P13` | ESM cancel/UNKNOWN/timers; Reservations | cancel race and resting/action-expiry distinction are mandatory scenarios | exact `expiresAfter` behavior requires current primary-source revalidation |
| `PREC-P14` | Execution modes and roadmaps; maker validation | TT→TTT→MT/MTT independent gates preserved; optimistic queue cannot establish robustness | HPD-01 and later evidence remain pending; TM/MM future |
| `PREC-P15` | Data SourceQuality/FeedProfile; Recorder quality | admissibility records feed capability, subscription, depth, aggregation, clocks/order, frequency, sequence/gaps/reconnect; documented vs measured separated | exact current feed facts require revalidation |
| `PREC-P16` | QF book walk; Data fidelity; Risk liquidity | unsupported/invisible depth yields invalid cell or smaller predeclared candidate; no extrapolation | richer feeds need separate historical point-in-time validation |
| `PREC-P17` | QF-030–033; Microstructure/Participants proxy boundary | feature name/method/version must say `OFI_snapshot` or equivalent; no exact event-level claim | decision authority requires later temporal OOS evidence |
| `PREC-P18` | Simulator maker queue modes; Participants/Validation calibration | maker T2 represents queue uncertainty and rejects touched-price/reduced-size-as-fill inference | calibration against genuine own fills requires separately authorized evidence |
| `PREC-P19` | L0 RAW, recorder order/clocks/gaps, point-in-time lineage | provenance diagram and admissibility prevent lookahead or retroactive quality repair | old snapshot limitations remain permanent and explicit |

No `PREC-*` item requires a competing Formula Book, duplicate SI/QF identifier or new route
enumeration. No unresolved `CONFLICT` was found. External statements remain
`EXTERNAL_REVALIDATION`, not validated facts.

## 12. Scientific inference and multiple testing

Every adaptive choice—manual rerun, duplicate with changed seed, changed exclusion, expanded route
set, revised chart, added metric or early stop—is part of the experiment family. The report records
the path, not only the final region.

Where confirmatory statistical claims are made, the protocol declares a justified family-wise or
false-discovery method. If no defensible adjustment exists, results are labeled exploratory and
require independent confirmation. Post-selection confidence intervals are not presented as naive
confirmatory intervals. Effective independent units account for overlapping opportunities,
episodes and positions.

Robustness claims require effect size and uncertainty, not a p-value or peak PnL alone. Stable
failure is useful evidence. A negative result is not erased because another parameter point wins.

## 13. Invalid, censored, failed and duplicate outcomes

The run ledger retains:

- every planned and launched evaluation;
- manual reruns and their reason;
- exact duplicates and cache/dedup disposition;
- invalid data/config/math outcomes;
- unsupported Simulator/model regions;
- process/job failures and timeouts;
- unresolved/censored route outcomes;
- zero/partial/full/Recovery/failure paths;
- negative and inconclusive economics;
- abandoned points after a valid predeclared stop.

The denominator for each metric is explicit. `UNKNOWN` at an analysis cutoff is unresolved/censored,
not zero fill or terminal failure. A failed job is not an economic loss. An invalid cell cannot be
dropped from coverage and then described as tested.

## 14. Human decisions required

Prompt 1 does not decide the following:

| Decision | Classification | Safe default until decided |
|---|---|---|
| numeric robustness/neighborhood/sample/uncertainty thresholds | `CALIBRATED / HUMAN_DECISION_REQUIRED` | no robust-region claim |
| exact Bounded Sweep resolution and budget per experiment | `CALIBRATED / HUMAN_DECISION_REQUIRED` | smallest finite defensible predeclared design |
| acceptable missingness/censoring coverage for a claim | `CALIBRATED / HUMAN_DECISION_REQUIRED` | `INCONCLUSIVE` when material |
| final report-local versus serialized disposition vocabulary | `HUMAN_DECISION_REQUIRED` | keep documentary and namespaced |
| final fields/compatibility/versioning of the five artifacts | `HUMAN_DECISION_REQUIRED` under Data/Validation | M0 outline only; no implementation |
| any candidate forwarding/promotion | separate later human/evidence decision | no promotion/authorization |
| any Micro-live/Live/capital use | separate canonical authorization | not authorized |

A human may approve, narrow, defer or reject a later evidence-eligible candidate. Human preference
cannot replace failed evidence, invalid mathematics, stale exchange facts, hard Risk, unsupported q
or an unavailable capability.

## 15. Non-regression audit

This specification preserves:

- `ExchangeTruth > LocalAssumption` and `ActualFill > ExpectedFill`;
- `SafetyOfExistingExposure > NewOpportunity` and the full Risk priority;
- no blind retry; `CancelRequested != Canceled`; UNKNOWN reserves capital;
- partial fill creates exposure immediately;
- immutable RAW, local receive order, explicit clocks/versions/RNG and no lookahead;
- Replay/Simulator/actual truth separation;
- QF-001–QF-110 unchanged and costs exactly once;
- fair OWA comparator; Bridge != OWA; Bridge != Rebalance;
- structural route, economic class, execution mode and accounting intent as orthogonal axes;
- Sizing != Slicing and no fabricated liquidity through fragmentation;
- non-monotonic `ValidatedQSet` and scalar-supremum `Q_validated`;
- TT first, separately gated TTT, separately gated MT/MTT and disabled TM/MM;
- no AI/research auto-promotion, no Live self-learning and no research mutation of economic state;
- exactly 26 canonical technical phases and 21 evidence stages;
- documentation acceptance does not authorize implementation or capital.

QF equation changes: **0**. Risk/ESM transition changes: **0**. Phase/evidence-stage additions:
**0**. Review/HDC/authorization changes: **0**.

## 16. Deferred integration

### Prompt 2

Deferred: Strategy Research/Registry/Workers/Dragonfly/Structure Discovery, generalized Parameter
Search, AI proposal boundaries, distributed research mechanics and any research runtime. This
Prompt-1 Bounded Sweep must not be generalized silently into those capabilities.

### Prompt 3

Deferred: roadmap placement without renumbering, cross-authority reconciliation, final artifact
schema ownership, HDC/precision ledgers, human review package, final F2 integration and any change
to review-candidate identity. Until then, this is an intermediate documentary addition and not an
approved Final Review Candidate.
