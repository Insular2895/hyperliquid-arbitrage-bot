# Sign Convention Constitution

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Quantity | Positive means | Negative means | Zero | Enforced QFs |
|---|---|---|---|---|
| Spread | valid width | invalid crossed state | locked/equal BBO | 002,003 |
| OWA/alpha/return/gain | indirect/MT/cycle advantage | disadvantage | parity | 019–025 |
| BUY/SELL slippage | execution cost | price improvement | no BBO slippage | 012,013 |
| mechanical impact | cost on either side | favorable movement | no measured impact | 042 |
| OFI/MLOFI | bid-side pressure under exact indicator definition | ask-side pressure | balance | 030–033 |
| micro dislocation | microprice above mid | below mid | at mid | 035 |
| return/edge/PnL/EV/RAEV | favorable gain/value | unfavorable | break even | 036,049,056–063 |
| adverse selection BUY/SELL | unfavorable post-fill movement | favorable | flat future mid | 054,055 |
| Loss | economic loss | profitable outcome | flat | 060–062 |
| inventory deviation/flow | above target/inflow | below target/outflow | target/net flat | 064,067 |
| penalties/costs/drawdown | burden/degradation | only if identity naturally permits; otherwise invalid | none | 065,068–072,080,105,109,110 |
| correction | edge corrected | edge expanded | no correction | 082 |
| incremental infra value | candidate improves | candidate worsens | parity | 086–091 |
| PnL prediction error | realized PnL above forecast | forecast overestimated PnL | calibrated mean | 097 |
| slippage error | execution cost underestimated | cost overestimated | exact | 098 |
| fill calibration error | more fills than predicted | fill probability overpredicted | calibrated bucket | 099 |
| OOD/disagreement | farther/more disagreement | prohibited | in-support agreement may be zero | 102,103 |

Side conventions are never inferred from a generic sign: B→Q walks bids; Q→B walks asks. BUY/SELL formulas retain distinct references. Percent, fraction and bps are labelled so scaling cannot change a sign or magnitude silently.
