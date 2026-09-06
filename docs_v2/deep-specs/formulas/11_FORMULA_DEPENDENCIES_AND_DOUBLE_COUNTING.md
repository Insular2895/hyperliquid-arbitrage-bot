# Formula Dependencies and Double Counting

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Dependency composition

```text
QF-001,002 -> QF-003
QF-004,005 -> QF-006,040
QF-007,008,009,010,014,015 -> QF-016
QF-016 -> QF-017,018,021,068,070
QF-017,018 -> QF-019,020,024,026 -> QF-027
QF-021 -> QF-022,023
QF-018 + execution mode -> QF-025
QF-028..033 + QF-001 -> QF-034,035
QF-036 -> QF-037 -> QF-038 -> QF-039
QF-009..013 -> QF-040,042; depth time series -> QF-043
QF-045 -> QF-046 -> QF-044,047,048
QF-044/048 + learned outcomes -> QF-049,050
QF-051 -> QF-052,053 -> QF-058
QF-054,055 -> adverse-cost evidence -> QF-058
QF-056 -> QF-057,058; QF-060 -> QF-061 -> QF-062
QF-057 + QF-065,069 + uncertainty -> QF-063
QF-064 -> QF-065; QF-066,073,074 -> QF-075,076,077,078
QF-068 + QF-105 -> QF-069; QF-016 -> QF-068,070
QF-070 -> QF-071,072; QF-079 -> QF-080
QF-081 -> QF-082; edge-death evidence -> QF-083
QF-084 + QF-044 -> QF-085; QF-086,087 -> QF-088,089,091
QF-090 -> QF-092; opportunity/PnL evidence -> QF-093,094
QF-095,096,099 -> calibration evidence; QF-097,098 -> prediction diagnostics
QF-090 -> QF-100; QF-084/100 -> QF-101; model outputs -> QF-102,103,104
QF-068/105 -> capital economics; QF-106,107,108 -> equity E_t -> QF-109 -> QF-110
```

The machine-readable/per-QF form is [FORMULA_DEPENDENCY_GRAPH](../../_analysis/pass11_formula_book/FORMULA_DEPENDENCY_GRAPH.md).

## First-entry cost ownership

| Cost / effect | First canonical entry | Downstream rule |
|---|---|---|
| walked spread/depth/slippage | QF-009/010 and QF-016 gross conversion | never subtract separate estimated slippage from that same realized/simulated walk |
| exchange fee | QF-014/015, applied by QF-016 | route outputs already include it; do not subtract in QF-019/020/022/023 |
| partial/failure/recovery scenario loss | QF-057 | QF-063 consumes EV once; do not add a second generic recovery deduction |
| MT adverse and recovery costs | QF-058 | include only if not already inside each `EV_leg2` outcome |
| inventory penalty | QF-065 into QF-063 | preference term; not actual PnL/MTM and not the QF-066 hard gate |
| exit/idle/risk stranded components | QF-068/QF-105 into QF-069 | QF-063 or relocation consumes the declared component once |
| bridge conversions | QF-016 within QF-070 | `V_end^net` already includes depth/fees/rounding |
| ExpectedExitCost in relocation | QF-072 | exclude it if already included in the chosen BridgeCost definition for that evaluation; evidence must show ownership |
| trading costs | QF-090 | GrossTradingPnL must exclude them; QF-106 components must reconcile without another subtraction |
| added model latency loss | QF-101 | must be disjoint from PnL_with/without and OperationalCost |
| infrastructure cost | QF-090/QF-106/QF-108 global close | subtract once at global EconomicPnL, never inside every route PnL and again globally |
| external cash flow | QF-107 | remove from MTM change; it is not trading PnL |

## Consumer boundaries

Formula Engine computes typed outputs but does not grant permission. Feature/Model/Simulator may estimate; Risk gates; Sizing selects among already computable candidates; Execution applies authorized intents; Accounting reconciles actual components. Predicted, counterfactual and realized values never share an unlabelled field. QF-063 is an objective, not realized accounting. QF-106/108 are accounting closure, not a sizing penalty.

## Recursive dependency guard

For candidate size `q`, compute projected inventory → QF-064 → QF-065, then QF-063(q), then compare candidates under QF-075. InventoryPenalty cannot depend on the final `q*` before candidates are evaluated. Shared QF-074 capacity is reserved atomically outside the pure formula result.
