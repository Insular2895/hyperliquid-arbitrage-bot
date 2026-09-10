# Hyperliquid Arbitrage Bot

Documentation canonique candidate d'un moteur spot de routing/arbitrage Hyperliquid.

| État | Valeur |
|---|---|
| Current review candidate | [`docs_v2/`](docs_v2/README.md) |
| Legacy reference | [`docs/`](docs/README.md) |
| Switchover | `NOT PERFORMED` |
| Human approval | `PENDING` |
| Implementation | `NOT AUTHORIZED` |

Le dépôt décrit l'architecture, les contrats, les invariants, les formules, le
risque, l'exécution, le Replay, le déploiement et la validation. La reconstruction
PASS00–PASS16, les corrections CORR-01→CORR-06, l'extension documentaire de
recherche scientifique différée et la finalisation async/concurrence sont terminées comme candidat de
revue. Elles n'autorisent ni code de production, ni ordre, ni capital, ni
basculement de `docs_v2/` vers `docs/`.

## Revue actuelle

1. [Commencer la revue finale](docs_v2/_review/00_REVIEW_START_HERE.md)
2. [Finalisation async et concurrence](docs_v2/_analysis/async_concurrency_architecture/ASYNC_ARCHITECTURE_FINAL_REPORT.md)
3. [Extension scientifique et stratégie future](docs_v2/_analysis/future_strategy_research_and_lifecycle/FINAL_REPORT.md)
4. [Architecture maîtresse](docs_v2/00_MASTER_ARCHITECTURE.md)
5. [Formula Book — QF-001 à QF-110](docs_v2/04_FORMULA_BOOK.md)
6. [Risk Constitution](docs_v2/09_RISK_CONSTITUTION.md)
7. [Execution State Machine](docs_v2/10_EXECUTION_STATE_MACHINE.md)
8. [Roadmap d'implémentation](docs_v2/17_IMPLEMENTATION_ROADMAP.md)
9. [Formulaire de décision humaine](docs_v2/_review/21_FINAL_HUMAN_DECISION_FORM.md)

## Gouvernance

Les décisions post-reconstruction `HDC-001..094` restent `PENDING FINAL REVIEW`.
Les paramètres `CALIBRATED`, `LEARNED`, `OPEN` ou `EXTERNAL_REVALIDATION` ne sont
pas des constantes implicites. Les faits Hyperliquid courants ont été rafraîchis
le 2026-09-09, mais doivent être revalidés avant leur consommateur et lors d'un
changement documentaire, réseau ou logiciel pertinent.

`DOCUMENTATION STATUS: CORR-01..06 + SCIENTIFIC ITERATION + ASYNC/CONCURRENCY FINALIZATION COMPLETE — HUMAN REVIEW PENDING`

**NEXT: FINAL HUMAN REVIEW.**
