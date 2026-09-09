# 03 — StrategySpec and Lineage

STATUS: FUTURE SPECIFIED / NOT ACTIVE

`StrategySpec` describes a candidate policy evaluated by the existing Core. It is not an alternate Core and cannot grant Live permission.

Required fields:

- `StrategyId` (`STRAT-*`) and immutable version;
- family, economic rationale/expected edge, hypothesis links, candidate origin, parent/baseline lineage and change summary;
- venue/product/asset/market/route/regime/time scope, supported and unsupported regimes and validated q scope;
- eligible observations, candidate construction and feature versions;
- supported execution modes, entry/exclusion/abstention, sizing proposal, execution and priority policies;
- inventory requirements, Recovery expectations and explicit Risk dependencies;
- parameter schema, bounds and locked constants;
- dependencies: Dataset, build, Formula, fee, metadata, Book, Simulator and model versions;
- evidence links: experiments, benchmarks, OOS windows, Monte Carlo and actual outcomes;
- known limitations, OOD/fallback/demotion behavior;
- status and human approval record.

The spec may propose q, but canonical capacity, Reservations and Risk decide whether any q is permitted. It may describe desired execution behavior, but the ESM, transport, Recovery and Reconciliation own execution truth. It may reference formulas but cannot fork QF semantics.

Lineage is a DAG. A new version states exactly what changed and which prior evidence remains transferable. Material feature, rule, parameter-domain, execution-policy or economics changes require a new immutable version and a fresh validation disposition. No report overwrites a prior spec.

Allowed statuses: `DRAFT`, `RESEARCH`, `OOS_VALIDATED`, `SHADOW_CANDIDATE`, `MICROLIVE_CANDIDATE`, `CHALLENGER`, `CHAMPION`, `DEMOTED`, `RETIRED`, `INVALID`. Status alone is not authorization; each capital-bearing transition also passes the existing roadmap and human/Risk gates.

Candidates may originate from human hypotheses, statistical segments, model residuals, incidents, Capture Funnel losses, regime/participant evidence, external market-structure change or AI suggestions. Origin is always recorded. `StrategyFamily` shares a logical engine; each scoped candidate is a distinct `StrategySpec` version rather than copied Core logic.
