# Formula Crosscheck

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

SRC-004 is authoritative. PASS07 checked consumer semantics and status; it does not create alternative formulas. `FORMULA_INDEX.md` locator extraction defects are explicitly routed to PASS11.

| QF | Name | Source status | PASS07 use | Crosscheck |
|---|---|---|---|---|
| QF-016 | NetConvert | LOCKED | executable conversion for route/Bridge/exit | OK; prevents fee/spread/slippage reinvention |
| QF-026 | Edge Curve | LOCKED | quantity-dependent edge | OK; vertically rendered expression needs PASS11 audit |
| QF-027 | Maximum Profitable Size | LOCKED | profitability boundary, not validation capacity | OK |
| QF-040 | Depth Participation | LOCKED | size/Risk constraint | OK |
| QF-041 | Volume Participation | LOCKED | size/Risk constraint | OK |
| QF-042 | Mechanical Impact | LOCKED | size-dependent cost/gate | OK |
| QF-056 | Expected Value | LOCKED | outcome aggregation | SOURCE OK; Formula Index locator captures only normalization clause—PASS11 |
| QF-057 | Execution EV | LOCKED | full/partial/failure economics | SOURCE OK; Formula Index locator incomplete—PASS11 |
| QF-059 | Probability Positive PnL | LOCKED | sizing gate | OK |
| QF-062 | CVaR / Expected Shortfall | LOCKED | tail constraint | OK |
| QF-063 | Risk-Adjusted EV | CALIBRATED | sizing/allocation objective | OK; keep components/double-count convention aligned |
| QF-064 | Normalized Inventory Deviation | LOCKED | comparable distance to target | SOURCE OK; Formula Index locator omits full fraction—PASS11 |
| QF-065 | Soft Inventory Penalty | CALIBRATED | decision penalty | OK; not realized PnL |
| QF-066 | Hard Inventory Gate | LOCKED | future-state hard reject | SOURCE OK; Formula Index vertical extraction incomplete—PASS11 |
| QF-067 | Net Flow | LOCKED | directional accumulation | OK |
| QF-068 | Expected Exit Cost | LOCKED STRUCTURE | terminal/stranded/Bridge | OK; size-dependent executable exit |
| QF-069 | Stranded Capital Penalty | CALIBRATED STRUCTURE | exit + idle + risk components | OK; components stored separately |
| QF-070 | Bridge Cost | LOCKED STRUCTURE | relocation path cost | OK; NetConvert avoids duplicate costs |
| QF-071 | Bridge Break-Even Cycles | LOCKED | amortization | SOURCE OK; Formula Index locator shows only infinity branch—PASS11 |
| QF-072 | Capital Relocation Value | LOCKED STRUCTURE | move versus stay | OK |
| QF-073 | Available Balance | LOCKED | actual minus reserved | OK |
| QF-074 | Available Book Capacity | LOCKED | observed minus reserved capacity | OK |
| QF-075 | Position Sizing Objective | LOCKED OPTIMIZATION | choose q inside gates | OK |
| QF-076 | Validated Capacity | LOCKED DEFINITION | largest all-gates-valid q | OK |
| QF-077 | Sizing Search | LOCKED ALGORITHM | grid -> best region -> local refinement | SOURCE OK; Formula Index extraction incomplete—PASS11 |
| QF-078 | Multi-Opportunity Allocation | LOCKED OPTIMIZATION | joint RAEV under shared constraints | SOURCE OK; Formula Index output/input split malformed—PASS11 |
| QF-079 | Recovery Objective | LOCKED | best allowed post-exposure action | OK; both max-value and min-loss forms retained |
| QF-080 | Recovery Loss | LOCKED | post-Recovery loss excluding sunk loss | OK |
| QF-105 | Expected Idle Capital Cost | CALIBRATED | empirical opportunity cost | OK |
| QF-106 | Economic PnL global | LOCKED | component-preserving global economics | OK |
| QF-107 | Inventory Mark-to-Market | LOCKED | MTM excluding external flows | OK |
| QF-108 | Total Strategy PnL | LOCKED | strategy aggregate and global infra relation | SOURCE OK; Formula Index captures only second equality—PASS11 |

Direct consumer formulas additionally checked: QF-019/020 for OWA comparator/gain, QF-021–023 for Triangle boundary, and QF-104 Simulation Confidence as sizing evidence. No PASS07 formula was invented.
