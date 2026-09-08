# BBO, L1 and L2 Evaluation

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

QF-016 remains the only economic conversion authority. BBO logic has four disjoint roles:

| Class | Role | Outcome |
|---|---|---|
| `BBO-C1` | state validity | existing canonical invalid reason |
| `BBO-C2` | proved conservative economic rejector | permanent reject only inside proved domain |
| `BBO-C3` | exact L1 specialization eligibility | FastL1 or full-L2 fallback |
| `BBO-C4` | heuristic priority/scheduling | never permanent economic reject |

A C2 proof states direction, q, BBO price/size, fees and debit asset, quantization/minima, protected limits, comparator, bound and whether deeper levels can overturn it. Its universal obligation is `reject → exact full-L2 cannot be acceptable`. Existing C1 rules are safe; CORR-02 does not promote a new complete route-level C2 predicate. Unknown cases run full L2.

Best-price unlimited fill is an optimistic gross bound for a single directed walk because deeper prices cannot improve on the correct best side. Fees, rebates, debit assets, minima, precision and sequential leg transformations prevent treating that observation as an automatic net route proof. OWA needs a compatible indirect upper bound and direct executable lower/comparator value for the same q/state. Triangle composition needs monotonic transforms and exact start-asset closure.

`q` exceeding L1 quantity means C3 is ineligible, never that the route is invalid. FastL1 specializes traversal only when the complete legal conversion fits at the best level. Quote→Base eligibility derives the quantized base and quote spend under all rules; naive `quote <= price × quantity` is insufficient.

FastL1 returns the exact full QF-016 result/reasons/versions or returns only `FALLBACK_REQUIRED`. Full-L2 is the oracle across both directions, fee assets/rebates, minima, rounding, protection and boundary quantities. See the [classification](../../_analysis/corr02_hot_path_performance/BBO_PREFILTER_CLASSIFICATION.md), [safe-bound analysis](../../_analysis/corr02_hot_path_performance/BBO_SAFE_BOUND_ANALYSIS.md) and [parity contract](../../_analysis/corr02_hot_path_performance/NETCONVERT_FAST_FULL_PARITY_CONTRACT.md).
