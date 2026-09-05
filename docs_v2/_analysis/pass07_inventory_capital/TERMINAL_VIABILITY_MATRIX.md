# Terminal Viability Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Evaluation dimension | Input | Quantity-sensitive? | Owner | Result effect |
|---|---|---:|---|---|
| Hard inventory | Future inventory and hard bounds | Yes | Risk/QF-066 | Hard reject except strict risk reduction |
| Soft inventory | QF-064/065 | Yes | Inventory economics | Penalize/rank/downsize |
| Exit path | Allowed point-in-time route set | Yes | PASS08 interface | Reject unsupported terminal |
| Exit cost | Best executable exit | Yes | QF-068 | Economic cost/reject threshold |
| Exit liquidity | Books/Atlas support | Yes | PASS08/Simulator/Risk | Reject/downsize/OOD |
| Stranded risk | exit + idle + risk components | Yes | QF-069/Risk | Penalty or reject |
| Future utility | validated opportunities/capacity/capture | Yes | PASS08 Atlas interface | Destination value |
| Risk | volatility/concentration/tail/hard gates | Yes | PASS05 | Permission boundary |
| Model confidence | regime/size/horizon support | Yes | Simulator/Risk | Reduce/reject |
| Classification | `CORE_INVENTORY`/`TRANSIT`/`EXCLUDED` | State-dependent | Inventory | Allowed normal terminal or reject |
| Decision | coherent aggregation inside hard safe set | Yes | Capital/Risk | accept, reduced size, reject |

Threshold values are not invented. The matrix is evaluated at post-action state and point-in-time evidence.
