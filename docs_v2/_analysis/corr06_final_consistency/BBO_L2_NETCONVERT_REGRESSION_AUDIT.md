# BBO / L2 / NetConvert Regression Audit

| Rule | Result |
|---|---|
| BBO role = C1 state validity / C2 proved conservative reject / C3 FastL1 eligibility / C4 heuristic priority | PRESERVED |
| full L2 QF-016 NetConvert = canonical oracle | PRESERVED |
| FastL1 = exact specialization | PRESERVED |
| FastL1 ineligible → full L2 fallback | PRESERVED |
| `q > L1 capacity` alone rejects | NO |
| heuristic C4 permanently rejects | NO |
| `pair_to_routes` logical reverse dependency | PRESERVED |
| dense/contiguous indices | implementation detail only |

Profile and compiler A/B tests require exact DecisionTrace/economic parity unless a timing policy is intentionally versioned. Any FastL1/full-L2 economic divergence fails (`VP-007`). Regression count: `0`.
