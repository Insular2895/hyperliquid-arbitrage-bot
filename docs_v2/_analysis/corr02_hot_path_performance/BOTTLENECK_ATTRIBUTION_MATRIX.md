# Bottleneck Attribution Matrix

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

| Signal | Plausible cause | Disambiguating evidence | First hypothesis class |
|---|---|---|---|
| high evaluations/event | reverse-index fan-out, duplicate membership, activation | route degree, unique tuple count, HWC mix | eliminate work |
| high full-L2/survivor ratio | weak C2 bounds or low C3 eligibility | filter confusion matrix, depth/fee reasons | safe classification/specialization |
| high cycles and instructions | arithmetic/branches/repeated validation | per-symbol samples and retired instructions | algorithm/specialization |
| low IPC + cache misses | pointer chasing/data layout/working set | PMU cache evidence, structure A/B | locality/layout |
| branch misses | unpredictable classification/walk | per-branch samples, workload stratification | branch/layout only after measurement |
| allocator activity | per-event containers/clones/growth | alloc count/bytes/call sites/capacity growth | preallocate/reuse/borrow |
| context switches/scheduler delay | oversubscription, blocking, wakeups | perf sched, runqueue and queue wait | topology/bounded handoff |
| queue wait/full | slow consumer/burst/capacity | producer/consumer service distributions | work reduction/backpressure |
| stale worker output | long compute or rapid version churn | age, versions, cancellation timing | dirty generation/cancel |
| page faults | cold memory/growth/mapping | minor/major faults and phase | warm-up/capacity/layout |
| local win, no end-to-end win | Amdahl/measurement overhead/other stage | CORR-01 stage delta | stop or retarget |
| latency win, worse capture | changed scheduling/filter false negatives | funnel cohorts and Replay divergence | reject semantic change |

Correlation is not attribution. Each promotion report states competing explanations, negative evidence and whether the effect reproduces across representative regimes.
