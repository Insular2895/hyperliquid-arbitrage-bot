# PASS07 Conflict Resolution

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| ID | Source evolution/conflict | Resolution | Authority | Remaining? |
|---|---|---|---|---:|
| IC-01 | Fixed inventory percentages vs dynamic bands | Examples remain non-binding; ordered bands are locked, values calibrated | SRC-005 §§62–65 | No |
| IC-02 | Any asset holdable vs three asset classes | `CORE_INVENTORY`, `TRANSIT`, `EXCLUDED`; class learned/versioned | SRC-003 §§20–23 + SRC-005 Data §37 | No |
| IC-03 | Profitable route implies acceptance vs Terminal Viability | Post-action terminal/exit/Risk can reject | SRC-003 §§24–33 + SRC-005 §§70–71 | No |
| IC-04 | OWA conflated with Bridge | OWA requires direct comparator; otherwise Bridge/relocation | SRC-003 §§15–18 | No |
| IC-05 | Fewest-hop Bridge vs economic path | Compare all allowed paths by relocation value/NetConvert | SRC-006 §§93–94 | No |
| IC-06 | Bridge fees only vs full economics | QF-070 plus QF-068 and relocation risk; no duplicate conversion costs | SRC-004 QF-068/070/072 | No |
| IC-07 | Move on one edge vs future evidence | Point-in-time destination utility and persistence required | SRC-002/003/007 + QF-072 | No |
| IC-08 | Move on every rank change vs hysteresis | Calibrated threshold, hysteresis, cooldown, persistence | SRC-005 §74 | No |
| IC-09 | Position Sizing conflated with Order Slicing | Exposure quantity first; child execution second | SRC-003 §§39–46 + SRC-006 §§78–86 | No |
| IC-10 | QF-027 max profitable vs `Q_validated` | QF-076 requires all gates, not profitability alone | SRC-004 | No |
| IC-11 | More capital implies larger size | Capital changes balance ceiling only; evidence controls capacity | SRC-005 §§149–152 | No |
| IC-12 | Independent route sizes vs shared resources | Joint reservations and QF-078 constraint matrix | SRC-003 §§45–47 + SRC-004 | No |
| IC-13 | Highest edge wins vs constrained portfolio | Allocate absolute RAEV curves inside constraints | QF-075/078 | No |
| IC-14 | Route-only PnL vs hierarchical PnL | Separate route/recovery/rebalance/inventory/Bridge/infra/global | QF-105–108 | No |
| IC-15 | Losing Rebalance hidden as OWA | Rebalance has separate purpose and accounting | SRC-003 §31/rebalance sections | No |
| IC-16 | Recovery treated as Rebalance/Bridge | Existing unwanted exposure invokes Recovery priority and QF-079/080 | SRC-004/005 | No |

Formula Index extraction defects for QF-056/057/064/066/071/077/078/108 are not semantic conflicts; they are PASS11 audit items recorded in `FORMULA_CROSSCHECK.md`.

## PASS00 heuristic status corrections

Closure already established by PASS04/PASS05 is retained: `REQ-RECON-0001`, `REQ-EXEC-0033`, `REQ-EXEC-0131`, `REQ-EXEC-0174`, `REQ-RISK-0111`, `REQ-RISK-0117`, `REQ-RISK-0134`, `REQ-RISK-0190`, `REQ-RISK-0202`, `REQ-RISK-0245` and `REQ-SURV-0015` are prescriptive closure/interface requirements, not OPEN/REJECTED/FUTURE dispositions. PASS07 routes them to `DEEP_SPEC` while their owning completed pass remains authoritative.

Direct source rereading also corrects obvious keyword false positives: `REQ-GRAPH-0006` routes to PASS08; `REQ-CAP-0009`, `REQ-CAP-0013` and `REQ-BRIDGE-0010` are canonical capital/terminal principles; `REQ-CLOCK-0003` and `REQ-RISK-0023` are positive cross-domain principles; `REQ-ACCT-0008` and `REQ-VALID-0014` are supporting research examples. The genuinely rejected approaches retained as `REJECTED` are `REQ-SLICE-0002` (simultaneous fixed fragmentation as fake depth) and `REQ-DEPLOY-0220` (the enumerated infrastructure anti-patterns). Original PASS00 status remains visible in the ledger.
