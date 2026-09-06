# Golden Vector Requirement Catalog

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Vector family | QFs | Required cases | Equality |
|---|---|---|---|
| GV-001 BBO | 001–003 | source 99/101→100,2,200 bps; locked/crossed/zero | exact when representable; typed failures exact |
| GV-002 depth | 004–006 | one/multi level, side/band exact boundary, empty/corrupt | ticks/lots exact |
| GV-003 precision | 007–008 | below/on/above lot; sig/decimal/integer price; stale rule | exact |
| GV-004 walks | 009–013 | each direction, source 402/4/100.5/50 bps, zero/partial/exhausted/wrong side | fills/residual exact; ratios tolerance |
| GV-005 fees/NC | 014–016 | taker/maker/rebate, fee in output/other asset, minimum/rounding, sequential leg | asset deltas/legal outputs exact |
| GV-006 routes | 017–027 | equal/positive/negative OWA, zero denominator, closed/open triangle, alpha isolation, discontinuous curve, empty max | outputs exact after quantization; ratios tolerance |
| GV-007 order-flow | 028–035 | imbalance endpoints/zero denom; OFI price up/down/equal; proxy label; microprice/dislocation | indicators/sums exact; ratios tolerance |
| GV-008 volatility/liquidity | 036–043 | log reference/positive prices, zero/known variance, epsilon, zero depth/volume, both sides, raw >1/zero denominator | validity exact; float tolerance |
| GV-009 survival | 044–050 | probabilities/range, hazard product 1..k, half-life crossing/no crossing, deterministic/discrete L, strict threshold | categories/censor exact; float tolerance |
| GV-010 maker | 051–055 | survival/CDF complement, tail truncation, BUY/SELL adverse/favorable/flat | complement/sign exact predicate |
| GV-011 EV/tail | 056–063 | mass/overlap, F/P/R/X one-hot/mixed, MT costs once, PnL zero strict, Loss sign, analytic/empirical VaR/ES, each RAEV penalty | mass/failure exact; float tolerance |
| GV-012 inventory/bridge | 064–074 | target ±/zero band; hard boundaries; flows; exit depth/fees; bridge zero/negative cycle EV; relocation; negative availability | exact gates/asset quantities |
| GV-013 sizing/recovery | 075–080 | feasible/infeasible/discontinuous/ties/shared resource; actual current state; sunk cost excluded | selected discrete sizes/actions exact |
| GV-014 participants | 081–083 | distribution direction/horizon; correction 0/1/>1/E0≤0; nonnegative hazard/global cause | predicates exact; floats tolerance |
| GV-015 infrastructure | 084–094 | latency stage sums; capture; like-for-like deltas; ΔCost≤0; strict LCB; ratio-of-sums; zero denominators; censoring | stages/gates/failures exact; floats tolerance |
| GV-016 calibration | 095–104 | perfect/worst scores; log clipping; error signs; fill buckets; comparable lift/value; ensemble permutation; OOD order; six-gate truth table | categories/ranges exact; floats tolerance |
| GV-017 accounting/drawdown | 105–110 | zero-factor idle cost; each PnL component; external-flow removal; reconciliation; new peak/trough/recovery/zero peak/empty interval | ledger equality exact; valuation floats toleranced |

Every QF has at least one normal vector and every implementation-critical QF has boundary/invalid vectors. A golden result includes its QF/FormulaVersion, units, arithmetic domain, exact/tolerance policy and expected error code. Rust and Python run the same serialized vector corpus.
