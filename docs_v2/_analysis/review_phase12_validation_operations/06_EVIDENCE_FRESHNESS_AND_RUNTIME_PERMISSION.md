# Evidence Freshness and Runtime Permission

| Evidence condition | Runtime | Promotion | Demotion/review |
|---|---|---|---|
| FRESH | eligible for intersection | may support explicit review | continue monitoring |
| AGING | policy-dependent current scope only | no widening | schedule revalidation |
| REVALIDATION_REQUIRED | contract/restrict affected scope | blocked | obtain new evidence |
| STALE | affected claim unavailable | blocked | demote/disable as scoped |
| INVALID | fail closed for affected claim | blocked | immediate contraction and investigation |

These are mappings, not a new universal enum. Domain vocabulary prevails. Missing/unobservable mandatory evidence is not healthy. A valid manifest cannot override stale evidence; healthy recovery cannot auto-re-promote.
