# Risk Formula Crosscheck

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

PASS 05 consumes but does not redefine Formula Book equations. SRC-004 QF entries and `docs_v2/_analysis/FORMULA_INDEX.md` remain authoritative; any earlier variant is subordinate and a formula change waits for PASS 11.

| Risk concept | Formula authority | Status | Risk use | Crosscheck result |
|---|---|---|---|---|
| Absolute/relative spread | `QF-002`/`QF-003`, SRC-004 3563–3640 | LOCKED | SpreadGate/economic support | Referenced, not copied |
| Cumulative/depth-within-band | `QF-004`–`QF-006`, 3651–3792 | LOCKED | Liquidity/capacity | Referenced, not copied |
| Realized volatility | `QF-038`, 5282–5298 | LOCKED | VolatilityGate | Estimator fixed; windows calibrated |
| Robust jump score | `QF-039`, 5299–5363 | LOCKED | JumpGate/outlier checks | Structure fixed; threshold calibrated |
| Depth participation | `QF-040`, 5364–5409 | LOCKED | Market/capacity gate | Bound calibrated |
| Volume participation | `QF-041`, 5410–5446 | LOCKED | Flow/size gate | Window/bound calibrated |
| Mechanical impact | `QF-042`, 5460–5515 | LOCKED | Impact/price protection | No participant-response double count |
| Survival/capture/arrival support | `QF-044`–`QF-050`, 5529–5861 | mixed LOCKED/LEARNED | Survival and expected-arrival gates | Model values learned; objects/aggregations authoritative |
| Execution PnL distribution | `QF-059`, 6246–6282 | LOCKED | `P(PnL>0)` gate | Probability threshold calibrated |
| Loss variable | `QF-060`, 6283–6313 | LOCKED | Tail-loss convention | Loss sign convention retained |
| VaR | `QF-061`, 6314–6342 | LOCKED | Diagnostic quantile | Never used alone as full tail bound |
| Expected Shortfall/CVaR | `QF-062`, 6343–6391 | LOCKED | Tail gate | Alpha/limit calibrated |
| Risk-adjusted EV | `QF-063`, 6392–6491 | CALIBRATED | Ranking inside safe set | Never converts hard failure into penalty |
| Normalized inventory deviation | `QF-064`, 6492–6517 | LOCKED | Soft/hard inventory inputs | Unit/target contract required |
| Soft inventory penalty | `QF-065`, 6518–6542 | CALIBRATED | Soft portfolio objective | Cannot replace hard gate |
| Hard inventory gate | `QF-066`, 6543–6589 | LOCKED | New-risk eligibility | Reducing exception classified separately |
| Net flow | `QF-067`, 6590–6622 | LOCKED | Accumulation guard | Windows/limits calibrated |
| Concentration/stranded capital | `QF-068`–`QF-069`, 6623–6763 | mixed | Portfolio/asset risk | Earlier variants do not override |
| Available balance/book capacity | `QF-073`–`QF-074`, 7004–7140 | LOCKED | Reservations/resources | Unknown stays unavailable |
| Position sizing objective | `QF-075`, 7141–7273 | LOCKED | Optimize within safe sizes | Hard gates applied before objective |
| Validated capacity | `QF-076`, 7274–7313 | LOCKED | Scaling/size ceiling | Capital cannot exceed evidence |
| Sizing search | `QF-077`, 7314–7342 | LOCKED | Final size | `q*=0` when no valid size |
| Portfolio allocation constraints | `QF-078`, 7343–7380 | LOCKED | Concurrent safe candidates | Shared resources aggregated once |
| Recovery objective/loss | `QF-079`–`QF-080`, 7381–7546 | LOCKED | Bounded exit choice/tail | Sunk costs and route loyalty excluded |
| Infrastructure latency | `QF-084`, 7660–7765 | LOCKED | Compute/network freshness and survival inputs | Health thresholds not defined by ROI |
| Infrastructure economic gate | `QF-085`–`QF-091`, 7766–8076 | mixed | Scaling/provider cross-link only | Does not authorize unsafe trading |
| Model disagreement | `QF-102`, 8702–8750 | LOCKED | DisagreementGate | Threshold/model set calibrated |
| OOD distance | `QF-103`, 8751–8781 | LOCKED structure | Hard/soft OOD | Representation/bounds model-specific |
| Simulation confidence | `QF-104`, 8782–8832 | LOCKED structure | SimulationGate | Required support/calibration provenance |
| Drawdown/max drawdown | `QF-109`–`QF-110`, 9148–9224 | LOCKED | Drawdown state inputs | State thresholds/hysteresis calibrated |

## Findings

1. No formula conflict requires a PASS 05 rewrite.
2. The Constitution's `CapitalAtRisk`, loss-window, quality and InfraHealth state policies are risk-policy objects; where no QF exists, PASS 05 does not manufacture one.
3. `RAEV` is an objective among safe actions. Treating a hard violation as a finite penalty would contradict SRC-005.
4. VaR is retained as a diagnostic; ES/CVaR and worst-loss constraints remain the tail authority.
5. Formula thresholds, units and estimator parameters awaiting evidence remain `CALIBRATED`/`LEARNED` or `OPEN-007`; exact formula transcription remains PASS 11.

Formula references checked: 30 concept groups covering all prompt-required families. Conflicts found: 0 formula-definition conflicts; boundary clarifications: 5.
