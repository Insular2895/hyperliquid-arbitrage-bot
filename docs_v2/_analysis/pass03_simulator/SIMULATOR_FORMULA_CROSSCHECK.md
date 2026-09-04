# PASS 03 — Simulator Formula Crosscheck

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

SRC-004 Formula Book sections were reopened. This pass references formulas; it does not alter or re-ID them. **42** QF entries were checked.

Explicit checked set: `QF-009`, `QF-010`, `QF-011`, `QF-012`, `QF-013`, `QF-014`, `QF-015`, `QF-016`, `QF-026`, `QF-027`, `QF-040`, `QF-041`, `QF-042`, `QF-043`, `QF-044`, `QF-045`, `QF-046`, `QF-047`, `QF-048`, `QF-049`, `QF-050`, `QF-051`, `QF-052`, `QF-053`, `QF-054`, `QF-055`, `QF-056`, `QF-057`, `QF-058`, `QF-059`, `QF-060`, `QF-061`, `QF-062`, `QF-063`, `QF-076`, `QF-079`, `QF-080`, `QF-081`, `QF-082`, `QF-084`, `QF-085`, `QF-104`.

| QF | Canonical role in Simulator | Status / PASS 03 check |
|---|---|---|
| QF-009 / 010 | Directional bid/ask book walk at arrival | `LOCKED`; partial quantity preserved. |
| QF-011 | VWAP over actually executed base; undefined at zero fill | `LOCKED`; PASS 00 summary saying undefined is a truncation artifact, not the formula. |
| QF-012 / 013 | Mechanical slippage versus Ask1/Bid1, adverse cost non-negative | `LOCKED`; not Market Response. |
| QF-014 / 015 | Dynamic historical fee rate and economic/asset fee amount | `LOCKED SOURCE/DYNAMIC VALUE`; never hardcode. |
| QF-016 | `NetConvert` with book, fees, precision, rules, execution mode | `LOCKED ARCHITECTURE`; same implementation all modes. |
| QF-026 / 027 | Empirical/discontinuous edge curve and maximum profitable size | `LOCKED`; not linear interpolation. |
| QF-040 / 041 | Depth and recent-volume participation | `LOCKED`; zero depth rejects; support/confidence inputs. |
| QF-042 | Mechanical Impact relative to pre-trade mid | `LOCKED`; distinct from BBO slippage and response. |
| QF-043 | Depth resiliency after shock | `LOCKED`; raw over-replenishment may be retained. |
| QF-044–050 | Edge survival/hazard/arrival/capture threshold | Structure/object locked; QF-045/049/050 learned. Inputs to arrival/scenarios, not full EV. |
| QF-051–053 | Maker fill survival, CDF, expected fill time | QF-051 learned; mappings/definitions locked. Queue observability disclosed. |
| QF-054 / 055 | Maker BUY/SELL adverse selection by horizon | `LOCKED`; positive means adverse. |
| QF-056 | EV over mutually exclusive scenarios | `LOCKED`; probabilities sum to one. |
| QF-057 | Execution EV across full/partial/recovery/failure | `LOCKED STRUCTURE`; no happy-path-only forecast. |
| QF-058 | MT EV integrates fill-time-conditioned second-leg value minus adverse/recovery costs | Locked structure, learned components. |
| QF-059 | Monte Carlo `P(PnL > 0)` | `LOCKED`. |
| QF-060 | `Loss = -PnL` | `LOCKED`; tail convention retained. |
| QF-061 | VaR as loss quantile | `LOCKED`; alpha set by Risk/config. |
| QF-062 | CVaR / Expected Shortfall | `LOCKED`; internal term `ExpectedShortfall` avoids convention ambiguity. |
| QF-063 | Risk-Adjusted EV | `CALIBRATED`; do not subtract fees/partial/recovery twice. |
| QF-076 | `Q_validated = sup{q: Gates(q)=TRUE}` | `LOCKED`; Simulator supplies size-dependent evidence, Sizing/Risk own gates. |
| QF-079 / 080 | Recovery objective and loss from recovery-start state | `LOCKED`; sunk costs excluded. |
| QF-081 | Conditional Cross-Market Response distribution | `LEARNED`; not a fixed matrix/coefficient. |
| QF-082 | Edge correction fraction/velocity over horizon | `LOCKED`; values above one allowed when edge crosses zero. |
| QF-084 | Total latency and compute decomposition | `LOCKED`; refines SRC-008 compact `t_arrival` equation. |
| QF-085 | Capture probability integrated over infrastructure latency | `LOCKED`; connects survival and latency. |
| QF-104 | Simulation Confidence gates | `LOCKED semantics`; explicitly rejects a fake fixed weighted score. |

## Discovered adjacent dependencies

QF-007/QF-008 (exchange size/price validity), QF-083 (Competition Hazard), QF-094–QF-096 (empirical survival/Brier/Log Loss), QF-097–QF-101 (prediction/slippage/fill/economic/model-value validation), and QF-102/QF-103 (disagreement/OOD) are adjacent dependencies. They are referenced by their owning Participant/Validation/Data docs, not duplicated into the mandatory 42 count.

## PASS 11 flags

1. PASS 00 `FORMULA_INDEX.md` has mechanically truncated expression summaries (notably QF-011); authoritative SRC-004 text is intact.
2. `World_cf = HistoricalBaseline + Δour + Δresponse` remains a conceptual decomposition, not a new QF.
3. Rejoin compatibility/threshold has no QF and remains calibrated; do not invent one.
4. Validate units and discretization for sampled/empirical model outputs in PASS 11/Data Contracts.

No mathematical contradiction was found among the authoritative sections used by PASS 03.
