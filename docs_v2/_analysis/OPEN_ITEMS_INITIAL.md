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

## PASS 05 — Risk disposition

| Open ID | PASS 05 status | Evidence still required |
|---|---|---|
| OPEN-004 | `REMAINS OPEN; INFRA/RISK CO-OWNER` | Measured feed/clock/network/compute/recorder distributions, false-trigger cost and hysteresis validation for health states. |
| OPEN-007 | `REMAINS OPEN; RISK OWNER` | Exact spread/impact/participation/P+/CVaR/loss/recovery/drawdown/TTL and related limits by scope, with replay/shadow/micro-live evidence. |
| OPEN-008 | `REMAINS OPEN; PARTICIPANTS/VALIDATION OWNER` | Promoted models, support domains, OOD/confidence/disagreement and fallback evidence consumed by Risk. |
| OPEN-009 | `REMAINS OPEN; PASS 07 OWNER` | Exact inventory targets/bands/penalties, concentration, transit/stranded and portfolio capacity values. |
| OPEN-010 | `REMAINS OPEN; PARTICIPANTS OWNER` | Survival parameters/horizons used in arrival gates and `TTL_risk`. |
| OPEN-012 | `REMAINS OPEN; EXECUTION/RISK/VALIDATION CO-OWNER` | Explicit maker/MT/MTT/TM/MM activation, size limits and queue/adverse/recovery micro-live evidence. |

PASS 05 creates no new architectural open item. Exact numeric thresholds are evidence-governed calibrated policies; the four identified Data schema encodings remain cross-domain closure work rather than guessed Risk decisions.

## PASS 06 — Data / Recorder / Replay disposition

| Open ID | PASS 06 status | Evidence still required |
|---|---|---|
| OPEN-004 | `REMAINS OPEN; INFRA/RISK CO-OWNER` | Clock/Recorder/disk/backlog health distributions and fail-safe thresholds |
| OPEN-008 | `REMAINS OPEN; PARTICIPANTS/VALIDATION OWNER` | Exact promoted model artifacts/support consumed by RunManifest and Replay |
| OPEN-009 | `REMAINS OPEN; PASS 07 OWNER` | Full Inventory/Capital state contracts and checkpoint materialization details |
| OPEN-011 | `REMAINS OPEN; DATA/INFRA/OPERATIONS CO-OWNER` | Measured volume, final local capacity, archive provider and retention durations |
| OPEN-015 | `REMAINS OPEN; OPERATIONS OWNER` | Telemetry/export backend for data-quality and incident evidence |

Calibrated rather than architectural-open: RAW binary codec, 5–15-minute example chunk duration, queue capacities, disk watermarks, trade/incident window lengths, checkpoint cadence, partition sizes, checksum algorithm, source-priority table and cross-recorder merge policy. PASS 06 creates no new irreversible architecture decision.

## PASS 07 — Inventory / Capital disposition

| Open ID | PASS 07 status | Evidence still required |
|---|---|---|
| OPEN-007 | `REMAINS OPEN; RISK OWNER` | Exact P+/CVaR/impact/participation/capital-at-risk limits used by the feasible size region |
| OPEN-008 | `REMAINS OPEN; PARTICIPANTS/VALIDATION OWNER` | Promoted forecast models/support that influence Q_validated and capital utility |
| OPEN-009 | `REMAINS OPEN; PASS07 CALIBRATION OWNER` | Asset classifications, targets, soft/hard bands, NetFlow windows, penalty/stranded parameters, Bridge threshold/hysteresis/cooldown, search grid and allocation limits |
| OPEN-010 | `REMAINS OPEN; PARTICIPANTS OWNER` | Survival horizons/parameters used for future opportunity value and slicing |
| OPEN-012 | `REMAINS OPEN; EXECUTION/RISK/VALIDATION CO-OWNER` | MT/MTT/TM/MM activation and size support |

PASS07 closes the architecture and ownership boundaries, not numeric policy. It creates no new irreversible decision. The PASS00 `REQ-RISK-0301` OPEN keyword remains an indexed prior-domain item; PASS07 does not decide participant-address data collection policy.

## PASS 08 — Graph / Routes / Atlas / Quant disposition

| Open ID | PASS 08 status | Evidence still required |
|---|---|---|
| OPEN-004 | `REMAINS OPEN; INFRA/RISK CO-OWNER` | freshness/skew/compute budgets used by route state consistency |
| OPEN-007 | `REMAINS OPEN; RISK OWNER` | spread/depth/volatility/jump/impact and route-level Risk limits |
| OPEN-008 | `REMAINS OPEN; PARTICIPANTS/VALIDATION OWNER` | promoted survival/replenishment/response/competition models consumed by Atlas |
| OPEN-009 | `REMAINS OPEN; PASS07 CALIBRATION OWNER` | capital reachability/Bridge/terminal parameters informing HWC |
| OPEN-010 | `REMAINS OPEN; PARTICIPANTS OWNER` | survival/correction horizons and episode parameters |
| OPEN-012 | `REMAINS OPEN; EXECUTION/RISK/VALIDATION CO-OWNER` | MT/MTT mode capability and size support |
| OPEN-016 | `OPEN; PASS08/VALIDATION OWNER` | exact HWC thresholds, hysteresis, Atlas horizons/score components/support minima and route-activation compute budgets |

PASS08 closes architecture and semantic ownership, not numeric calibration. It creates no new irreversible execution decision. Formula rendering/unit audit remains PASS11 work; current exchange facts are external revalidation rather than guessed open constants.

## PASS 09 — Deployment / Security disposition

| Open ID | PASS 09 status | Evidence or decision still required |
|---|---|---|
| OPEN-003 | `REMAINS OPEN; INFRA/SECURITY CO-OWNER` | Docker bridge versus host-mode latency evidence plus attack-surface review |
| OPEN-004 | `REMAINS OPEN; INFRA/RISK OWNER` | CPU/memory/disk/clock/restart health thresholds and hysteresis |
| OPEN-011 | `REMAINS OPEN; DATA/INFRA/OPERATIONS CO-OWNER` | Volume capacity, backup/restore target and retention values |
| OPEN-014 | `REMAINS OPEN; COMMERCIAL/SECURITY OWNER` | License provider/mechanism, grace duration, binding and revocation delivery |
| OPEN-015 | `REMAINS OPEN; OPERATIONS OWNER` | Telemetry/export backend and client-consent implementation |
| OPEN-016 | `REMAINS OPEN; VALIDATION OWNER` | Capability evidence thresholds affected by release/deployment changes |

Additional calibrated/tool choices—base image/linkage, registry, SBOM/signing/scanner, UID/seccomp/resource profile, exact CLI aliases/exit numbers and support-bundle tooling—are not promoted into irreversible architecture decisions. PASS09 creates no new permanent open ID.

## PASS 10 — Validation / Operations disposition

| Open ID | PASS 10 status | Evidence or decision still required |
|---|---|---|
| OPEN-004 | `REMAINS OPEN; INFRA/RISK/OPERATIONS` | measured health distributions, thresholds, hold/recovery hysteresis and safe-action validation |
| OPEN-007 | `REMAINS OPEN; RISK` | exact risk/tail/TTL/Recovery limits with Replay/Shadow/Micro-live evidence |
| OPEN-008 | `REMAINS OPEN; PARTICIPANTS/VALIDATION` | exact Champion/Challenger artifacts, temporal OOS/calibration/economics/OOD/runtime evidence |
| OPEN-009 | `REMAINS OPEN; INVENTORY/CAPITAL` | exact bands, penalties, q search/allocation limits and promoted size scopes |
| OPEN-010 | `REMAINS OPEN; PARTICIPANTS` | survival horizons/parameters and drift criteria |
| OPEN-011 | `REMAINS OPEN; DATA/INFRA/OPERATIONS` | capacity, incident pinning, restore objectives and retention/archive durations |
| OPEN-012 | `REMAINS OPEN; EXECUTION/RISK/VALIDATION` | explicit MT/MTT/TM/MM activation and supported size/market evidence |
| OPEN-014 | `REMAINS OPEN; COMMERCIAL/SECURITY` | license mechanism/current service behavior and tested outage/revocation path |
| OPEN-015 | `REMAINS OPEN; OPERATIONS` | telemetry, dashboard, paging/export backend and per-client consent model |
| OPEN-016 | `REMAINS OPEN; VALIDATION` | HWC/Atlas/support thresholds and evidence/sample sufficiency by capability |

Additional calibrated choices: SLO targets/error budgets, alert thresholds/windows/routing/response objectives, operational calendar, evidence retention, fault-injection tooling, metric names/labels, command implementation and EvidenceId/CapabilityManifest serialized storage. PASS10 creates no irreversible project decision and no new permanent open ID.
