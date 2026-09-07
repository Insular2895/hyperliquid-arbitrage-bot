# PASS 16 — Critical Invariant Source Map

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Invariant family | Rules covered | Canonical authorities | Principal proof |
|---|---|---|---|
| constitutional priority and fail-less-active | priority hierarchy; no hard bypass; failure narrows | `09_RISK_CONSTITUTION.md`, `16_VALIDATION_MATRIX.md` | Risk property/fault suite |
| coherent inputs | no stale book; known fee/precision; no lookahead; pinned versions | `11_DATA_CONTRACTS.md`, `12_RECORDER_AND_REPLAY.md`, `04_FORMULA_BOOK.md` | gap/freshness/parity/leakage tests |
| resource ownership | reserve first; no double spend; UNKNOWN locks | `08_INVENTORY_AND_CAPITAL.md`, `09_RISK_CONSTITUTION.md`, `10_EXECUTION_STATE_MACHINE.md` | concurrent reservation/restart replay |
| execution truth | no blind retry; SENT may execute; cancel intent nonterminal; actual fills only; partial-fill update | `10_EXECUTION_STATE_MACHINE.md` | zero/full/partial/unknown/cancel traces |
| closure | Recovery current state; sunk cost ignored; reconciliation after uncertainty | `10_EXECUTION_STATE_MACHINE.md`, `09_RISK_CONSTITUTION.md` | recovery/reconciliation fault suite |
| semantic boundaries | Sizing≠Slicing; OWA comparator; Bridge≠OWA; action classes distinct | `03_MARKET_GRAPH_AND_ROUTES.md`, `08_INVENTORY_AND_CAPITAL.md` | classification/quantity/accounting vectors |
| evidence/permission | capital≠Qvalidated; implemented≠validated; licensed≠validated; running≠ready | `16_VALIDATION_MATRIX.md`, `14_DEPLOYMENT_AND_DOCKER.md` | manifest/readiness/permission tests |
| ownership/rollback | rollback≠exchange rollback; no dual owner | `00_MASTER_ARCHITECTURE.md`, `14_DEPLOYMENT_AND_DOCKER.md` | ownership audit + rollback drill |

Mapped safety rules: 28/28 in `_review/04_SAFETY_CRITICAL_INVARIANTS.md`. Documentary presentation does not claim implemented proof.
