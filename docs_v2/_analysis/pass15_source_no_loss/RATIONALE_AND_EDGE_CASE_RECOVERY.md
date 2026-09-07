# Rationale and Edge-Case Recovery

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| ID | Source | Category | Preserved meaning | Destination | PASS15 action |
|---|---|---|---|---|---|
| `RER-P15-001` | SRC-001:1127–1137 | implementation-important scenario branch | evidence and capacity must be sliced by TT/MT/TTT/MTT, not only size/latency/inventory | Execution §23; Validation/Simulator evidence | added explicit recovered trace; canonical semantics already full |
| `RER-P15-002` | SRC-003:643–646 | non-obvious Recorder rationale | production recording exists for reconstruction, predicted/actual comparison, regime/drift detection and offline point-in-time recalibration | Recorder §1; deep 09/10 | restored explicit four-purpose list |
| `RER-P15-003` | SRC-001:819–963 | rejection/fallback rationale | rejected runtime shortcuts retain their reasons; insufficient depth reduces size/rejects; V1 activates final architecture progressively | Architecture/Risk/Execution/Validation owners | seven recovered rows preserve choices and negative rules |
| `RER-P15-004` | SRC-001:3844–5255 | data lineage and failure rationale | immutable payload, point-in-time metadata/config, checkpoint-not-truth, gap marking, async archive and non-aggressive early retention prevent irrecoverable evidence loss | Data/Recorder/Replay deep specs | 32 recovered rows restore precise owners |
| `RER-P15-005` | SRC-002:165–804 | route/hot-path/negative-evidence rationale | amount simulation replaces headline multiplication; only affected routes receive heavy work; rejects and stage latencies are evidence, not noise | Graph/Architecture/Recorder/Operations | 20 recovered rows restore decision boundaries |
| `RER-P15-006` | SRC-002:3821–4991 | evidence-authority and calibration rationale | external history bootstraps but cannot validate execution; first-party ordered events, policy replay and venue measurement govern activation/relocation | Data/Recorder/Validation/Capital | 18 recovered rows restore authority and evidence paths |

Rationale/edge-case source concepts recovered: **22** (12 rationale; 10 failure-mode traces). New unmitigated safety-critical failure modes: **0**. Existing failure semantics were verified rather than re-created: no blind retry, cancel race, UNKNOWN, actual-fill-only, dust/buffer, split Recovery, fail-conservative data gaps, disk/backpressure, split brain and license-safe Recovery all remain explicit.
