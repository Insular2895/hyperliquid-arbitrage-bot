# CORR-02 Cross-Domain Change Map

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

| Domain | Change | Non-change / authority retained |
|---|---|---|
| Architecture | work-elimination doctrine, memory/single-writer/queue gates | no new component or state machine |
| Graph/Routes | BBO C1–C4, FastL1 eligibility, physical reverse-index candidates, exact dedup | route topology and canonical IDs unchanged |
| Formula | cross-reference only through QF-016 authority | zero new/changed QF; FormulaVersion unchanged |
| Data/Replay | generation-local dense index and complete input tuple | frozen schemas not expanded ad hoc; ordered truth unchanged |
| Recorder | bounded queue evidence gate | lock-free not mandatory; priority semantics unchanged |
| Infrastructure | CPU/work/allocation/copy/cache profiling protocol | no host/provider/kernel/container decision |
| Risk | parity and priority restated | no gate/threshold/authority change |
| Execution/Recovery/Accounting | C++ exclusions and single-writer preservation | no behavior or ownership change |
| Validation | correctness-before-performance evidence matrix | no direct Live promotion |
| Operations | low-cardinality performance signals | no unbounded labels or new backend |
| Roadmaps | optimization loop mapped to existing phases | no Phase 27; implementation unauthorized |
| Review/Audits | existing stale notice retained | PASS14/15 historical reports untouched; CORR-06 refreshes |

All new requirements are `HUMAN_POST_RECONSTRUCTION` (`HDC-007..019`). They are not retroactively attributed to SRC-001..008.
