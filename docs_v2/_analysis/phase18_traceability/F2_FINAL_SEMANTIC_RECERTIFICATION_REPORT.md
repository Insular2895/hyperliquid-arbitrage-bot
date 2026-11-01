# F2 Final Documentary and Semantic Recertification Report

`DOCUMENTATION STATUS: PROPOSED RECERTIFICATION EVIDENCE — HUMAN REVIEW PENDING`

`OVERALL RESULT: PASS_WITH_RESERVATIONS / NOT_CERTIFIED`

This report records the final documentary correction and the reproducible checks performed against
the exact F2 starting subject. It does not certify profitability, current external facts, runtime
behavior or implementation, and it grants no authorization.

## 1. Exact starting subject

| Field | Value |
|---|---|
| repository | `Insular2895/hyperliquid-arbitrage-bot` |
| branch | `f2-governance-p3` |
| required starting commit | `19e69ab067456bae28e883462662e9252b1947c1` |
| required starting tree | `c2cace47d8e9a21da6bbe99127020fa24ce9edb3` |
| observed starting commit/tree | exact match |
| pre-existing untracked item | `.DS_Store`, excluded from every commit |
| correction scope | documentary only |

The commit containing this report is a later evidence envelope. Its SHA/tree are intentionally not
self-embedded. They must be read from Git after commit and verified externally.

## 2. Audit inputs and evidence boundary

The supplied package was read in full. Its files were treated as evidence and proposed tooling,
not as authority independent of the user's request.

- `INSTRUCTIONS_CODEX.md`;
- `RAPPORT_FINAL_AUDIT_SEMANTIQUE_F2.md`;
- `F2_PRECISIONS_SOURCE_ADDENDUM.md`;
- `Verification_F2_corrige.py` and `test_verification_f2.py`;
- `appliquer_addendum_f2.py` and `test_addendum_f2.py`.

The raw file `Hyperliquid_Fiche_precisions_conception_v1.md` was not present under that exact name
in the local Downloads tree or the local Spotlight index. Consequently:

- the source-to-F2 semantic comparison uses the supplied full audit report and addendum;
- cryptographic identity and direct byte-for-byte rereading of that precision source are
  `NOT_RUN` in this execution;
- October 2026 exchange/API statements remain dated claims requiring official-source
  revalidation before implementation.

## 3. Supplied tooling execution

### Unit tests

Executed with Python bytecode generation disabled:

```text
python3 -m unittest discover -v -s . -p 'test_*.py'
```

Result: six tests passed.

| Test family | Cases | Result |
|---|---:|---|
| corrected Git directory resolution | 4 | PASS |
| one-time addendum application and exact P14 replacement | 2 | PASS |

### Corrected verifier on the previous exact F2 subject

Executed:

```text
python3 Verification_F2_corrige.py <repo> --all-markdown
```

The default immutable target was `6511185315af8ea022bf33542ca27f894e6bc3bb`, tree
`033231c1e729afcf16f86c72e1b826f266fdd2ec`.

| Check | Observed | Result |
|---|---:|---|
| exact expected tree | match | PASS |
| historical F ancestry | descendant | PASS |
| F→subject delta | 51 Markdown blobs; 41 modified, 10 added, 0 deleted | PASS |
| protected core documents | all unchanged | PASS |
| historical inventory/extractions/mapping/HDC rows | unchanged | PASS |
| QF/SI/HDC/PREC/phases/stages | expected inventories | PASS |
| all-Markdown paths | 948 files, 883 relative targets, 0 broken | PASS |
| aggregate | `PASS_WITH_FULL_SOURCE_RECERTIFICATION_OUTSTANDING` | PASS_WITH_RESERVATION |

This reproduces removal of the former false positive for the valid Git directory
`docs_v2/_analysis/pass08_graph_routes_quant/`.

### Addendum application

The applicator dry-run passed on the exact starting HEAD and expected target blob
`e84cf1b2183ac7266b4a7bee072101ccbe36035e`. The applicator was then executed in a detached
temporary worktree. Its output changed exactly one file and produced blob
`1224650a42992d1f1e0eff7f830c20f42536051e`.

The same reviewed diff was applied to the working branch. Before this report was added, the only
tracked modification was:

```text
docs_v2/_analysis/f2_final_integration/F2_PRECISION_AND_HDC_TRACEABILITY.md
```

## 4. HYP-P01…P19 to PREC-P01…P19 reconciliation

The source and F2 namespaces are ordinal aliases for traceability, not separate executable
families:

| Source | F2 | Source | F2 |
|---|---|---|---|
| `HYP-P01` | `PREC-P01` | `HYP-P11` | `PREC-P11` |
| `HYP-P02` | `PREC-P02` | `HYP-P12` | `PREC-P12` |
| `HYP-P03` | `PREC-P03` | `HYP-P13` | `PREC-P13` |
| `HYP-P04` | `PREC-P04` | `HYP-P14` | `PREC-P14` |
| `HYP-P05` | `PREC-P05` | `HYP-P15` | `PREC-P15` |
| `HYP-P06` | `PREC-P06` | `HYP-P16` | `PREC-P16` |
| `HYP-P07` | `PREC-P07` | `HYP-P17` | `PREC-P17` |
| `HYP-P08` | `PREC-P08` | `HYP-P18` | `PREC-P18` |
| `HYP-P09` | `PREC-P09` | `HYP-P19` | `PREC-P19` |
| `HYP-P10` | `PREC-P10` | — | — |

Computed F2 inventory: exactly `PREC-P01..PREC-P19`, contiguous, with no twentieth entry.

Result: `19/19 TRACEABLE`, `0 ABSENT`, `0 NEW EXECUTABLE ID FAMILY`.

## 5. Semantic clarification checks

| Family | Preserved intent | Result |
|---|---|---|
| profitability | entry requires supported net economics; a Risk-governed defensive exit may realize a loss | PASS documentary |
| maker/taker | viability is independently evidenced; taker profitability is not a prerequisite for maker research | PASS documentary |
| activation | TT-first is staged operational activation, not economic dependence or MT/MTT permission | PASS documentary |
| scenario accounting | outcomes exclusive, probability total one, no duplicate L2/adverse-selection/Recovery charge | PASS documentary |
| uncertainty accounting | no second penalty for uncertainty already absorbed by RAEV | PASS documentary |
| comparator | decision-time comparator/deadline/budget frozen; no ex-post taker selection | PASS documentary |
| portfolio accounting | conversion savings not added again to portfolio PnL; valuation/liquidation/reporting currency separated | PASS documentary |
| execution | unique actual fills, late/partial fill exposure, reservations and cancel races preserved | PASS documentary |
| cancellation | `expiresAfter` is not guaranteed resting-order cancellation | PASS documentary |
| market data | snapshot L2/OFI/queue limits explicit; silence distinguished from verified outage | PASS documentary |
| historical fidelity | no retroactive upgrade of old data | PASS documentary |
| implementation/profitability evidence | explicitly unvalidated | PASS documentary |

No Formula, Risk, ESM, Inventory, FillLedger, QF or SI contract was changed. The clarification adds
no phase, Evidence Stage, HDC, capability, capital scope or authorization.

## 6. Repository-wide documentary controls

Checks were run on the corrected working corpus before commit.

| Control | Observed | Result |
|---|---:|---|
| Markdown files decoded | 950 | PASS |
| unclosed fenced blocks | 0 | PASS |
| local references | 916 | PASS |
| local file references | 889 | PASS |
| local directory references | 1 | PASS |
| local anchor references | 26 | PASS |
| anchors indexed | 8,974 | PASS |
| missing local path/anchor | 0 | PASS |
| unique HTTP(S) targets reachable at check time | 50/50 | PASS |
| `git diff --check` | no error | PASS |

The addendum introduces no link. Point-in-time reachability does not prove the authority, freshness or
meaning of external content.

## 7. Frozen inventories and protected contracts

| Inventory | Recomputed result | Result |
|---|---:|---|
| Formula | 110 contiguous `QF-001..QF-110` | PASS |
| Safety invariants | 29 contiguous `SI-001..SI-029` | PASS |
| HDC | 100 contiguous `HDC-001..HDC-100` | PASS |
| historical HDC | exact `HDC-001..HDC-094` text unchanged from F | PASS |
| precisions | 19 contiguous `PREC-P01..PREC-P19` | PASS |
| technical phases | exact `1..26` | PASS |
| Evidence Stages | exact `1..21` | PASS |

No working-tree diff existed in:

- `04_FORMULA_BOOK.md`;
- `08_INVENTORY_AND_CAPITAL.md`;
- `09_RISK_CONSTITUTION.md`;
- `10_EXECUTION_STATE_MACHINE.md`;
- `11_DATA_CONTRACTS.md`;
- `12_RECORDER_AND_REPLAY.md`;
- Roadmaps 17/19;
- the aggregate HDC register.

## 8. Authorization boundary

The canonical decision form remains unchanged.

| Scope | Current status |
|---|---|
| Documentation approval | PENDING |
| Phase 1 development | NOT_AUTHORIZED / prerequisite unavailable |
| Phase 2+ development | NOT_AUTHORIZED |
| Shadow | NOT_AUTHORIZED |
| Micro-live | NOT_AUTHORIZED |
| Live | NOT_AUTHORIZED |
| MT/MTT | NOT_AUTHORIZED |
| Strategy Discovery / Parameter Search / Monte Carlo | NOT_AUTHORIZED |
| real orders/capital/exchange effects | NOT_AUTHORIZED |
| `docs_v2 -> docs` switchover | NOT_AUTHORIZED / NOT_EXECUTED |

Maker viability clarification does not authorize maker research execution, MT/MTT, Shadow,
Micro-live, Live or capital.

## 9. PASS / FAIL / NOT_RUN register

| Item | Status | Reservation |
|---|---|---|
| exact starting Git identity | PASS | none |
| supplied unit tests | PASS | six cases |
| corrected verifier on previous exact subject | PASS | full-source recertification remains separate |
| one-file correction guard and resulting blob | PASS | exact reviewed output |
| HYP↔PREC ordinal mapping | PASS_WITH_RESERVATION | raw precision source not locally materialized |
| semantic qualifier coverage | PASS_WITH_RESERVATION | based on supplied audit/addendum |
| local Markdown paths and anchors | PASS | zero broken |
| QF/SI/HDC/PREC/phases/stages | PASS | identity/structure, not runtime validity |
| failures requiring a repository correction beyond the addendum | PASS: NONE FOUND | — |
| raw precision-source SHA-256 and direct byte reread | NOT_RUN | source file unavailable locally |
| current Hyperliquid/API fact revalidation | NOT_RUN | requires fresh official sources |
| real profitability/maker fill/queue validation | NOT_RUN | requires empirical evidence |
| runtime, trading, deployment or capital tests | NOT_RUN | outside documentary scope |
| human documentation approval | NOT_RUN / PENDING | human DecisionRecord required |
| formal certification | NOT_CERTIFIED | mandatory evidence/review reservations remain |

## 10. Final disposition

```text
DOCUMENTARY_CORRECTION: PASS
SEMANTIC_RECONCILIATION: PASS_WITH_RESERVATIONS
FORMAL_CERTIFICATION: NOT_CERTIFIED
DOCUMENTATION_APPROVAL: PENDING
DEVELOPMENT: NOT_AUTHORIZED
SHADOW: NOT_AUTHORIZED
MICRO_LIVE: NOT_AUTHORIZED
LIVE: NOT_AUTHORIZED
REAL_CAPITAL_OR_ORDER_EFFECTS: NOT_AUTHORIZED
SWITCHOVER_DOCS_V2_TO_DOCS: NOT_AUTHORIZED / NOT_EXECUTED
```

No stage promotes itself. The exact post-commit SHA/tree and the corrected-verifier result for that
immutable commit must be recorded externally after commit; producing those values does not grant
approval or authorization.
