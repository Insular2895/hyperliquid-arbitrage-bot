# Maturity Dependency and N/A Semantics

`NOT_APPLICABLE != FAILED != UNVALIDATED != LOW_MATURITY`. Exclusion from the numeric minimum requires a documented no-independent-economic-meaning rationale, substitute contract/integration evidence and reviewer authority. Otherwise the stage is applicable and missing evidence blocks promotion.

| Dependency | M1 | M2 | M3 | M4 | M5 | Rationale |
|---|---|---|---|---|---|---|
| parser/config loader | required | contract evidence | N/A candidate | N/A candidate | N/A candidate | later N/A only if semantic changes are fully exercised through consumers |
| pure deterministic formula | required | parity/Replay through consumers | N/A candidate | N/A candidate | N/A candidate | cannot independently emit effects |
| schema decoder | required | compatibility/Replay | N/A candidate | N/A candidate | N/A candidate | integration proof substitutes for independent live stage |
| Book/Risk/Execution Engine | required | required | required | required | required | decision/capital/effect bearing |
| Simulator/model | required | required | required | actual calibration applicable | supported Live monitoring applicable | affects sizing/permission |
| feed adapter/infra profile/deployment artifact | required | required | required | required when supporting real effects | required for promoted scope | can change live behavior |

Cells marked “N/A candidate” are not decided globally: the exact capability record must justify them. Target maturity is bounded by every applicable dependency requirement.
