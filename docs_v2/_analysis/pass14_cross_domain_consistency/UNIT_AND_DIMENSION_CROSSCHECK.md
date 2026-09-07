# Unit and Dimension Crosscheck

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

PASS 11's 110/110 dimensional audit was rechecked at cross-domain consumption boundaries.

| Quantity family | Canonical unit | Producer→consumer boundary | Required guard | Result |
|---|---|---|---|---|
| price | quote/base; exchange boundary `price_ticks` | Book/Precision→Formula/Execution | metadata version and side | PASS |
| quantity | explicit asset/base; boundary `size_lots`/`quantity_lots` | Book/Inventory→Sizer/Execution | asset and lot quantum | PASS |
| notional/value/PnL/cost | explicit quote asset or declared numeraire | Formula/Simulator/Accounting→Risk/Ops | conversion timestamp/policy | PASS |
| fee rate | dimensionless | Fee→QF-014/Conversion | account/market/mode/time/version | PASS |
| fee amount | explicit debit/economic asset | QF-015→Inventory/Accounting | never infer debit asset | PASS, `EXT-003` gate |
| fraction/bps | dimensionless; `1 bp = 10^-4` | Formula→Risk/Ops | `_bps` label or explicit conversion | PASS |
| probability | `[0,1]` | Models/Simulator→Risk | event/horizon/support/version | PASS |
| latency/duration | one declared unit; internal elapsed ns | Clock/Infra→Simulator/Risk | monotonic clock, no mixed ms/ns | PASS |
| timestamp | exchange optional; receive wall; receive monotonic; Replay logical | Data→all | never subtract incompatible clocks | PASS |
| hazard | probability per bin or nonnegative rate/time as defined | Participants→Simulator | bin/horizon/unit | PASS |
| loss | same numeraire as PnL, `Loss = -PnL` | Simulator→Risk | upper positive tail | PASS |
| inventory deviation | dimensionless `z_a` | Inventory→Risk/Sizer | positive normalization band | PASS; `OPEN-020` |
| book capacity | leg input unit | Graph/Reservation→Sizer | observed minus reserved, same side/band | PASS |
| equity/drawdown | absolute numeraire; relative dimensionless | Accounting→Risk/Ops | peak > 0 for relative form | PASS; `OPEN-027` |
| ROI/efficiency | dimensionless ratios | Infra/Accounting→Validation | valid positive denominator | PASS; `OPEN-023/024` |

Unit/sign mismatches unresolved: **0**. Source-omitted denominator/estimator policies remain typed-invalid/open rather than silently returning zero.
