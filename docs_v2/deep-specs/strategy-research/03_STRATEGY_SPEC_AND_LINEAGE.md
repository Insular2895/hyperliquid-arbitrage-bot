# 03 — StrategySpec and Lineage

`DOCUMENTATION STATUS: F2 PART 2 / INTERMEDIATE DOCUMENTARY WORK / AWAITING HUMAN REVIEW`

`CAPABILITY STATUS: FUTURE SPECIFIED / NOT ACTIVE`

`StrategySpec` describes a documentary candidate policy evaluated by the existing Core. It is not
an alternate Core and cannot grant Live permission.

## 1. Complete conceptual hierarchy

| Concept | Precise meaning | Identity / example | Never implies |
|---|---|---|---|
| Economic Structure | fundamental route/economic mechanism represented by the canonical Graph plus economic classification | Direct; OWA over `Route2Leg`; Triangle over `Cycle3Leg`; later Bridge with capital-relocation intent | strategy, execution mode or accounting permission |
| Hypothesis | falsifiable economic claim over an explicit Structure, population, conditions and execution assumptions | existing `HYP-*`; “an OWA family may survive exact comparator costs under declared TT scope” | a strategy or positive outcome |
| `StrategyFamily` | coherent logical decision-policy family around a mechanism, sharing the canonical Core | documentary family field; no competing runtime ID | a new Formula, Risk or ESM |
| `StrategySpec` | versioned, scoped candidate policy and its behavior contract | existing `STRAT-*` plus immutable version | implementation, validation or capital |
| Configuration | one exact parameter assignment under a declared family/spec and experiment | canonical serialized config plus content hash | a new `STRAT-*` |
| Experiment | frozen scientific protocol, domains, splits, budget and decision rules | existing `EXP-*` plus immutable version | a favorable result |
| Run | one exact recorded evaluation with dataset/build/config/scenario/version evidence | canonical `RunId` | a strategy or promotion |
| `RobustnessRegion` | Prompt-1 evidence artifact over neighboring evaluated configurations | Discovery, validation-supported and final robust maturity remain distinct | filled q interval, `Q_validated` or authorization |
| `StrategyVersion` | immutable pair `(STRAT-*, version)` with parent, change reason and evidence-transfer limits | `STRAT-XXXX@vN`; version is not another ID family | in-place mutation or inherited validity by default |
| `ValidatedCapability` | separately governed exact-scope capability under M0–M5 and authorization | existing capability/manifest/evidence system | creation by `StrategySpec`, Falsifier GO or status |

Structural route, economic class, execution mode and accounting/capital intent stay orthogonal. For
example, `Route2Leg` is structural; OWA is economic classification requiring a fair direct
comparator; TT is execution mode; Strategy is accounting intent. Bridge is intentional capital
relocation, not a missing OWA comparator, and Rebalance is separate.

### D1 — First OWA/TT baseline path and later Challengers

```text
FIRST BASELINE PATH

OWA/TT HYP-* Hypothesis
          |
          v
Falsifier + Bounded Sweep
(RobustnessRegion / possible ROBUST_CANDIDATE evidence only)
          |
          v
DRAFT Strategy Candidate
          |
          v
Separate Evidence / Authorizations
          |
          v
Replay -> Shadow -> Micro-live
each through its own existing gate
          |
          v
Bounded Validated Baseline
          |
          v
FUTURE STRATEGY RESEARCH FACTORY
full baseline gate now satisfied
          |
          v
New HYP-* / Challengers
          |
          v
full frozen experiment and evidence chain again
```

Read top-to-bottom: the first simple OWA/TT claim is falsified without depending on the future
Factory. Its evidence may justify documenting a DRAFT StrategySpec. That exact candidate can then
enter Replay, Shadow and Micro-live only through their distinct prerequisites, evidence and
authorizations. A bounded baseline becomes validated only after those applicable gates succeed.
Only then may the complete baseline gate permit the future Factory to propose new hypotheses and
Challengers, each of which re-enters the full frozen evidence chain.

Contract — **Inputs:** the initial canonical OWA structure/class, TT mode, Strategy intent,
`HYP-*`, frozen `EXP-*`, admissible datasets and current canonical versions. Future Factory work
additionally requires the already bounded Validated Baseline. **Operations:** the initial path uses
the Bounded Falsifier contract and may produce region/candidate evidence; the same immutable DRAFT
candidate then progresses through separately gated Replay, Shadow and Micro-live. The later
Factory may propose new hypotheses/Challengers but cannot skip their experiments or validation.
**Outputs:** immutable runs, `RobustnessRegion`, a possible non-authorizing `ROBUST_CANDIDATE`, an
optional DRAFT `STRAT-*` version, and—only after separate gates—a bounded Validated Baseline.
Future Factory outputs remain proposals/Challengers. **Canonical authority:** Graph/Formula/Data/
Replay/Simulator/Validation retain scientific and economic truth; Risk, capability governance and
the named human authorization processes retain permission at every stage. **Failure/uncertainty:**
invalid, failed, negative, censored and unsupported evidence remains; failure at any gate stops or
narrows only that exact scope, never fabricates a baseline. **Activation timing:** the initial
OWA/TT DRAFT and its separately authorized Replay/Shadow/Micro-live progression may precede
activation of the Factory. The full baseline gate remains mandatory for the Strategy Research
Factory, generalized Parameter Search, advanced Strategy Discovery and other deferred research
programs.

The bootstrap rule removes a circular dependency: the first bounded OWA/TT StrategySpec helps
establish the baseline that later gates the Factory; the Factory is not a prerequisite for that
first StrategySpec. `DRAFT`, `ROBUST_CANDIDATE`, `OOS_VALIDATED`, `SHADOW_CANDIDATE` and every other
documentary status are evidence labels only. In particular, `ROBUST_CANDIDATE` is not Shadow
permission, and neither a Falsifier result nor a Strategy status authorizes development,
activation, q/capital, an order or Live use. M0–M5, Replay, Risk, Shadow, Micro-live and capital
gates remain independent, explicit and non-transitive.

| D1 part | Inputs and step | Result | Authority | Restriction |
|---|---|---|---|---|
| first OWA/TT falsification | scoped `HYP-*`, frozen `EXP-*`, admissible evidence; run the Bounded Falsifier | retained runs, region and possible `ROBUST_CANDIDATE` evidence | Formula/Data/Replay/Simulator/Validation | no automatic `STRAT-*`, development or next-stage permission |
| first documentary candidate | qualifying evidence is linked to an immutable DRAFT `STRAT-*` version | inspectable candidate lineage | Strategy Research owns documentation only | DRAFT is not implementation, Shadow, capital or Live authorization |
| baseline capability progression | exact candidate plus each stage's prerequisites, evidence and separate authorization | Replay, then Shadow, then Micro-live evidence; bounded Validated Baseline only if all applicable gates pass | M0–M5, Risk, Replay, Shadow, Micro-live and authorization owners | no inherited or automatic transition; failure stops/narrows the exact scope |
| future Research Factory | complete bounded Validated Baseline and full baseline gate | new hypotheses and Challenger proposals | Factory proposes; canonical engines and human governance decide evidence/permission | Factory, generalized search and advanced discovery remain inactive before the full gate |

## 2. StrategySpec contract

Required fields:

- `StrategyId` (`STRAT-*`) and immutable version;
- `StrategyFamily`, economic rationale/expected edge, `HYP-*` links, candidate origin,
  parent/baseline lineage and exact change summary;
- Structure, venue/product/asset/market/route/regime/time scope, supported and unsupported regimes
  and evidence-backed exact q scope;
- eligible point-in-time observations, candidate construction and feature versions;
- supported execution modes, entry/exclusion/abstention, sizing proposal, execution and priority
  policies where independently eligible;
- inventory requirements, Recovery expectations and explicit Risk dependencies;
- parameter schema/domains, locked constants and Configuration canonicalization/hash rule;
- dependencies: Dataset, build, Formula, Fee, Metadata, Book, Graph, Simulator and model versions;
- evidence links: experiments, runs, benchmarks, OOS windows, Monte Carlo and actual outcomes;
- known limitations, OOD/fallback/demotion behavior;
- status, reviewer and separate human decision/authorization links.

The spec may propose q, but canonical capacity, Reservations and Risk decide whether any exact q is
permitted. It may describe desired execution behavior, but ESM, transport, Recovery and
Reconciliation own execution truth. It may reference formulas but cannot fork QF semantics.

Allowed documentary statuses remain `DRAFT`, `RESEARCH`, `OOS_VALIDATED`, `SHADOW_CANDIDATE`,
`MICROLIVE_CANDIDATE`, `CHALLENGER`, `CHAMPION`, `DEMOTED`, `RETIRED`, `INVALID`. Status alone is not
authorization; every capital-bearing transition passes the existing roadmap, evidence, Risk and
human gates. F2 creates no status transition.

## 3. Identity and version boundary

### D2 — Run versus Configuration versus StrategySpec versus StrategyVersion

```text
STRAT-0007 @ v1  (immutable StrategyVersion; illustrative identity only)
       |
       +-- EXP-A / Configuration hash C1 -- RunId R1
       |                                 `-- RunId R2 (rerun/attempt retained)
       |
       +-- EXP-A / Configuration hash C2 ---- RunId R3
       |
       `-- material policy revision ----------> STRAT-0007 @ v2
                                                   |
                                                   `-- new EXP / configs / RunIds

new logical policy family -----------------------> new StrategyFamily
unrepresentable economic mechanism --------------> StructureHypothesis
                                                     (not a live route type)
```

Read left-to-right: many runs may evaluate one configuration; many configurations may evaluate one
immutable version; only a material policy revision creates a version, while a new logical policy
or economic mechanism crosses a higher boundary.

Contract — **Inputs:** existing `STRAT-*`, exact config, `EXP-*`, `RunId` and proposed change.
**Operations:** canonicalize/hash configurations and apply the predeclared materiality policy.
**Outputs:** another run, a new Configuration, a new immutable `StrategyVersion`, a new family
proposal or a `StructureHypothesis`. **Canonical authority:** Research governs documentary lineage;
Graph/Formula/Risk/ESM keep their domains; humans approve family/structure boundaries.
**Failure/uncertainty:** ambiguous materiality is `HUMAN_DECISION_REQUIRED` and defaults to a new
version or proposal without evidence transfer. **Activation timing:** documentary lineage now;
implementation and promotion remain gated.

## 4. Anti-explosion decision rules

| Change | Classification | Identity action | Evidence consequence |
|---|---|---|---|
| q, threshold, seed, scenario or other assignment inside the frozen domain | `New Configuration` | no new `STRAT-*`; retain config hash and RunIds | contributes to the same experiment/region |
| rerun of the exact assignment | new run/attempt | same config; new canonical `RunId` or linked attempt per Data contract | duplicate/manual-rerun reason retained |
| material feature, policy, economics, market/regime scope, parameter domain or execution-policy change | `New StrategyVersion` | same `STRAT-*`, increment immutable version with parent | state exactly which prior evidence is non-transferable; fresh validation where material |
| genuinely new logical decision policy around the mechanism | `New StrategyFamily` | family proposal; create `STRAT-*` only for an actual scoped documentary candidate | new family evidence; no cloned Core |
| mechanism cannot be faithfully represented by canonical Structures | `Proposed New Structure` | `StructureHypothesis`; no live type or automatic `STRAT-*` | human Architecture Review and separate authority specs first |

One Structure can support several families, but a parameter cluster never becomes a family merely
because it is visually distinct. One family can support several `STRAT-*` candidates when scopes
or maintained policy artifacts genuinely differ. Thousands of configurations must not create
thousands of Strategy IDs.

Materiality has no universal numeric threshold. The experiment predeclares a defensible policy;
ambiguous economic/behavioral changes are `HUMAN_DECISION_REQUIRED`. Conservative default: create a
new immutable version, narrow evidence transfer and revalidate. A new family or Structure requires
explicit human review, not automated clustering.

## 5. Lineage, origins and supersession

Lineage is a DAG. A new version records exact parent(s), reason, changed fields, unchanged fields,
evidence consumed, evidence-transfer justification, new validation obligations and supersession
status. No report overwrites an earlier spec or failed/superseded version.

Candidates may originate from human hypotheses, statistical segments, model residuals, incidents,
Capture Funnel losses, regime/participant evidence, external market-structure change or AI
suggestions. Origin is always recorded. AI output is a `HYPOTHESIS` or `INTERPRETATION` until the
named authority makes a separate decision; it cannot create a `ValidatedCapability`.

Final schema serialization and the materiality policy are `HUMAN_DECISION_REQUIRED`. Until decided,
the documentary fields above are M0 outlines, and the safest non-widening classification applies.
