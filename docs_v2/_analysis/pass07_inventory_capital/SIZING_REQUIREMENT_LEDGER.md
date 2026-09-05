# Sizing Requirement Ledger

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

This focused ledger groups the sizing obligations extracted from the 545-row domain ledger. Row-level IDs and dispositions are in `INVENTORY_CAPITAL_REQUIREMENT_LEDGER.md`.

| Obligation | Status | Owner | Destination | Source/QF |
|---|---|---|---|---|
| Position Sizing chooses total exposure, not child execution | LOCKED | Sizing | Master §20/23 + deep 06/07 | SRC-003 §§39–47; QF-075 |
| Maximum Profitable Size differs from Validated Capacity | LOCKED | Sizing/Formula | deep 06 | QF-027/QF-076 |
| Evaluate nonlinear size curve | LOCKED | Sizing + Simulator input | deep 06 | SRC-003 §39; SRC-006 §79 |
| Intersect balance, book, validated, Risk, future inventory and capability | LOCKED | Sizing/Risk | matrix + deep 06 | QF-073–076; SRC-005 §59 |
| P+, CVaR/ES, impact, completion, confidence/OOD at every q | LOCKED | Risk/Simulator/Sizing | matrix + validation | QF-040–042/059/062; SRC-006 §78 |
| `Q_validated` is evidence/state/mode dependent | LOCKED | Sizing | master §21 + deep 06 | QF-076; SRC-008 §44 |
| `Q_validated` may increase or decrease | LOCKED | Validation/Sizing | deep 11 | SRC-006 §§274–277 |
| Search uses candidate grid, best region, local refinement | LOCKED | Sizing | master §22 | QF-077 |
| Return q*=0 if no valid point | LOCKED | Sizing/Risk | deep 06 | SRC-006 §82 |
| TT/MT/TTT/MTT have distinct capacity curves | LOCKED interface | Sizing/Execution/Simulator | deep 06/07 | PASS02–04 contracts |
| 40–50 EUR is Micro-live probe, not strategy size | LOCKED | Validation | deep 11 | SRC-006 §139 |
| No fixed percent/Kelly/auto-compound rule | LOCKED negative constraint | Sizing/Risk | master §26 | SRC-003; SRC-005 §150 |
| Horizontal opportunities still obey shared resources | LOCKED | Portfolio | deep 08 | QF-078 |

Exact thresholds, size grid and `Q_validated` values are CALIBRATED/LEARNED; formula structures are not restated as alternatives.
