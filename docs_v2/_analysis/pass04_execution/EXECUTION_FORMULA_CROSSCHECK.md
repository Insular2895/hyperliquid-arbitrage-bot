# PASS 04 — Execution Formula Crosscheck

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

Formula authority remains SRC-004 Formula Book / PASS 11. PASS 04 checked names, statuses, locators, and consumption; it does not rewrite equations.

| QF | Canonical name | Execution use | Owner/status | PASS 04 result |
|---|---|---|---|---|
| QF-007 | Hyperliquid Size Quantization | intent `size_lots`, partial/downstream sizing | Formula; `LOCKED` | referenced; exchange parameters external |
| QF-008 | Hyperliquid Price Validity | protected `price_ticks` | Formula; `LOCKED` | referenced; current rules external |
| QF-009/010 | Book Walk Base→Quote / Quote→Base | expected/arrival execution quantities | Formula; `LOCKED` | no generic slippage substitute |
| QF-011 | VWAP | actual fill aggregation | Formula; `LOCKED` | actual fills only |
| QF-012/013 | Mechanical Slippage BUY/SELL | expected/actual execution deviation | Formula; `LOCKED` | protected limits remain separate guards |
| QF-014/015 | Fee Rate / Fee Amount | intent forecast and actual fill fees | Formula; `LOCKED` | actual fee evidence wins |
| QF-016 | NetConvert | actual leg output/downstream quantity | Formula; `LOCKED` | fees/rounding included |
| QF-024 | Conversion Alpha | route economics input | Formula; `LOCKED` | no duplicate expression |
| QF-025 | Execution Alpha | execution-method advantage | Formula; `LOCKED` | canonical overlay retained |
| QF-026/027 | Edge Curve / Maximum Profitable Size | plan size envelope/current revalidation | Formula; `LOCKED` | Sizing/Risk own final choice |
| QF-040 | Depth Participation | book/route capacity context | Formula; `LOCKED` | does not replace actual book walk |
| QF-041/042 | Volume Participation / Mechanical Impact | support/capacity and price impact | Formula; `LOCKED` | book reservation avoids concurrent overcommit |
| QF-043 | Liquidity Resilience | maker/continuation/recovery state evolution | Formula; `LOCKED` | Participant forecast, not order truth |
| QF-044–050 | Survival/hazard/arrival edge/threshold probability | continuation, maker age, route timer | Formula; learned where indexed | Participants owns forecasts/parameters |
| QF-051–053 | Maker Fill Survival/CDF/Expected Fill Time | resting/partial/staleness decision | Formula; QF-051 learned, rest locked | consumed as forecast, not truth |
| QF-054/055 | Adverse Selection BUY/SELL | maker cancellation/continuation | Formula; `LOCKED` | side-specific |
| QF-056 | Expected Value | candidate outcome aggregation | Formula; `LOCKED` | probabilities mutually exclusive |
| QF-057 | Execution EV | TT/TTT/route execution comparison | Formula; `LOCKED` | current-state recomputation |
| QF-058 | MT EV | maker-triggered plan evaluation | Formula; `LOCKED` | partial fill handled explicitly |
| QF-063 | Risk-Adjusted EV | current continuation/recovery gate input | Formula; `CALIBRATED` | penalties not double-counted |
| QF-066 | Hard Inventory Gate | forbid invalid continuation/recovery | Inventory/Formula; `LOCKED` | PASS 07 owns bands |
| QF-073 | Available Balance | actual less reserved | Formula; `LOCKED` | reservation invariant |
| QF-074 | Available Book Capacity | observed less reserved depth | Formula; `LOCKED` | versioned book capacity |
| QF-076 | Validated Capacity | upper evidence-backed authority | Sizing/Formula; `LOCKED` | cannot be exceeded by mode |
| QF-078 | Multi-Opportunity Allocation | shared reservations/capital | Capital/Formula; `LOCKED` | single owner prevents double spend |
| QF-079 | Recovery Objective | best current/split exit selection | Recovery/Formula; `LOCKED` | original route has no privilege |
| QF-080 | Recovery Loss | loss from recovery-start state | Recovery/Accounting; `LOCKED` | sunk costs excluded from permission |
| QF-084 | Infrastructure Latency | arrival/ACK/transition distribution input | Infra/Formula; `LOCKED` | no magic timeout |
| QF-099 | Fill Calibration Error | predicted-versus-actual evidence | Validation/Formula; `LOCKED` | feeds maker/Simulator calibration |
| QF-104 | Simulation Confidence | authority reduction/rejection | Simulator/Formula; `LOCKED` | cannot authorize execution |
| QF-106–108 | Economic PnL / Inventory MTM / Total Strategy PnL | downstream accounting separation | Accounting/Formula; `LOCKED` | not redefined in Execution |

## Crosscheck result

- Required families checked: **QF-007–016, 024–027, 041–042, 044–058, 063, 079–080**.
- Additional explicit consumers checked: **QF-066, 073, 074, 076, 078, 084, 099, 104, 106–108**.
- Unique Formula IDs covered: **47**.
- Expression discrepancies found: **0**.
- PASS 11 flags: confirm detailed units/precision and status metadata for learned/calibrated formulas; revalidate external exchange parameters. No formula was modified.
