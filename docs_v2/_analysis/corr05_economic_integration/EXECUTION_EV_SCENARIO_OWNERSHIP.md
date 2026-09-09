# ExecutionEV Scenario Ownership

QF-056 is the generic expectation `Σ_i p_i × PnL_i`. QF-057 instantiates the canonical resolved-attempt scenario partition F/P/R/X. Each scenario probability appears exactly once and its scenario PnL contains all economics caused by that path exactly once.

| Owner | Owns | Must not own again |
|---|---|---|
| Simulator | joint F/P/R/X probabilities and scenario PnL distribution | actual truth or Risk permission |
| Formula Engine | deterministic QF-056/QF-057 aggregation | a second completion discount |
| Risk | hard permission gates | conversion of hard gates into soft PnL penalties |
| Inventory/Capital | external QF-063 state penalties and capacity evidence | scenario fees/Recovery cashflows |
| Accounting | reconciled realized action buckets | predicted values as realized PnL |

`ExecutionEV` is not multiplied by a completion rate or survival score after this distribution is formed.
