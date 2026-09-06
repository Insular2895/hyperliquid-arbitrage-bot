# QF-028–QF-043 — Microstructure, Volatility and Liquidity

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| QF | Expression | Symbols / output unit | Preconditions | Failure semantics | Golden requirements |
|---|---|---|---|---|---|
| QF-028 | `(Q_bid-Q_ask)/(Q_bid+Q_ask)` | base/base→ratio | aligned BBO sizes ≥0; denominator>0 | both zero → invalid | balanced 0, bid-heavy +, ask-heavy -, both zero |
| QF-029 | `(ΣwQ^b-ΣwQ^a)/(ΣwQ^b+ΣwQ^a)` | ratio | aligned K; weights/nonnegative sizes; denominator>0 | missing level/weights or zero denominator invalid | single-level parity and weighted multi-level |
| QF-030 | `1[P^b_n≥P^b_{n-1}]Q^b_n-1[P^b_n≤P^b_{n-1}]Q^b_{n-1}` | base | ordered event pair, valid bid states | gap/reorder/invalid BBO → invalid | price up/down/equal; equality activates both terms |
| QF-031 | `1[P^a_n≤P^a_{n-1}]Q^a_n-1[P^a_n≥P^a_{n-1}]Q^a_{n-1}` | base | ordered event pair, valid ask states | gap/reorder/invalid BBO → invalid | price down/up/equal; equality activates both terms |
| QF-032 | `OFI_n=e^b_n-e^a_n`; `OFI_W=ΣOFI_n` | base | QF-030/031 valid, declared ordered W | invalid contribution/window → invalid; snapshots labelled proxy | bid/ask events, cancellation, exact sum, proxy label |
| QF-033 | `MLOFI=Σ_kw_kOFI^(k)` | weighted base | valid level OFIs, calibrated/versioned weights | schema/weight mismatch invalid | one/multi-level and weight-version change |
| QF-034 | `(AskQ_bid+BidQ_ask)/(Q_bid+Q_ask)` | price | coherent BBO; sizes≥0; positive denominator | both zero/invalid price → invalid | balanced→Mid; dominant bid/ask direction |
| QF-035 | `(MicroPrice-Mid)/Mid`; bps `×10^4` | ratio/bps | QF-001/034 valid; Mid>0 | invalid dependency/zero Mid → invalid | at Mid 0; positive/negative sign |
| QF-036 | `ln(P_t/P_{t-1})` | dimensionless | explicit reference series/time order; both prices>0 | missing/nonpositive/out-of-order → invalid | equal→0; known ratio; reference identity |
| QF-037 | `Σ_{t∈W}r_t²` | dimensionless² | valid returns; declared nonempty W | empty/gapped invalid unless explicit quality policy | zero returns; multi-return exact reference |
| QF-038 | `sqrt(RV_W)` | dimensionless | QF-037 valid and ≥0 | negative/invalid RV → invalid | zero/positive; no implicit annualization |
| QF-039 | `abs(r_t)/(σ_fast,t+ε)` | ratio | valid r/scale; σ≥0; ε>0 | nonfinite/invalid parameter → invalid | zero r; zero σ with ε; symmetry ±r |
| QF-040 | `Notional(q)/DepthQuote(δ)` | ratio | same side/book/band; depth>0 | zero depth means reject/conceptual +∞, not stored Inf | positive case, zero depth reject, side mismatch |
| QF-041 | `Notional(q)/ExecutedVolume_W` | ratio | aligned market/window; positive volume | zero-volume source behavior unspecified: typed invalid/open | normal; zero volume invalid; window mismatch |
| QF-042 | BUY `(VWAP-Mid0)/Mid0`; SELL `(Mid0-VWAP)/Mid0` | ratio | valid walk/VWAP; Mid0>0; declared side | zero Mid/invalid walk invalid | flat/cost/favorable each side |
| QF-043 | `(D_t-D_s)/(D_0-D_s)` | ratio | aligned depth definition/times; D0≠Ds | zero denominator source-unspecified: typed invalid/open | 0 immediately after, 1 recovered, >1 raw; display clamp |

True OFI requires ordered changes. A snapshot delta may be retained as a reduced-fidelity proxy but cannot satisfy the QF-030–032 event contract. Mechanical impact (QF-042) and future resilience (QF-043) are separate and must not be conflated.
