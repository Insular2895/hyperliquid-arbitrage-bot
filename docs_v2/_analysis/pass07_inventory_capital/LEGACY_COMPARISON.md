# PASS07 Legacy Comparison

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Comparison was performed only after V2 reconstruction against `docs/08_INVENTORY_AND_CAPITAL.md`, `docs/03_MARKET_GRAPH_AND_ROUTES.md`, `docs/04_FORMULA_BOOK.md`, `docs/09_RISK_CONSTITUTION.md`, `docs/10_EXECUTION_STATE_MACHINE.md`, `docs/16_VALIDATION_MATRIX.md` and relevant `docs/specs/**`. Legacy files were not edited.

| Classification | Legacy finding | V2 treatment |
|---|---|---|
| RECOVERED | Actual-fill inventory and balance/reservation separation | Master §§4/24 + deep 01/08 |
| RECOVERED | Core/Transit/Excluded and bands | Master §§5–7 + matrices |
| RECOVERED | Terminal Viability/credible exit | Master §§8–10 + deep 02/03 |
| RECOVERED | Bridge/relocation economics and STAY | Master §§12–19 + deep 04/05 |
| RECOVERED | Nonlinear sizing and shared capacity | Master §§20–25 + deep 06–08 |
| RECOVERED | Hierarchical PnL attribution | Master §27 + deep 10 |
| OVER_COMPRESSED | OWA/Bridge/Rebalance/Recovery boundaries | Expanded taxonomy and deep 09 |
| OVER_COMPRESSED | `Q_validated` vs maximum profitable size | Expanded deep 06 and constraint matrix |
| MISSING | Candidate/rejected Bridge and complete size-curve datasets | Added Replay/evidence contract |
| MISSING | Point-in-time Atlas/relocation no-lookahead | Added cross-domain interface |
| MISSING | Explicit decision penalty vs realized accounting | Added deep 03/10 |
| SUPERSEDED | Fixed inventory percentages/50 EUR normal size | Examples retained only as calibration/probe |
| SUPERSEDED | Fewest-hop Bridge and independent full route capacity | Economic paths + joint reservations |
| CONTRADICTED | Positive route edge always acceptable | Terminal/Risk/portfolio gates take precedence |
| LEGACY_UNTRACED | Generic useful portfolio prose without SRC-001–008 locator | Not promoted; remains legacy-only |
| ROUTED_TO_PASS08 | Market Graph topology, route catalog, Atlas, HOT/WARM/COLD | Explicit PASS08 dependency |
| ROUTED_TO_PASS11 | Formula expression/unit audit and Formula Index extraction defects | `FORMULA_CROSSCHECK.md` |

Material omission families recovered: 12. Legacy edits: 0.
