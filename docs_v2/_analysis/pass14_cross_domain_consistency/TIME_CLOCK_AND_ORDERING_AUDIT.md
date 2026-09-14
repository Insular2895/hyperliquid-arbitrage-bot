# Time, Clock and Ordering Audit

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Concept | Authority/use | Forbidden use | Result |
|---|---|---|---|
| exchange time | source-asserted market chronology, optional | local knowledge order or trusted elapsed time | PASS |
| receive wall clock | logs/cross-machine comparison with clock quality | elapsed latency without uncertainty | PASS |
| receive monotonic ns | local elapsed time, timers, latency | cross-machine absolute ordering | PASS |
| `recorder_seq` | definitive captured local order in one fixed context | global cross-recorder truth without merge policy | PASS |
| canonical local order | ascending assigned `recorder_seq`; Phase 08 correction | post-assignment timestamp/priority reorder | PASS |
| `ReplayClock` | advances by recorded/logical schedule and preserves relative durations | host wall time | PASS |
| `TestClock` | explicit deterministic test time | hidden sleep/scheduler time | PASS |
| `TimerEvent` | ordered strategic timeout/expiry/recheck evidence | implicit background timer mutation | PASS |
| worker completion | version-tagged result only | state commit order | PASS |
| model availability time | point-in-time artifact eligibility | today’s model in historical truth | PASS |
| training split | `training_end < validation_start` | random temporal leakage | PASS |
| Atlas/config/fee/metadata time | exact effective version at decision T | completed future aggregate/rule | PASS |

No-lookahead rule: no event, rule, config, model, formula/schema or feature unavailable at decision time T can affect historical-truth Replay. A later model on old data is permitted only as declared `COUNTERFACTUAL_MODEL`. Cross-recorder merging remains a versioned implementation policy; until chosen, no false total order is claimed.

Ordering inconsistencies after the Phase 08 superseding clarification: **0**. Hidden wall-clock/RNG paths authorized: **0**.
