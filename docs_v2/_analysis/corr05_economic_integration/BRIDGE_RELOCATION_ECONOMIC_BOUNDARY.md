# Bridge and Relocation Economic Boundary

Bridge/relocation is a distinct capital action, never an OWA route leg or hidden Strategy ExecutionEV outcome.

- QF-070 computes `BridgeCost = V_start - V_end^net + RiskCost(P)` using sequential NetConvert; per-step fees are not repeated.
- QF-071 uses `(BridgeCost + ExpectedExitCost) / E[PnL_cycle]`; a non-positive denominator means never break even.
- QF-072 uses `EV_destination - EV_stay - BridgeCost - ExpectedExitCost - RelocationRiskCost`.

`EV_stay` is mandatory opportunity cost. ExpectedExitCost remains separate in QF-071/QF-072 because canonical QF-070 does not include it. Expanding BridgeCost ad hoc would create duplication and is forbidden without formula change control. Bridge PnL reconciles in its own action bucket.
