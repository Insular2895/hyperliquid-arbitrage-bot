# PASS 16 — Review Start Here

> **POST-RECONSTRUCTION CORRECTIONS IN PROGRESS.**
>
> **DO NOT APPROVE THIS REVIEW BASELINE.**
>
> **FINAL REVIEW PACKAGE WILL BE REFRESHED AFTER CORR-06.**

CORR-01 and CORR-02 changed canonical documentation after the PASS16 baseline. All approval remains pending; implementation and legacy switchover remain unauthorized.

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

This package turns the reconstructed corpus into a finite human decision. It is documentary evidence only: implementation, the `docs_v2` → `docs` switchover, Micro-live and Live all remain unauthorized.

## Decision at the end

The reviewer may approve the documentation baseline and, separately, authorize **technical Phase 1 only**. Phase 1 contains domain types, units, identifiers, schema/version contracts, `Clock`, explicit RNG, `RunManifest` foundations and tests. It contains no network connection, exchange adapter, strategy decision, order, signer or capital effect.

## Required reading — first

1. [Safety-critical invariants](04_SAFETY_CRITICAL_INVARIANTS.md)
2. [Open human decisions](14_OPEN_HUMAN_DECISIONS.md)
3. [Implementation authorization checklist](19_IMPLEMENTATION_AUTHORIZATION_CHECKLIST.md)
4. [Final human decision form](21_FINAL_HUMAN_DECISION_FORM.md)

## Required reading — then

1. [Executive project summary](01_EXECUTIVE_PROJECT_SUMMARY.md)
2. [Final system scope](02_FINAL_SYSTEM_SCOPE.md)
3. [Canonical decisions](03_CANONICAL_DECISIONS_SUMMARY.md)
4. [Architecture review](05_ARCHITECTURE_REVIEW.md)
5. [Execution, Risk and Recovery](07_EXECUTION_RISK_AND_RECOVERY_REVIEW.md)
6. [Data, Replay and evidence](08_DATA_REPLAY_AND_EVIDENCE_REVIEW.md)
7. [Implementation and scale roadmaps](13_IMPLEMENTATION_AND_SCALE_ROADMAP_REVIEW.md)

## Should review

- [Formula and economics](06_FORMULA_AND_ECONOMICS_REVIEW.md)
- [Participants, Simulator and models](09_PARTICIPANTS_SIMULATOR_AND_MODELS_REVIEW.md)
- [Capital, Bridge and Sizing](10_CAPITAL_BRIDGE_AND_SIZING_REVIEW.md)
- [Infrastructure, deployment and security](11_INFRA_DEPLOYMENT_AND_SECURITY_REVIEW.md)
- [Validation and operations](12_VALIDATION_AND_OPERATIONS_REVIEW.md)
- [Calibration and learned items](15_CALIBRATION_AND_LEARNED_ITEMS.md)
- [External revalidation checklist](16_EXTERNAL_REVALIDATION_CHECKLIST.md)
- [Research and future scope](17_RESEARCH_AND_FUTURE_SCOPE.md)
- [Final switchover plan](20_FINAL_SWITCHOVER_PLAN.md)

## Evidence tier

- [Source and traceability certificate](18_SOURCE_AND_TRACEABILITY_CERTIFICATE.md)
- [PASS 15 final report](../_analysis/pass15_source_no_loss/PASS15_FINAL_REPORT.md)
- [PASS 14 consistency report](../_analysis/pass14_cross_domain_consistency/PASS14_FINAL_REPORT.md)
- [Formula Book](../04_FORMULA_BOOK.md), 17 [canonical Masters](../README.md), 181 deep specs and PASS00–PASS16 analysis artifacts.

## Review protocol

1. Record the exact PASS 16 commit from the final handoff.
2. Read Tier 1 and Tier 2 in order.
3. Resolve or explicitly defer each scoped item in the decision form.
4. Perform the prepared spot checks and red-team questions.
5. Approve or reject the documentation baseline.
6. Separately authorize or reject Phase 1.
7. Only after explicit approval, follow the deterministic switchover plan.

All approval boxes are intentionally unchecked. Semantic edits after approval require a new reviewed commit.

## Recommended source spot checks

Each row lets the reviewer sample the chain without reopening the full 61,645-line corpus.

| Question | Canonical statement | Canonical file | Requirement ID | Original source / lines | PASS15 traceability entry |
|---|---|---|---|---|---|
| Does one formula own executable conversion? | QF-016 `NetConvert` subtracts converted fee value from gross output under typed walk/rule inputs. | [Formula Book](../04_FORMULA_BOOK.md) | REQ-FORMULA-0029 | SRC-004 `DOSSIER 16 — EXECUTION STATE MACHINE.md`, 4182–4325 | `SRC-004-ITEM-0174`, `EXACT`, `VERIFIED` |
| Can an ambiguous submit be retried? | No blind retry; query order status, fills and open orders first. | [Execution](../10_EXECUTION_STATE_MACHINE.md) | REQ-EXEC-0118 | SRC-004, 584–604 | `SRC-004-ITEM-0024`, `FULL`, `VERIFIED` |
| What wins when Risk objectives conflict? | `Safety > StateConsistency > ExistingExposure > RiskLimits > ExpectedPnL > Opportunity`. | [Risk](../09_RISK_CONSTITUTION.md) | REQ-RISK-0046 | SRC-005 `DOSSIER 36 — RISK CONSTITUTION V1.md`, 3–90 | `SRC-005-ITEM-0003`, `FULL`, `VERIFIED` |
| Must Replay share production logic? | Replay runs in Rust through the canonical Core rather than a divergent Python execution engine. | [Recorder/Replay](../12_RECORDER_AND_REPLAY.md) | REQ-REPLAY-0005 | SRC-002 `Bot hyperliquid .md`, 4421–4478 | `SRC-002-ITEM-0157`, `FULL`, `VERIFIED` |
| Are individual competitor identities claimed? | No; production predicts collective response/survival, with identity agents confined to Research. | [Participants](../06_MARKET_PARTICIPANTS.md) | REQ-PART-9001 | derived from SRC-007 326–425, 1226–1292, 4677–4799, 5308–5380 and SRC-008 1094–1162, 2168–2192 | PASS00 overlay derivation, `FULL`, `OVERLAY_DERIVATION_VERIFIED` |
| How is counterfactual response bounded? | Historical baseline, our mechanical change and modeled response are distinct; the result is not exact alternate truth. | [Simulator](../07_COUNTERFACTUAL_SIMULATOR.md) | REQ-SIM-0001 | SRC-007, 3000–3072 | `SRC-007-ITEM-0067`, `FULL`, `VERIFIED` |
| Can licensing sit in the hot path? | Licensing may control commercial permission but must stay outside the hot path. | [Deployment](../14_DEPLOYMENT_AND_DOCKER.md) | REQ-LIC-0001 | SRC-006 `DOSSIER 56 — DOCKER, DÉPLOIEMENT, SÉCURITÉ ET DISTRIBUTION CLIENT.md`, 1574–1581 | `SRC-006-ITEM-0131`, `FULL`, `VERIFIED` |
| May Micro-live precede sustained Shadow? | No; Shadow is the fifth milestone and Micro-live TT the sixth. | [Validation](../16_VALIDATION_MATRIX.md) | REQ-VALID-0284/0285 | SRC-006, 5753–5758 | `SRC-006-ITEM-0549/0550`, `FULL`, `VERIFIED` |

The row-level evidence is in [`FINAL_SOURCE_ITEM_TRACEABILITY.csv`](../_analysis/pass15_source_no_loss/FINAL_SOURCE_ITEM_TRACEABILITY.csv).

## Red-team checklist

Any **YES** is blocking.

- [ ] Could two orders be sent after a timeout?
- [ ] Could planned fills alter Inventory?
- [ ] Could a canceled-but-unconfirmed order be forgotten?
- [ ] Could a stale book trade?
- [ ] Could unknown fee/precision rules trade?
- [ ] Could two processes own the same account?
- [ ] Could license failure strand exposure or block Recovery/Reconciliation?
- [ ] Could Replay know future data?
- [ ] Could a model or formula silently change?
- [ ] Could a bigger account increase `q` without evidence?
- [ ] Could Bridge loss hide inside Strategy PnL?
- [ ] Could Shadow mutate real Inventory or submit strategy effects?
- [ ] Could rollback resume activity without Reconciliation?
