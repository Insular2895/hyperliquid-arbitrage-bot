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

## PASS 02 — Market Participants disposition

| Open ID | PASS 02 status | Evidence still required |
|---|---|---|
| OPEN-008 | `REMAINS OPEN` | Training data, temporal OOS calibration, EconomicLift, ModelValue, runtime/OOD/fallback evidence for exact Champion and Challenger variants |
| OPEN-010 | `REMAINS OPEN` | OpportunityEpisode corpus, censor-aware fit, supported horizons/strata and validation for exact survival/hazard parameters |
| OPEN-012 | `REMAINS OPEN; EXECUTION/RISK CO-OWNER` | Calibrated fill/adverse-selection, second-leg/recovery validation and explicit activation decision for maker/TM/MM |

Additional Participant parameters—feature windows/weights, sparse neighbours, response horizons, OOD/drift methods and promotion gates—are `CALIBRATED`/`LEARNED`; they are not converted into new open architecture questions. P4/P5 remain Research/Future rather than unresolved production requirements.

## PASS 03 — Counterfactual Simulator disposition

| Open ID | PASS 03 status | Simulator relevance / evidence still required |
|---|---|---|
| OPEN-004 | `REMAINS OPEN; INFRA/RISK OWNER` | Exact latency/health windows affect arrival support; measured distributions required. |
| OPEN-007 | `REMAINS OPEN; PASS 05 OWNER` | Exact CVaR/confidence/Risk limits remain unchosen. |
| OPEN-008 | `REMAINS OPEN; PARTICIPANTS/VALIDATION OWNER` | Exact response Champion/Challenger estimator and parameters require temporal OOS, calibration and economic evidence. |
| OPEN-010 | `REMAINS OPEN; PARTICIPANTS OWNER` | Survival horizons/parameters affect arrival and slicing scenarios. |
| OPEN-012 | `REMAINS OPEN; EXECUTION/RISK OWNER` | Maker/TM/MM activation needs queue/fill/adverse/recovery Micro-live evidence. |

No new architecture decision was left open by PASS 03. Rejoin thresholds/horizons, probabilistic queue allocation, scenario count, dependence method, size grid, response horizons, confidence thresholds and calibration tolerances are explicitly `CALIBRATED`/`LEARNED`, not promoted to permanent open architecture questions.

## PASS 04 — Execution disposition

| Open ID | PASS 04 status | Execution relevance / evidence still required |
|---|---|---|
| OPEN-004 | `REMAINS OPEN; INFRA/RISK OWNER` | ACK/feed/recovery/reconciliation health windows use measured distributions, not magic constants. |
| OPEN-007 | `REMAINS OPEN; PASS 05 OWNER` | Exact route/leg/order/Recovery Risk thresholds remain unchosen. |
| OPEN-008 | `REMAINS OPEN; PARTICIPANTS/VALIDATION OWNER` | Exact maker/continuation forecast Champion and coefficients need evidence. |
| OPEN-009 | `REMAINS OPEN; PASS 07 OWNER` | Dust tolerances, inventory bands and PendingIntermediateBuffer bounds require calibration. |
| OPEN-010 | `REMAINS OPEN; PARTICIPANTS OWNER` | Exact survival parameters affect maker age and continuation. |
| OPEN-012 | `REMAINS OPEN; EXECUTION/RISK/VALIDATION CO-OWNER` | MT/MTT activation and all TM/MM activation/capital authority require explicit decision plus queue/adverse/recovery evidence. |

No new architecture open item was created. DMS/API/nonce/precision semantics are external revalidation, while timeouts, buffer limits, retry/escalation counts and tolerances are calibrated policy parameters rather than hidden fixed defaults.
