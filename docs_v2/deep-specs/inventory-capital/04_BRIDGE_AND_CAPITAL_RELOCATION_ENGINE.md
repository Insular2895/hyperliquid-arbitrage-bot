# 04 — Bridge and Capital Relocation Engine

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Definition and boundary

A Bridge deliberately changes where capital lives to improve expected future utility. It is not automatically OWA. OWA requires a valid direct `A -> B` comparator for `A -> X -> B`; without it, the conversion is Bridge/Capital Relocation. Conversion Alpha measures current conversion efficiency; relocation value measures whether B is a better capital state than A.

## Decision pipeline

```text
CURRENT CAPITAL STATE
-> POINT-IN-TIME MARKET ATLAS / FORECAST
-> CANDIDATE DESTINATIONS
-> ALLOWED CANDIDATE PATHS
-> QF-070 BRIDGE COST
-> QF-068 EXPECTED EXIT COST
-> RELOCATION RISK
-> EV_destination versus EV_stay
-> QF-072 RELOCATION VALUE
-> HYSTERESIS / COOLDOWN / PERSISTENCE
-> RISK ELIGIBILITY
-> SHARED RESERVATION
-> EXECUTION
-> ACTUAL FILL-DERIVED CAPITAL STATE
-> OUTCOME EVIDENCE / CALIBRATION
```

PASS08 supplies candidate route/Atlas facts. Paths are evaluated economically through NetConvert and current executable state; fewest hops is not the objective.

## Canonical economics

- QF-070 `Bridge Cost` compares starting value with net destination value and adds path risk; NetConvert already incorporates fees/spread/slippage.
- QF-071 `Bridge Break-Even Cycles` amortizes Bridge plus expected exit cost using positive expected future cycle PnL; non-positive expected cycle PnL means infinity.
- QF-072 `Capital Relocation Value` compares `EV_destination` and `EV_stay`, then bridge, exit and relocation risk costs.

The exact QF expressions remain in SRC-004/Formula Index. Future cycle PnL is learned by regime and current evidence, not copied from a stale unconditional average. `STAY` is always valid unless a higher-priority safety action is required.

## Execution and evidence

Bridge uses the same balance, book and Risk reservations as other actions and competes with new opportunities for capital. It runs on a slower evidence horizon than hot-path opportunity execution. A partial or failed Bridge creates actual exposure and transitions to Execution/Recovery rules.

Record candidates and rejections, source/destination, path set, predicted bridge/exit/risk costs, destination/stay EV, threshold/hysteresis state, reservation, fills, actual costs, future opportunity utilization, break-even realization and later exit. Shadow evaluates both move and stay; Micro-live validates execution before material relocation.

Sources: SRC-001 Bridge experimental protocol; SRC-002 capital relocation sections; SRC-003 §§15–18 and recorder Bridge experiments; SRC-004 QF-016/QF-068/QF-070–072; SRC-005 §§72–74; SRC-006 §§93–96; SRC-007 §§65–68.
