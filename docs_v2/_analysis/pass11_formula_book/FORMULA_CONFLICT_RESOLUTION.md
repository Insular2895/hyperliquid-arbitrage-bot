# Formula Conflict Resolution

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

Only actual divergent claims are conflicts; missing detail is recorded in the gap/open registers.

| Conflict | Topic | Earlier claim | SRC-004 closure | Resolution |
|---|---|---|---|---|
| FC-001 | NetConvert fees | common simplification `output×(1-fee)` | actual fee debit asset and asset deltas govern; only B-debit has the shown subtraction | simplification superseded |
| FC-002 | insufficient book depth | legacy says QF-009 walk itself is invalid | source equations define filled quantity; route/full-fill consumers must decide residual acceptability | preserve partial walk result, fail full-fill route separately |
| FC-003 | survival from hazard | legacy QF-046 uses `Π_{j<k}` | source exact equation `Π_{j=1}^k(1-h_j)` | source indexing wins; new golden vector guards it |
| FC-004 | QF-099 status | index says LOCKED; legacy says review | no formal status label, but fixed calibration equation/context | `SOURCE_DERIVED_FROM_CONTEXT` |
| FC-005 | OOD status | index says LOCKED | source says MODEL DEPENDENT | `MODEL DEPENDENT`; only nonnegative/higher-worse contract fixed |
| FC-006 | confidence | index says LOCKED as if formula | source explicitly rejects a fixed weighted score and defines separate gates/categories | gated categorical contract retained |
| FC-007 | accounting statuses | index says LOCKED source-explicit for QF-106–110 | sections contain equations but no formal bold status | `SOURCE_DERIVED_FROM_CONTEXT` provenance |

## Actively inspected topics with no source conflict

OWA uses indirect/direct executable output; ConversionAlpha and ExecutionAlpha isolate route versus mode; OFI indicator/equality signs and microprice dislocation match SRC-004; JumpScore uses absolute return over robust scale plus epsilon; QF-049 imposes no exponential decay; capture is `E_L[S(L)]`; maker fill survival differs from edge survival; ES retains the robust quantile integral; RAEV has three explicit penalties and no repeated execution costs; stranded/bridge/relocation terms are explicit; sizing, Q_validated and Recovery objectives remain distinct; infra ROI/gate require positive/like-for-like denominators/evidence; global/strategy PnL and drawdown preserve separate identities.

Conflicts found: `7`; resolved: `7`; remaining: `0`. Open estimator/invalid-case choices are not falsely counted as source conflicts.
