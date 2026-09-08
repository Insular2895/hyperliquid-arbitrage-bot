# Performance Benchmark Matrix

DOCUMENTATION STATUS: BENCHMARK SPECIFICATION — NO RESULTS YET

`—` means not yet measured. All rows use the profiling protocol and report counts plus P50/P95/P99/P99.9, max and dispersion in their result artifact.

| Candidate | Hypothesis | Semantic change? (YES/NO) | Correctness oracle | Workload | Input distribution | P50 | P95 | P99 | P99.9 | CPU cycles | Instructions | Cache misses | Branch misses | Alloc count | Allocated bytes | Memory footprint | Build complexity | Runtime complexity | Replay parity | Downstream capture metric | Economic evidence required? | Promotion status |
|---|---|---:|---|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---|---|---|---:|---|
| baseline route lookup | reference cost | NO | logical reverse-index contract | affected-route lookup | real degree; direct/OWA/triangle; HWC | — | — | — | — | — | — | — | — | — | — | — | low | baseline | baseline hash | evaluations/event | YES if scheduling/capture changes | `BASELINE_REQUIRED` |
| dense route lookup | locality lowers lookup/scan cost | NO | canonical ID/member/order parity | affected-route lookup and rebuild | same plus topology churn | — | — | — | — | — | — | — | — | — | — | — | medium | low | exact required | evaluations/event | NO if transparent; YES for production value | `CANDIDATE` |
| BBO current prefilter | establish filter cost/quality | NO | full L2 | C1–C4 classification | all dispositions by route/q/regime | — | — | — | — | — | — | — | — | — | — | — | low | low | exact | full-L2 ratio/false negatives | YES | `BASELINE_REQUIRED` |
| BBO conservative bounds | safely reject more losers | NO | full L2 + proof | route C2 classification | fee/rule/direction/size boundaries | — | — | — | — | — | — | — | — | — | — | — | medium | medium | exact | survivors and missed-opportunity audit | YES | `PROOF_REQUIRED` |
| full L2 NetConvert | semantic oracle cost | NO | QF-016 golden/full | exact directed conversion | both sides, depth/fees/minima/q | — | — | — | — | — | — | — | — | — | — | — | low | baseline | canonical | exact-leg duration | NO, baseline | `ORACLE` |
| L1 specialized NetConvert | avoid irrelevant traversal | NO | full L2 exact equality | exact directed conversion | eligible/ineligible/boundary mix | — | — | — | — | — | — | — | — | — | — | — | medium | low | exact required | NetConvert stage/capture | YES | `CANDIDATE` |
| route dedup | remove same-tuple work | NO | evaluate unique tuples in order | route evaluation dispatch | duplicates/collisions/distinct versions | — | — | — | — | — | — | — | — | — | — | — | medium | medium | exact required | avoided work/evaluations | YES | `CANDIDATE` |
| dirty generation | cancel stale work sooner | NO unless scheduling changes | ordered baseline | worker dispatch/cancel | burst/churn/wrap/stale workers | — | — | — | — | — | — | — | — | — | — | — | medium | medium | exact required | stale ratio/tails | YES | `CANDIDATE` |
| HashMap vs contiguous index | locality beats hashing | NO | lookup membership/order | reverse dependency lookup | realistic graph/degree | — | — | — | — | — | — | — | — | — | — | — | medium | low | exact | lookup duration | NO if transparent | `CANDIDATE` |
| allocation-heavy vs scratch | reuse reduces allocator cost | NO | result/trace/failure parity | normalize/evaluate/record | steady, burst, growth/OOM | — | — | — | — | — | — | — | — | — | — | — | medium | medium | exact | stage tails | YES | `CANDIDATE` |
| copy vs reuse | fewer bytes improve locality | NO | ownership/result parity | payload/route/result transfer | size and lifetime mix | — | — | — | — | — | — | — | — | — | — | — | medium | medium | exact | stage tails | YES | `CANDIDATE` |
| current channel vs bounded queue | lower queue wait/contention | NO if order/loss identical | ordered queue contract | producer/consumer handoff | normal/burst/full/shutdown | — | — | — | — | — | — | — | — | — | — | — | medium | high | exact required | queue wait/drop/capture | YES | `EVIDENCE_GATE` |
| compiler LTO variants | codegen improves runtime | NO | same binary semantics/golden | full component + macro suite | complete representative regimes | — | — | — | — | — | — | — | — | — | — | — | medium/high | unchanged | exact | end-to-end stages | YES | `CANDIDATE` |
| PGO candidate | representative profile improves layout | NO | non-PGO release oracle | full component + macro suite | diverse training + held-out workloads | — | — | — | — | — | — | — | — | — | — | — | high | unchanged | exact | end-to-end stages | YES | `CANDIDATE` |
| Rust vs future C++ pure kernel | foreign kernel materially wins net of FFI | NO | Rust oracle | same bounded kernel with FFI | bounded bytes/data and edge cases | — | — | — | — | — | — | — | — | — | — | — | very high | medium | exact required | end-to-end/capture | YES | `NOT ELIGIBLE YET` |

## BBO quality measures

Each BBO row additionally reports disposition counts, C2 rejection rate, C3 eligibility/fallback, full-L2 survivor rate, false-negative count against the oracle (must be zero for C2), false-positive/work-waste rate and distribution by q/direction/fee/rule/route family. Filter speed without quality is incomplete evidence.
