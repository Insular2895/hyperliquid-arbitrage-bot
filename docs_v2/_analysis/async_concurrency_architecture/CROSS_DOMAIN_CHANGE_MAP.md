# Cross-Domain Change Map

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

| Domain/document | Integration | Semantic change |
|---|---|---:|
| Architecture 00 + deep spec 14 | C0–C5 classes, ordered acceptance, baseline/challenger topology | 0 to domain truth; new concurrency contract |
| Market Graph 03 | existing `pair_to_routes`, BBO/FastL1/full-L2 rules referenced | 0 |
| Formula Book 04 | QF-001–110 untouched; full L2 remains QF-016 oracle | 0 |
| Participants 06 / Simulator 07 | optional snapshot workers and supported fallback clarified | 0 |
| Inventory/Capital 08 | allocation/Reservation commit stays ordered and atomic | 0 |
| Risk 09 | final Risk stays current C0; stale ALLOW excluded | 0 |
| Execution 10 | actual-fill dependency and async effect return clarified | 0 |
| Data 11 | worker job/result provenance and scheduling independence | 0 to frozen structs; schema family requirement |
| Recorder/Replay 12 | background disk/checkpoint and concurrency Replay tests | 0 |
| Infrastructure 13 | I/O/CPU separation and two-vCPU oversubscription risk | 0 |
| Deployment 14 | one container/process and no remote hot-path dependency reaffirmed | 0 |
| Validation 16 | CT-001..015, queue/deadline/stale/failure gates | validation strengthening |
| Roadmap 17 | work mapped to existing Phases 1–20/26; no Phase 27 | 0 responsibilities; 26 phases |
| Operations 18 | queue/scheduler/stale/deadline/background metrics | monitoring strengthening |
| Journey 19 | baseline→profile→parallel challenger→Replay/Shadow/economics | 0 stages |
| HDC ledger | append only genuinely new human scheduling decisions | pending review |
| Review package | mark this extension as required pending evidence | no approval granted |

## Regression statement

Formula, Risk priority/gates, Execution transitions, `UNKNOWN`, no-blind-retry, Recovery, Reconciliation, BBO/L2/NetConvert, `Q_validated`, accounting and public-feed/node epistemic boundaries are unchanged. Implementation remains unauthorized.
