# PASS 12 — Experiment and Data Requirement Map

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

| Learning target | Required data | Earliest stage | Replay? | Shadow? | Micro-live / Live? | Label / source of truth | Bias risk | Consumer |
|---|---|---:|---|---|---|---|---|---|
| Opportunity frequency | Valid books, graph/routes, exact opportunity/reject episodes | 4 | Yes | Improves | No | Count per valid support interval; DecisionTrace | Missing/gapped data, selection | Atlas, strategy |
| `Edge(q)` | Point-in-time L2, fees, precision, route/formula versions | 4 | Yes | Yes | Actual calibration | Exact NetConvert curve | Stale/future metadata | Opportunity, Sizing |
| Survival | Opportunity birth/death/censor episodes, microstructure | 5 | Yes | Required for live regimes | No normally | QF-044–050 episode label | Right-censoring, selection | Participants, Simulator, Infra |
| Correction velocity | Synchronized route/market episodes and cause labels | 5 | Yes | Useful | No normally | QF-082 point-in-time response | Clock/cross-market leakage | Participants |
| Capture probability | Opportunity survival + decision/arrival/execution outcome | 7 | Counterfactual | Required | Required for actual | Captured before death under declared scope | Only-traded selection | Infra, strategy |
| Maker fill | Maker arrival/rest/cancel/trade/fill events with queue observability | 13 | Yes at declared fidelity | Required | Dedicated probes/Live needed | Fill by horizon, QF-051/052 | L2 queue ambiguity | Maker/MT |
| Time-to-fill | Same maker episode with censoring and clocks | 13 | Yes | Required | Needed for calibration | QF-053 | Unobserved priority/censoring | Maker/Simulator |
| Adverse selection | Fill plus subsequent point-in-time prices by horizon | 13 | Yes | Partial | Micro-live/Live | QF-054/055 conditional on fill | Survivorship/regime | Maker/Risk |
| Liquidity resilience | Shock/consumption, depth recovery, valid clocks | 6 | Yes | Required | Micro-live strengthens causal data | QF-043 recovery profile | Confounding historical flow | Participants/Simulator |
| Cross-market response | Synchronized markets, sparse neighborhood, shock time | 9 | Yes | Required | Optional calibration | QF-081–083 response label | Multiple testing/lookahead | Participants/F3 |
| Slippage | Arrival book, intent, actual fills, fees/precision | 8/10 | Predicted | Required prediction | Micro-live required actual | Actual minus predicted under stable IDs | Missing fills/arrival state | Simulator/Sizing/Risk |
| Recovery loss | Recovery-start state, allowed exits, fills, fees, terminal state | 10 | Yes | Scenario proof | Micro-live/Live actual | QF-080 from recovery start | Only successful recoveries | Risk/Execution |
| `Q_validated` | Size curves + all Risk/inventory/model/execution/ops gates | 10/11 | Candidate | Required | Required for real band | QF-076 current support | Extrapolation, capital bias | Sizing/Capital |
| Bridge break-even | Bridge cost, exit cost, future cycle PnL/utilization | 15/17 | Yes | Required | Separate probe/Live | QF-071 per decision horizon | Future leakage, transient edge | Bridge |
| Capital utility | Actual inventory/reservations, opportunity/capture/capacity/exit history | 15 | Yes | Required | Live strengthens | Supported opportunity value per capital-time | Idle/opportunity misattribution | Atlas/Portfolio/Bridge |
| `InfraLostPnL` | Same-event multi-host arrival/capture plus opportunity survival | 7/20 | Counterfactual | Required | Live evidence improves | QF-087/QF-088 attribution | Clock/provider selection | Infra |
| Prediction error | Predeclared forecast joined to actual outcome | 8/10 | For historical actuals | Produces forecasts | Micro-live/Live actual | QF-095–100 | Post-hoc buckets/missing joins | Validation/models |

## Permanent rules

- Historical decisions see only information available at T; Market Atlas, models, Sizing and Bridge obey PASS 06 no-lookahead.
- Every target declares support, missingness, censoring, units, versions and label definition.
- A complex model competes with the simplest adequate Champion under temporal OOS, calibration and `EconomicLift`.
- Failed, rejected and negative experiments remain in the research archive.
