# Global Unit and Dimension Matrix

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

| QF ranges | Input dimensions | Output dimension | Dimensional proof / constraint | Result |
|---|---|---|---|---|
| 001–002 | price, price | price | only equal-price addition/subtraction | PASS |
| 003 | price/price | ratio,bps | bps is labelled `×10^4` scale | PASS |
| 004 | base quantities | base | homogeneous sum | PASS |
| 005–006 | price×base | quote | band predicates compare prices | PASS |
| 007–008 | base+decimal metadata; price+metadata | base; legal price | exact quantum/rule predicate | PASS; external rule |
| 009–011 | base×price, quote/price | quote/base/price | walk and VWAP cancel base correctly | PASS |
| 012–013 | price/price | ratio,bps | compatible side reference required | PASS |
| 014–016 | ratio×notional; asset conversions | rate,value,net asset | debit asset and economic conversion explicit | PASS; external fee rules |
| 017–025 | route asset outputs | asset/ratio | comparisons require same terminal asset | PASS |
| 026–027 | size→edge, edge threshold | curve/size | E and E_min same edge unit | PASS |
| 028–035 | base/base, price×base/base, price/price | ratios/prices | weighted sums require compatible weights | PASS |
| 036–039 | price ratio/log, squared ratio, ratio/ratio | ratio,ratio²,ratio | no implicit annualization | PASS |
| 040–043 | quote/quote; depth/depth | ratio | side/window/depth definition aligned | PASS; QF-041/043 zero rules open |
| 044–052 | probability/time distributions | probabilities/time | latency and survival share time unit/origin | PASS |
| 053 | probability×dt | time | tail/support convention required | PASS; estimator detail open |
| 054–055 | price/price | ratio | side-specific future reference | PASS |
| 056–063 | probability×PnL, Loss distribution, penalties | PnL/Loss numeraire | all scenarios/components one numeraire | PASS; empirical ES policy open |
| 064–067 | asset/asset; coefficient×ratio²; asset sums | ratio,numeraire,asset | B_a same asset and positive | PASS; zero B open |
| 068–072 | comparable values/costs | numeraire/cycles | same valuation numeraire/horizon | PASS |
| 073–078 | like asset/resource quantities | asset/vector/objective | matrix rows have typed resource units | PASS |
| 079–080 | portfolio values | action/loss numeraire | before/after same valuation | PASS |
| 081–085 | distributions, edge/edge, time sums | distribution/ratio/hazard/time/probability | named market/horizon and time units | PASS |
| 086–093 | like PnLs/costs | value/ratios | experimental cohorts and periods aligned | PASS; denominator rules explicit/open where source silent |
| 094–096 | counts/counts, probability errors/logs | ratios | labels and probabilities same event | PASS |
| 097–104 | like predictions/outcomes/costs | errors/value/score/category | no unitless confidence scalar invented | PASS |
| 105 | capital×value/(capital·time)×time | value | opportunity rate empirically dimensioned | PASS |
| 106–108 | disjoint values | numeraire | same period/currency; external flows removed | PASS |
| 109–110 | equity differences/ratio/max | equity/ratio | relative requires positive peak | PASS; zero peak/empty interval open |

No dimensionally contradictory source equation was found. Source omissions requiring policy closure are not dimensional contradictions: QF-041/043/064/061–062/109–110 invalid or estimator conventions remain typed open items.
