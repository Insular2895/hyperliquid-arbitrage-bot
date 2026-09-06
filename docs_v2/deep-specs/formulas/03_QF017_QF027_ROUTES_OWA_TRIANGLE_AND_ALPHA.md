# QF-017–QF-027 — Routes, OWA, Triangle and Alpha

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| QF | Expression | Symbols / output unit | Preconditions | Failure semantics | Golden requirements |
|---|---|---|---|---|---|
| QF-017 | `D(q_A)=NC(A,B,q_A)` | A input; B output | valid direct leg and coherent state | propagate QF-016 failure | exact one-leg composition |
| QF-018 | `q_X=NC(A,X,q_A)`; `I(q_A)=NC(X,B,q_X)` | A→X→B, B output | route continuity; second input is exact net q_X | either leg invalid/residual/minimum failure invalidates route | sequential rounding; never feed gross/original amount |
| QF-019 | `Edge_OWA=I/D-1`; bps `×10^4` | dimensionless/bps | identical q_A, terminal B, state policy, fees/precision; D>0 | missing comparator or D≤0 → invalid | equal outputs→0; positive/negative; zero D rejects |
| QF-020 | `Gain_B=I-D` | B | same comparator contract | invalid D/I propagates | aligned outputs and sign |
| QF-021 | `q_X=NC(A,X,q_A)`; `q_B=NC(X,B,q_X)`; `q'_A=NC(B,A,q_B)` | returns A | closed legal path; every previous output valid | any leg failure invalidates cycle; residual exposure explicit | three legs with rounding/fees at each boundary |
| QF-022 | `R_triangle=q'_A/q_A-1` | dimensionless | QF-021 valid; q_A>0 | open path/zero input invalid | return-to-start, 0/positive/negative |
| QF-023 | `PnL_A=q'_A-q_A` | A | QF-021 valid | invalid cycle propagates | sign and A-unit equality |
| QF-024 | `ConversionAlpha=Output_Indirect,TT/Output_Direct,T-1` | ratio | same q/terminal asset/state; positive direct output | denominator≤0 or incomparable modes invalid | isolate route effect with like-for-like fixtures |
| QF-025 | `ExecutionAlpha_MT=Output_Indirect,MT/Output_Indirect,TT-1` | ratio | same indirect route/input/state; TT output>0 | different route/state or denominator≤0 invalid | isolate execution mode only |
| QF-026 | `E:q↦E(q)` from repeated exact simulation | edge unit by size | valid discrete size grid and complete simulation | invalid point remains invalid; no interpolation/monotonic fill | depth breaks, minimums and rounding discontinuities |
| QF-027 | `Q_profitable=sup{q:E(q)≥E_min}` | input-size unit | QF-026 evaluated on valid quantities; calibrated E_min | empty feasible set → no profitable size; unbounded/not sampled not invented | threshold equality, disjoint regions, empty set |

Direct, indirect and triangular results are economic outputs, not execution permission. QF-027 is profitability capacity, distinct from QF-076 validated capacity and QF-075 optimal size.
