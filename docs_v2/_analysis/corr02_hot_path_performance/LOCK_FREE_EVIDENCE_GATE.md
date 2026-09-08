# Lock-Free Evidence Gate

DOCUMENTATION STATUS: EVIDENCE-GATED CANDIDATE — AWAITING FINAL HUMAN REVIEW

Blocking, obstruction-free, lock-free, wait-free and bounded-time are distinct claims. No component is required to be lock-free by CORR-02.

A lock-free candidate advances only when all are shown:

1. the synchronization boundary is on the measured critical path;
2. wait/lock contention materially contributes to representative tail latency or loss;
3. work elimination, ownership simplification and layout/locality do not adequately solve it;
4. producer/consumer topology is explicit, preferring SPSC over MPMC when true;
5. capacity, priority, overflow, shutdown and backpressure semantics are safe;
6. ordering, loss, duplication, ABA, reclamation, false sharing and memory-order invariants are addressed;
7. stress/model-check/sanitizer/Miri-style evidence is available as applicable;
8. end-to-end Replay, capture and operational evidence beats the simpler champion.

Candidate boundaries are market-feed ingress, ordered-core handoff, Recorder handoff, immutable worker queues and low-priority metrics. A queue never owns economic state or weakens the single writer.

Custom unsafe lock-free code is last resort. A maintained safe abstraction is still not adopted without workload evidence and dependency/supply-chain review.
