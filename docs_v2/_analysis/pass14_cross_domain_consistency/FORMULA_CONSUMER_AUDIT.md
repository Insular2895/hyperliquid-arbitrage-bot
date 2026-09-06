# Formula Consumer Audit

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

PASS 14 rechecked the PASS11 110-row consumer matrix against canonical masters/deep specs. Every QF has one primary owner, at least one consumer, units/sign/preconditions and a version/evidence boundary.

| Range | Count | Primary output family | Main consumers | Cross-domain checks | Result |
|---|---:|---|---|---|---|
| QF-001–016 | 16 | BBO, depth, precision, walks, fees, `NetConvert` | Graph, Simulator, Risk, Execution, Accounting | bid/ask direction; partial walk vs full route; fee asset; no repeat cost | PASS; external rules gated |
| QF-017–027 | 11 | direct/indirect/Triangle/alpha/edge capacity | Route, Simulator, Risk, Sizer | comparator/terminal unit; QF-027 ≠ QF-076 | PASS |
| QF-028–043 | 16 | microstructure/liquidity features | Participants, Simulator, Risk, Atlas | reference/window/fidelity; mechanical vs response | PASS; QF-041/043 open invalid case |
| QF-044–055 | 12 | survival/capture/maker/adverse selection | Participants, Simulator, Infra, Execution | horizon/time origin, learned artifact, censoring | PASS; QF-047/053 estimator open |
| QF-056–063 | 8 | EV/outcome/Loss/VaR/ES/RAEV | Simulator, Risk, Sizer, Accounting | scenario mass, Loss sign, common numeraire, once-only penalties | PASS; empirical estimator open |
| QF-064–080 | 17 | inventory/Bridge/sizing/allocation/Recovery | Inventory, Capital, Risk, Sizer, Execution | hard vs soft, `Q_validated`, sunk cost, shared capacity | PASS; grid/solver choices open |
| QF-081–094 | 14 | cross-market/competition/infrastructure | Participants, Simulator, Infra, Accounting, Validation | rate/time units, aligned cohorts, non-overlap latency | PASS; LCB/diagnostic estimators open |
| QF-095–104 | 10 | calibration/model value/OOD/confidence | Models, Simulator, Risk, Validation | probability clipping, like-for-like cost, categorical confidence | PASS; epsilon open |
| QF-105–110 | 6 | idle cost/accounting/drawdown | Capital, Accounting, Risk, Ops | disjoint PnL, external flows, zero peak/nonempty interval | PASS; QF-109/110 invalid cases open |

Totals: **110 expected / 110 audited / 0 missing / 0 duplicate canonical definitions / 0 ownerless / 0 consumerless / 0 unresolved formula misuse**. `OPEN-017..028` remain implementation preconditions, not permission to guess.
