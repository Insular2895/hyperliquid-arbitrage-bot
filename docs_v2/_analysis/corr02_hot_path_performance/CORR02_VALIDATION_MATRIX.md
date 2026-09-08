# CORR-02 Validation Matrix

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

`U` Unit, `G` Golden, `P` Property/Fuzz, `R` Replay, `Perf` controlled performance, `S` Shadow, `M` Micro-live, `E` economic/capture evidence.

| Optimization/contract | U | G | P | R | Perf | S | M | E | Promotion blocker |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---|
| BBO C1 validity | yes | yes | yes | yes | yes | as applicable | no new need | no | reason/state mismatch |
| BBO C2 rejector | yes | yes | yes | yes | yes | yes | after normal gates | yes | any false negative or unproved domain |
| FastL1 eligibility/result | yes | yes | yes | yes | yes | yes | after normal gates | yes | any full-L2/result/trace difference |
| reverse-index representation | yes | no | yes | yes | yes | yes | no direct need | if capture scheduling changes | missing/duplicate/nondeterministic dependency |
| dense ID mapping | yes | no | yes | yes | yes | as applicable | no | no | failed round-trip, width or generation mix |
| exact-tuple dedup | yes | no | yes | yes | yes | yes | no direct need | yes | distinct input lost or DecisionTrace change |
| dirty/cancellation | yes | no | yes | yes | yes | yes | after normal gates | yes | unique state skipped/reordered |
| preallocation/reuse | yes | yes | yes | yes | yes | yes | no direct need | yes | stale data, truncation or changed failure |
| bounded/lock-free queue | yes | no | yes/model | yes | yes/stress | yes | after normal gates | yes | loss/reorder/duplicate/overflow/shutdown defect |
| compiler/LTO/PGO | yes | yes | yes | yes | yes | yes | after normal gates | yes | semantic, portability or held-out regression |
| future C++ kernel | yes/ABI | yes | yes/fuzz/sanitizer | yes | yes incl. FFI | yes | never direct | yes | any gate/parity/fault-containment failure |

## Cross-cutting assertions

- Semantic parity is assessed before performance results.
- C2 is property-tested over its full declared valid state domain against full L2.
- Fast eligible equals full; fast ineligible falls back.
- `pair_to_routes` has every dependency exactly once, includes comparator edges and invalidates deterministically.
- Reuse retains results, reasons, versions and failure semantics and is poison-tested.
- Transparent changes preserve `DecisionTrace`; scheduling changes declare a versioned semantic policy and require capture/economic comparison.
- Safety, state consistency, existing exposure and Risk always outrank performance.
