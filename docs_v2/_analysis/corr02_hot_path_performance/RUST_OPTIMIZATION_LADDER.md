# Rust Optimization Ladder

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

Advance one measured bottleneck at a time; later rungs do not bypass earlier correctness gates.

| Rung | Candidate action | Required evidence |
|---|---|---|
| `R0` | establish semantic/performance baseline | reproducible benchmark + CORR-01 endpoints |
| `R1` | eliminate unnecessary route/evaluation work | complete-input and DecisionTrace parity |
| `R2` | improve locality/data layout | cache/working-set evidence and logical parity |
| `R3` | eliminate avoidable allocation | allocation counts/bytes and reset safety |
| `R4` | eliminate avoidable copies/clones | lifetime/ownership proof and byte evidence |
| `R5` | preallocate/reuse bounded storage | capacity/fallback/stale-reuse tests |
| `R6` | exact special cases such as eligible FastL1 | full-oracle equality over broad state |
| `R7` | branch/representation tuning | profile evidence, maintainability review |
| `R8` | remove proven synchronization contention | lock-free evidence gate and stress/model proof |
| `R9` | compiler/profile variants | reproducible same-workload A/B and portability |
| `R10` | PGO; SIMD only when justified | representative training or vectorizable-kernel proof |
| `R11` | foreign-language candidate | full C++ escalation gate |

No blanket `inline(always)`, unchecked indexing, unsafe code, custom hasher, SIMD, atomics or allocator replacement is authorized. Dense indices may remove hashing rather than tune it. `Arc`/clone costs are measured before redesign.
