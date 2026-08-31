# Superseded Candidates

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Candidate | Prior direction | Replacing direction | Source authority / review pass |
|---|---|---|---|
| SUP-001 | Generic/full graph expensive scan in hot path | Precomputed affected routes + HOT/WARM/COLD | Later architecture; PASS 08 |
| SUP-002 | Python live core | Rust production/replay core; Python research | Later explicit direction; PASS 13 |
| SUP-003 | Blind market orders | Protected IOC/FOK/limits | SRC-004 execution; PASS 04 |
| SUP-004 | Blind order retry | Query/reconcile before retry | SRC-004/005; PASS 04/05 |
| SUP-005 | Fixed/static fees | FeeEngine + exchange/account fee inputs | Formula/Data closure; PASS 08/11 |
| SUP-006 | OWA without direct comparator | Bridge/capital relocation | Later routing refinement; PASS 07/08 |
| SUP-007 | 40–50 € as production sizing | Micro-live calibration probe only | SRC-006 validation; PASS 07/10 |
| SUP-008 | Naive equal order slicing | Slicing conditioned on replenishment/survival/risk | Formula/model refinements; PASS 04/08 |
| SUP-009 | Node required day one | Public feed first, node-compatible | SRC-008 + SRC-006; PASS 01 |
| SUP-010 | Premium/multi-server initial infrastructure | One cheap VPS/client; upgrade by ROI | SRC-008; PASS 01 |
| SUP-011 | Capital increase automatically upgrades infra | Recoverable PnL + LCB ROI gate | SRC-008/QF-091; PASS 01 |
| SUP-012 | Ping/bandwidth/marketing selects VPS | 12 benchmarks + economic validation | SRC-008/SRC-006; PASS 01 |
| SUP-013 | Recorder/cloud writes in hot path | Asynchronous non-blocking Recorder/local buffer | SRC-005/006; PASS 06 |
| SUP-014 | Central SaaS execution plane | Client-local isolated Docker | SRC-006; PASS 09 |
| SUP-015 | PnL global permits local risk violation | Risk hierarchy cannot be bypassed | SRC-005; PASS 05 |
| SUP-016 | Exact synthetic agents as production truth | Aggregate response/survival model | SRC-007/008; PASS 02/03 |
