# QF-001–QF-016 — Pricing, Depth, Precision, Fees and NetConvert

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

Each row is an individual audit. “Invalid” means a typed non-value and fail-closed consumer behavior; it never means silently return zero.

| QF | Expression | Symbols / output unit | Preconditions | Failure semantics | Golden requirements |
|---|---|---|---|---|---|
| QF-001 | `Mid=(Bid+Ask)/2` | Bid/Ask/Mid: quote/base price | finite positive coherent BBO | missing/crossed/nonpositive BBO → invalid | 99/101→100; exact tick-compatible case |
| QF-002 | `Spread=Ask-Bid` | price | valid BBO | crossed/nonpositive state → invalid | 99/101→2; zero-spread boundary |
| QF-003 | `SpreadRel=Spread/Mid`; bps `=10^4×` | ratio; bps | QF-001/002 valid, Mid>0 | zero denominator → invalid | 2/100=.02→200 bps |
| QF-004 | `DepthBase_s(K)=Σ_{i=1}^Kq_i` | q: base; output base | side/order declared; K≥1; q≥0 | absent/corrupt level or insufficient requested K → invalid/explicit partial policy | one/multi/zero-size levels |
| QF-005 | `DepthQuote_s(K)=Σp_iq_i` | p quote/base, q base; quote | QF-004 conditions, p>0 | invalid level/overflow → invalid | exact ticks×lots and multiple levels |
| QF-006 | asks `Σ_{p_i≤Ask1(1+δ)}p_iq_i`; bids `Σ_{p_i≥Bid1(1-δ)}p_iq_i` | δ ratio; output quote | δ≥0; coherent BBO; side/band/version | invalid δ/BBO/level → invalid | δ=0, exact boundary inclusion, each side |
| QF-007 | `Δq=10^-d`; `q_valid=floor(q10^d)10^-d` | q base; d decimals | q finite ≥0; valid metadata d | metadata missing/overflow → invalid | below/exact/above lot; no round-up |
| QF-008 | max significant figures `5`; max decimals `8-szDecimals`; integer allowed | price→validity/legal price | current metadata/rule version; p>0 | illegal/unknown/stale rule → reject | significant/decimal boundary, integer, external fixtures |
| QF-009 | `x_i=min(q_remaining,q_i)`; `GrossQuote=Σx_ip_i`; `Σx_i=q_B^filled` | input/filled base; output quote | q≥0; ordered valid bids; protection bound | return explicit fill/residual; full-fill consumer rejects residual; never extrapolate | zero, partial, exact exhaustion, multi-level, insufficient depth |
| QF-010 | `x_i=min(q_i,Q_remaining/p_i)`; `Q_i=x_ip_i`; `GrossBase=Σx_i` | input/spent quote; output base | Q≥0; ordered positive asks; protection bound | explicit spent/residual/fill; invalid price or residual under full-fill gate rejects | source asks 100×2,101×3 and 402 spend→4 base; partial/depth |
| QF-011 | `VWAP=Σp_ix_i/Σx_i` | price | valid fills; Σx_i>0 | zero fill → typed undefined, no Mid substitute | source fills 2@100+2@101→100.5; zero fill |
| QF-012 | `(VWAP-Ask1)/Ask1`; bps `×10^4` | ratio/bps, positive cost | valid BUY VWAP; Ask1>0 | invalid side/reference/denominator → invalid | source 100.5 vs 100→50 bps; favorable negative case |
| QF-013 | `(Bid1-VWAP)/Bid1`; bps `×10^4` | ratio/bps, positive cost | valid SELL VWAP; Bid1>0 | invalid side/reference/denominator → invalid | flat, costly, favorable; side-symmetry sign |
| QF-014 | `f_market,mode=FeeEngine(account,market,mode,t)` | rate dimensionless | point-in-time account/market/mode evidence | missing/stale fee state → invalid; rebate `f<0` is valid | taker/maker/rebate/tier transition, external fixtures |
| QF-015 | `FeeValue=Notional×f` | explicit fee asset/numeraire | compatible notional, rate and debit-asset policy | unlabeled asset or overflow → invalid | positive fee, zero, rebate, alternate debit asset |
| QF-016 | `NC(A,B,q_A,S)=q_B^net`; B-debit case `Quantize_B(GrossConvert-FeeDebit_B)` | A input, B net output plus actual asset deltas | valid QF-007–010/014–015, minimums, state/version | any invalid leg, illegal quantization, insufficient required fill/minimum or unknown debit asset → invalid; residual explicit | B→Q/Q→B, fees in output/other asset, rebate, rounding/minimum, insufficient depth, sequential legs |

QF-016 owns conversion economics. Book-walk price effects and an included fee must not be subtracted again by routes, EV, RAEV or accounting. Its output is the actual legal net quantity in B under state `S`, accompanied by fill/residual and asset-delta evidence; it is not a generic scalar after-fee approximation.
