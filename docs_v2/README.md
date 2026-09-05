# Documentation v2 — Clean-room rebuild

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

`docs_v2` est reconstruit exclusivement depuis les huit sources originales. Le dossier `/docs` est une référence legacy en lecture seule et n'est pas une autorité de conception.

PASS 00 cartographie les exigences, formules, concepts, conflits et destinations documentaires. PASS 01 a reconstruit Infrastructure. PASS 02 a reconstruit Market Participants / Competition. PASS 03 a reconstruit le Counterfactual Simulator. PASS 04 a reconstruit l'Execution State Machine, ses cinq automates, ses branches de partial/dust/cancel, Recovery, Reconciliation et sa validation depuis les sources originales. PASS 05 a reconstruit la Risk Constitution, ses 30 invariants, ses gates, permissions, kills, contrats, politiques de Recovery et preuves. PASS 06 a reconstruit les Data Contracts, le Recorder, le Replay, la déterminisme, la lineage, la rétention et les règles de checkpoint/recovery. L'ensemble reste soumis à revue humaine.

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

Ordre d'autorité: dossiers de fermeture 1–6 dans leurs domaines, puis sources exploratoires non contredites. Les faits externes datés exigent une revalidation ultérieure.
