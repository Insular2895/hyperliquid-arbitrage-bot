# Documentation v2 — Clean-room rebuild

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

> **POST-RECONSTRUCTION CORRECTIONS IN PROGRESS.** The PASS16 review baseline is stale after CORR-01 through CORR-04. Do not approve or implement it until the correction series is complete and the review package is refreshed.

`docs_v2` est reconstruit exclusivement depuis les huit sources originales. Le dossier `/docs` est une référence legacy en lecture seule et n'est pas une autorité de conception. La reconstruction, l'audit transversal et la vérification source sans perte sont terminés comme **candidat**; l'approbation humaine, le basculement documentaire et toute implémentation restent en attente.

Les corrections postérieures `HDC-001..050` ont une origine humaine explicitement séparée; elles ne sont pas rétro-attribuées aux huit sources. Voir [CORR-01](_analysis/corr01_capture_observability/CORR01_FINAL_REPORT.md), [CORR-02](_analysis/corr02_hot_path_performance/CORR02_FINAL_REPORT.md), [CORR-03](_analysis/corr03_execution_completion/CORR03_FINAL_REPORT.md), [CORR-04](_analysis/corr04_infrastructure_execution_path/CORR04_FINAL_REPORT.md) et le [registre des décisions humaines](_analysis/POST_RECONSTRUCTION_HUMAN_DECISIONS.md).

PASS 00 cartographie les exigences, formules, concepts, conflits et destinations documentaires. PASS 01–10 reconstruisent Infrastructure, Participants, Simulator, Execution, Risk, Data/Replay, Inventory/Capital, Graph/Quant, Deployment/Security et Validation/Operations. PASS 11 audite les 110 contrats mathématiques. PASS 12 reconstruit séparément l'ordre technique et le parcours scientifique qui mène de la donnée à une capacité validée. PASS 13 assemble ces autorités dans une architecture transversale sans les remplacer. PASS 14 vérifie leurs interfaces, propriétaires, unités, états, modes et dépendances comme un seul système. PASS 15 rouvre les huit sources, vérifie leurs empreintes et leur couverture ligne par ligne, puis joint 2 577 unités PASS 00, 13 dérivations explicites et 79 récupérations documentées à leur sort final. PASS 16 fournit enfin un package fini de revue, de décisions, d'autorisation et de basculement sans s'auto-approuver.

- [PASS 16 — Start here](./_review/00_REVIEW_START_HERE.md)
- [PASS 16 final report](./_analysis/pass16_human_review/PASS16_FINAL_REPORT.md)

- [00 — Master Architecture](00_MASTER_ARCHITECTURE.md)
- [Architecture deep specs](deep-specs/architecture/README.md)
- [PASS 13 evidence](./_analysis/pass13_master_architecture/PASS13_FINAL_REPORT.md)
- [PASS 14 cross-domain consistency evidence](./_analysis/pass14_cross_domain_consistency/PASS14_FINAL_REPORT.md)
- [PASS 15 source-by-source no-loss evidence](./_analysis/pass15_source_no_loss/PASS15_FINAL_REPORT.md)
- [13 — Infrastructure](13_INFRASTRUCTURE.md)
- [Infrastructure deep specs](deep-specs/infrastructure/README.md)
- [PASS 01 evidence](./_analysis/pass01_infrastructure/PASS01_FINAL_REPORT.md)
- [06 — Market Participants](06_MARKET_PARTICIPANTS.md)
- [Market Participants deep specs](deep-specs/participants/README.md)
- [PASS 02 evidence](./_analysis/pass02_participants/PASS02_FINAL_REPORT.md)
- [07 — Counterfactual Simulator](07_COUNTERFACTUAL_SIMULATOR.md)
- [Counterfactual Simulator deep specs](deep-specs/simulator/README.md)
- [PASS 03 evidence](./_analysis/pass03_simulator/PASS03_FINAL_REPORT.md)
- [10 — Execution State Machine](10_EXECUTION_STATE_MACHINE.md)
- [Execution deep specs](deep-specs/execution/README.md)
- [PASS 04 evidence](./_analysis/pass04_execution/PASS04_FINAL_REPORT.md)
- [09 — Risk Constitution](09_RISK_CONSTITUTION.md)
- [Risk deep specs](deep-specs/risk/README.md)
- [PASS 05 evidence](./_analysis/pass05_risk/PASS05_FINAL_REPORT.md)
- [11 — Data Contracts](11_DATA_CONTRACTS.md)
- [Data deep specs](deep-specs/data/README.md)
- [12 — Recorder and Replay](12_RECORDER_AND_REPLAY.md)
- [Recorder/Replay deep specs](deep-specs/recorder-replay/README.md)
- [PASS 06 evidence](./_analysis/pass06_data_recorder_replay/PASS06_FINAL_REPORT.md)
- [08 — Inventory and Capital](08_INVENTORY_AND_CAPITAL.md)
- [03 — Market Graph and Routes](03_MARKET_GRAPH_AND_ROUTES.md)
- [05 — Market Microstructure](05_MARKET_MICROSTRUCTURE.md)
- [14 — Deployment and Docker](14_DEPLOYMENT_AND_DOCKER.md)
- [16 — Validation Matrix](16_VALIDATION_MATRIX.md)
- [18 — Operations and Monitoring](18_OPERATIONS_AND_MONITORING.md)
- [04 — Formula Book](04_FORMULA_BOOK.md)
- [Formula deep specs](deep-specs/formulas/README.md)
- [PASS 11 evidence](./_analysis/pass11_formula_book/PASS11_FINAL_REPORT.md)
- [17 — Technical Implementation Roadmap](17_IMPLEMENTATION_ROADMAP.md)
- [19 — Build / Validate / Scale Journey](19_BUILD_VALIDATE_SCALE_ROADMAP.md)
- [Roadmap deep specs](deep-specs/roadmaps/README.md)
- [PASS 12 evidence](./_analysis/pass12_build_validate_scale/PASS12_FINAL_REPORT.md)

Ordre d'autorité: dossiers de fermeture 1–6 dans leurs domaines, puis sources exploratoires non contredites. Les faits externes datés exigent une revalidation ultérieure.

**NEXT:** attendre une autorisation explicite pour CORR-03. Aucun successeur automatique. L'implémentation, le basculement `docs_v2` → `docs`, Micro-live et Live ne sont pas autorisés.
