# Time, Clock and Ordering Audit

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Concept | Authority/use | Forbidden use | Result |
|---|---|---|---|
| exchange time | source-asserted market chronology, optional | local knowledge order or trusted elapsed time | PASS |
| receive wall clock | logs/cross-machine comparison with clock quality | elapsed latency without uncertainty | PASS |
| receive monotonic ns | local elapsed time, timers, latency | cross-machine absolute ordering | PASS |
| `recorder_seq` | final unique local capture tie-break | global cross-recorder truth without merge policy | PASS |
| canonical local order | `(recv_monotonic_ns, source_priority, recorder_seq)` | reordering dependent facts by older exchange timestamp | PASS |
| `ReplayClock` | advances by recorded/logical schedule and preserves relative durations | host wall time | PASS |
| `TestClock` | explicit deterministic test time | hidden sleep/scheduler time | PASS |
| `TimerEvent` | ordered strategic timeout/expiry/recheck evidence | implicit background timer mutation | PASS |
| worker completion | version-tagged result only | state commit order | PASS |
| model availability time | point-in-time artifact eligibility | today’s model in historical truth | PASS |
| training split | `training_end < validation_start` | random temporal leakage | PASS |
| Atlas/config/fee/metadata time | exact effective version at decision T | completed future aggregate/rule | PASS |

No-lookahead rule: no event, rule, config, model, formula/schema or feature unavailable at decision time T can affect historical-truth Replay. A later model on old data is permitted only as declared `COUNTERFACTUAL_MODEL`. Cross-recorder merging remains a versioned implementation policy; until chosen, no false total order is claimed.

Ordering inconsistencies: **0**. Hidden wall-clock/RNG paths authorized: **0**.
