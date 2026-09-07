# QF-064–QF-080 — Inventory, Bridge, Sizing, Allocation and Recovery

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

| QF | Expression | Symbols / output unit | Preconditions | Failure semantics | Golden requirements |
|---|---|---|---|---|---|
| QF-064 | `z_a=(I_a-I_a*)/B_a` | ratio | asset-aligned actual/target/band; B_a>0 | zero/negative band invalid; normalization policy open | target→0, ±deviation, zero band reject |
| QF-065 | `Penalty_a=κ_az_a²` | numeraire | valid z; κ≥0 calibrated; soft band | invalid parameter/unit invalid; cannot replace hard gate | symmetry, κ=0, increasing magnitude |
| QF-066 | reject if future inventory outside `[HardMin,HardMax]` | boolean | exact projected post-action inventory/reservations | unknown/breach rejects new risk | exact boundaries pass, below/above reject |
| QF-067 | `NetFlow_a(W)=ΣΔI_a` | asset unit | ordered actual trade deltas, declared W | missing/duplicate/unreconciled event invalid | inflow/outflow/net-zero and window boundary |
| QF-068 | `CurrentValue(X)-BestExecutableExitValue(X)` | numeraire | point-in-time valuation and executable QF-016 exit | missing/stale/invalid exit → unavailable/conservative lock | zero-cost, depth/fee/rounding exit |
| QF-069 | `ExpectedExitCost+ExpectedIdleCost+ExpectedRiskCost` | numeraire | distinct aligned expected components and calibrated structure | component overlap/unit mismatch invalid | isolate each component and aggregate once |
| QF-070 | `V_start-V_end^net+RiskCost(P)` | numeraire | valid bridge path, sequential NC, same valuation time/numeraire | invalid path/exit/risk evidence → no bridge | zero-cost, conversion loss, risk cost, no double fee |
| QF-071 | `(BridgeCost+ExpectedExitCost)/E[PnL_cycle]` | cycles | numerator aligned; expected cycle PnL>0 | denominator≤0 → conceptual ∞/never break even | positive, zero and negative denominator |
| QF-072 | `EV_destination-EV_stay-BridgeCost-ExpectedExitCost-RelocationRiskCost` | numeraire | common horizon/state/numeraire; disjoint costs | incomparable/invalid terms → STAY/no new risk | value ±/0; threshold/hysteresis boundaries |
| QF-073 | `ActualBalance_a-ReservedBalance_a≥0` | asset unit | reconciled actual/reservations | negative is invariant violation/UNKNOWN capital lock | exact zero, positive, negative reject |
| QF-074 | `ObservedCapacity_j-ReservedCapacity_j` | leg input unit | same leg/book/version/side; coherent reservations | negative/stale capacity rejects | zero/positive/negative and concurrent reservation |
| QF-075 | `q*=argmax_qRAEV(q)` under balance/book/impact/ES/P+/confidence/hard-inventory gates | size | valid discrete candidates and every gate | empty feasible set→no action; tie deterministic | feasible/infeasible, discontinuous objective, tie-break |
| QF-076 | `Q_validated=sup{q:Gates(q)=TRUE}` | size | exact evidence/capability tuple; evaluated valid quantities | empty set→no validated capacity; no extrapolation | boundary equality, holes, empty set |
| QF-077 | valid grid → best region → local refinement | size/algorithm | deterministic grid/order/tie policy and evaluation budget | invalid evaluation remains invalid; no gradient assumption | discontinuity, local region, repeat determinism |
| QF-078 | `max_qΣ_iRAEV_i(q_i)` subject to `Aq≤b` | numeraire objective, vector sizes | aligned objectives and shared constraints | infeasible/solver uncertainty fails closed; solver choice open | shared-capacity contention and deterministic tie |
| QF-079 | `argmax_aE[PortfolioValue_after(a)∣CurrentState]` = `argmin ExpectedRecoveryLoss(a)` | action/objective numeraire | actual current exposure/state; legal risk-reducing actions | no safe action → contain/reconcile; never restart counterfactual from flat | current-state actions, sunk-cost exclusion |
| QF-080 | `PortfolioValue_beforeRecovery-PortfolioValue_afterRecovery` | numeraire | consistent before/after valuation and action boundary | missing valuation/account mismatch invalid | no change 0; worse positive; sunk prior loss excluded |

QF-064–080 separate soft preference, constitutional hard limits, physical capacity, evidence-backed validated capacity and recovery. A recursive definition in which InventoryPenalty depends on the final size that it is itself selecting is prohibited; each candidate `q` produces a candidate post-state and penalty before comparison.
