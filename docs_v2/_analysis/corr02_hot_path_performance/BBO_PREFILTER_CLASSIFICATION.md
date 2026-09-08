# BBO Prefilter Classification

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

| Class | Name | May permanently reject? | May authorize/accept? | Required evidence |
|---|---|---:|---:|---|
| `BBO-C1` | `STATE_VALIDITY_GATE` | yes, under existing invalid/stale/incoherent state rules | no | canonical validity and reason parity |
| `BBO-C2` | `PROVEN_CONSERVATIVE_ECONOMIC_REJECTOR` | yes, only inside a proved domain | no | mathematical no-false-negative proof plus property/replay evidence |
| `BBO-C3` | `L1_EXACT_FASTPATH_ELIGIBILITY` | no; ineligible falls back | no; returns exact QF-016 only when eligible | exact fast/full result and trace parity |
| `BBO-C4` | `HEURISTIC_PRIORITY_OR_SCHEDULING_SIGNAL` | no | no | versioned scheduling policy, starvation/capture/replay analysis |

## Rules

- A favorable BBO value never proves executable edge.
- `q > L1 quantity` is not a route rejection. It means C3 is ineligible and canonical full L2 is required unless a separate C2 proof rejects.
- A heuristic, learned score, stale Atlas value or ranking never becomes C2 by naming it a bound.
- A scheduling change may affect which transient state is evaluated before expiry. It is therefore a semantic performance policy, not a transparent compute optimization.
- Every disposition records class, version, consumed state, quantity, reason and fallback/reject status.
