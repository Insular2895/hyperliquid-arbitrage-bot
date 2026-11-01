# Strategy Research — Deferred Canonical Specifications

`DOCUMENTATION STATUS: F2 PART 2 / INTERMEDIATE DOCUMENTARY WORK / AWAITING HUMAN REVIEW`

`CAPABILITY STATUS: FUTURE SPECIFIED / NOT ACTIVE`

This directory specifies the future research layer of the same production Core. It is not a second
economic engine, a second Strategy/Formula/Risk authority, a Phase 27, or permission to implement,
run research or trade. F2 Part 2 adds documentary lifecycle and orchestration contracts only.

## Baseline-first activation gate

The full Strategy Research Factory remains blocked until the end-to-end baseline exists and is
evidenced: adapters; Recorder; canonical Book; metadata, fees and precision; graph/routes and
full-L2 `NetConvert`; deterministic Replay; baseline Opportunity logic; Inventory and Reservations;
Risk; ESM; transport; Recovery and Reconciliation; canonical Simulator; Shadow; Micro-live actual
evidence; and a bounded, validated baseline. Recorder evidence, deterministic reports and
reconciled attempt outcomes must already exist.

The first success target remains one simple, correct, measurable and reconcilable same-venue
Hyperliquid spot baseline: TT, simple direct/OWA comparison, exact executable L2 economics,
conservative Risk and bounded q. It does not depend on Strategy Discovery, regime portfolios,
Monte Carlo search, AI optimization or drift-driven research. A separately authorized, bounded
local Falsifier batch may become available earlier when all of its Replay/T1 dependencies exist;
that narrow capability does not satisfy or bypass the full Factory gate.

## Authority and ownership

Order of authority:

1. masters, Formula Book, Risk Constitution and Execution state machine;
2. existing Data, Recorder/Replay, Simulator and Validation contracts;
3. this deferred research layer;
4. experiment reports, dashboards and AI/human interpretations.

Research proposes hypotheses, configurations, evidence and documentary candidates. Graph owns
canonical structures/routes; Formula owns economics; Simulator owns counterfactual scenario
evaluation; Execution/Inventory/Reconciliation own actual truth; Risk owns permission; Validation
owns evidence maturity; the authorization system owns activation. No research status is a
`ValidatedCapability`.

## Canonical audit dispositions

| Requirement | Disposition | Ownership result |
|---|---|---|
| QF-001–QF-110, fair OWA comparator and exact-once costs | `EXACT_REUSE` | link Formula/Graph; no research formula |
| `DatasetId`, `RunId`, `EvidenceId`, `IncidentId`, RAW and Replay order | `EXACT_REUSE` | link Data/Recorder; no competing runtime IDs |
| `HYP-*`, `EXP-*`, `STRAT-*`, `BENCH-*`, `ADR-*`, `POST-*`, `REL-*`, `EXT-*` | `EXACT_REUSE` | strengthen the existing Research Knowledge Base |
| Falsifier tiers, Bounded Sweep and `RobustnessRegion` | `EXACT_REUSE` | consume Prompt-1 Validation contracts |
| Strategy hierarchy, identity/materiality rules and immutable version lifecycle | `NEW_REQUIREMENT` | this directory owns documentary research semantics only |
| Experiment Manager, jobs, workers, deterministic aggregation and dashboard views | `NEW_REQUIREMENT` | orchestration/presentation without scientific or trading authority |
| Formula, Risk, ESM, ActualFill, Inventory, Recovery and capability maturity | `CROSS_LINK_ONLY` | canonical owners remain unchanged |
| generalized Parameter Search, Monte Carlo programs, Factory and distributed research | `DEFERRED` | full baseline gate and separate implementation authorization |
| materiality boundary, schema/storage, worker/queue policy and dashboard implementation | `HUMAN_DECISION_REQUIRED` | safe defaults remain documentary/local/disabled |
| DragonflyDB | `DEFERRED` and `HUMAN_DECISION_REQUIRED` | optional benchmark candidate; no dependency or deployment |
| structure proposal serialization and any Core integration | `HUMAN_DECISION_REQUIRED` / `DEFERRED` | human Architecture Review and separate specification |
| master roadmap, HDC, final review, switchover and authorization reconciliation | `DEFERRED` | Prompt 3 |

No accepted `CONFLICT` or authorized `SEMANTIC_CHANGE` was found. If later implementation exposes a
conflict, canonical owners win and the research proposal stops for review.

## Documents and diagram map

| Document | Purpose | Required diagram |
|---|---|---|
| [01 — Scientific iteration loop](01_SCIENTIFIC_ITERATION_LOOP.md) | controlled Factory proposal/evidence loop | D8 Factory and Challenger |
| [02 — Feature registry](02_FEATURE_REGISTRY.md) | point-in-time research inputs | — |
| [03 — Strategy specification and lineage](03_STRATEGY_SPEC_AND_LINEAGE.md) | hierarchy, identity and immutable versions | D1 hierarchy; D2 identity |
| [04 — Parameter search](04_PARAMETER_SEARCH.md) | later generalized search boundary | — |
| [05 — Monte Carlo robustness](05_MONTE_CARLO_ROBUSTNESS.md) | canonical Simulator ensemble driver | — |
| [06 — Temporal OOS and walk-forward](06_TEMPORAL_OOS_AND_WALK_FORWARD.md) | independent temporal evidence | — |
| [07 — Overfit and multiple hypotheses](07_OVERFIT_AND_MULTIPLE_HYPOTHESES.md) | selection/multiplicity control | — |
| [08 — Champion/Challenger](08_CHAMPION_CHALLENGER.md) | last-layer comparison and rollback | consumed by D8 |
| [09 — Reporting and knowledge base](09_REPORTING_AND_KNOWLEDGE_BASE.md) | immutable registry and read-only analytics | D6 lineage; D7 dashboard |
| [10 — Drift and research triggers](10_DRIFT_AND_RESEARCH_TRIGGERS.md) | immutable revision/demotion triggers | D9 drift/version |
| [11 — Research orchestration and workers](11_RESEARCH_ORCHESTRATION_AND_WORKERS.md) | Manager, local/distributed workers, optional coordination | D3 Manager; D4 scale; D5 coordination |
| [12 — Structure discovery and architecture change](12_STRUCTURE_DISCOVERY_AND_ARCHITECTURE_CHANGE.md) | proposed new mechanisms and review | D10 Structure review |

Each D1–D10 diagram includes inputs, operations, outputs, canonical authority, failure/uncertainty
handling and activation timing. The [Research Knowledge Base](../../research/README.md) remains
empty until real evidence exists.

## Human decisions and safe defaults

The following remain `HUMAN_DECISION_REQUIRED`: the materiality rule separating a
`StrategyVersion` from a new `StrategyFamily`; final serialized schemas; registry/storage
technology; local worker concurrency and resource budgets; distributed queue/lease/heartbeat/retry
policy; durable artifact store; any DragonflyDB benchmark or selection; dashboard implementation;
StructureHypothesis serialization; and evidence/readiness thresholds. Until decided, use the
smallest frozen experiment, bounded local execution if separately authorized, immutable files or
manifests, no distributed dependency, no dashboard authority, no promotion and no structure
integration.

## Non-regression and Prompt-3 boundary

This package changes zero QF equations, SI invariants, Risk/ESM transitions, technical phases,
evidence stages, maturity levels or authorization states. It preserves exactly 26 Technical
Phases, 21 Evidence Stages, M0–M5, ActualFill truth, UNKNOWN reservations, no blind retry, no
lookahead, immutable RAW, deterministic Replay, OWA/Bridge/Rebalance distinctions, non-monotonic
`ValidatedQSet`, scalar-supremum `Q_validated`, no automatic promotion, no Live self-learning, no
research trading authority, no production hot-path Dragonfly and no automatic Structure change.

Prompt 3 alone may reconcile the roadmap, HDC/precision ledgers, artifact-schema authority, human
review package, switchover and final F2 governance integration. Documentation presence here does
not approve that work or authorize Phase 1, Research, Shadow, Micro-live, Live or capital.
