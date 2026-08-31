# Initial Open Items

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

OPEN signifie décision réellement non prise. Les paramètres simplement calibrés restent `CALIBRATED`.

| Open ID | Item | Why open | Review pass |
|---|---|---|---|
| OPEN-001 | Final VPS provider and measured ranking | Requires controlled benchmark | PASS 01 |
| OPEN-002 | Final region if Tokyo is not empirically best/currently supported | Requires current external validation + benchmark | PASS 01 |
| OPEN-003 | Docker bridge vs host networking | Isolation/performance tradeoff not measured | PASS 01/09 |
| OPEN-004 | Exact infrastructure health thresholds/windows | Requires distributions and risk calibration | PASS 01/05/10 |
| OPEN-005 | Exact SF/alpha/LCB method for infra ROI | Formula structure fixed; values/method not | PASS 01/11 |
| OPEN-006 | Future node activation | Requires spot capability, reliability and ROI evidence | PASS 01 |
| OPEN-007 | Exact risk thresholds/CVaR limits | Strategy/data calibration required | PASS 05 |
| OPEN-008 | Exact model coefficients and champion variants | Requires training/OOS evidence | PASS 02/03/08 |
| OPEN-009 | Inventory penalties and bands | Requires data/validated capacity | PASS 07 |
| OPEN-010 | Exact survival model parameters | Learned from episodes | PASS 02 |
| OPEN-011 | Final retention and storage capacities | Requires measured recorder throughput | PASS 06 |
| OPEN-012 | Final maker/TM/MM activation | Architecture supports; evidence absent | PASS 02/04/10 |
| OPEN-013 | Cross-exchange activation/product scope | Explicitly future | future pass |
| OPEN-014 | Final license provider/mechanism | Deployment contract fixed, vendor open | PASS 09 |
| OPEN-015 | Final telemetry/export backend | Operations contract fixed, backend open | PASS 10 |

## PASS 01 — Infrastructure disposition

| Open ID | PASS 01 status | Evidence still required |
|---|---|---|
| OPEN-001 | `REMAINS OPEN` | Controlled benchmark of current, revalidated offers |
| OPEN-002 | `REMAINS OPEN` | Current platform availability plus region comparison; Tokyo remains first direction |
| OPEN-003 | `REMAINS OPEN` | Native/bridge/host performance evidence plus security review |
| OPEN-004 | `REMAINS OPEN` | Valid distributions, Risk calibration, windows and hysteresis |
| OPEN-005 | `REMAINS OPEN` | Validated `alpha`, safety factor and LCB method |
| OPEN-006 | `FUTURE GATE / OPEN` | Current node capabilities, public-feed limitation, reliability and ROI |
| OPEN-011 | `REMAINS OPEN; PASS 06 OWNER` | Measured Recorder throughput and retention/archive objectives |
| OPEN-015 | `REMAINS OPEN; PASS 10 OWNER` | Operations telemetry/export decision |

PASS 01 did not convert calibrated values into open architecture decisions. See `pass01_infrastructure/PASS01_FINAL_REPORT.md`.
