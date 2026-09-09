# 09 — Reporting and Knowledge Base

STATUS: DOCUMENT FORMAT SPECIFIED / GENERATOR NOT IMPLEMENTED

The knowledge base is durable evidence, not a results scrapbook. It indexes hypotheses, experiments, benchmarks, strategies, decisions, incidents, postmortems, releases, external facts, datasets and runs with stable links and supersession lineage.

Canonical runtime identities remain `DatasetId`, `RunId`, `IncidentId` and `EvidenceId`. Display forms `DATASET-*`, `RUN-*` and `INC-*` are reversible serializations or registry links, not duplicate IDs. Documentary families use `HYP-*`, `EXP-*`, `BENCH-*`, `STRAT-*`, `ADR-*`, `POST-*`, `REL-*`; external facts continue the existing `EXT-*` register. `HDC-*` records post-reconstruction human requirements and is not replaced by ADR.

Every report has machine facts and interpretation sections. A future deterministic generator owns machine-populated manifest fields, hashes, counts, metrics and links; human or AI content cannot overwrite them. Amendments append or create a superseding version.

An experiment report contains: identity/version/status; hypothesis/falsifier; owner/reviewer; dates; scope; Dataset/Run manifests; code/config/formula/model/strategy versions; split and leakage policy; method/search/seed/budget; primary/guardrail metrics; results and uncertainty; failures/censoring/missingness; sensitivity/OOS/stress; comparison; claim classification; limitations; conclusion; promotion/demotion disposition; linked incidents/ADRs/releases; and immutable artifacts/hashes.

The intended navigation is bidirectional: `StrategySpec -> Experiment -> Incident/Postmortem -> ADR/promotion decision -> Release`, with hypotheses, datasets and runs reachable from every relevant node. This lets a future engineer or AI answer why a strategy, threshold, feature, provider or optimization exists, failed, was rejected, changed, became champion or was retired—without relying on chat history.

Reports must be readable as Markdown by humans and parseable by tools through stable front matter and tables. Indexes may be empty before implementation, but must say `ZERO RECORDED ARTIFACTS`; no fake experiments or placeholder victories are created.

See [the research registry](../../research/README.md) and its templates.
