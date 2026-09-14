# Timer Replay Ownership Matrix

| Mode | Risk/Maker/UNKNOWN/Reconcile timers | Metrics flush |
|---|---|---|
| Live, Shadow, MicroLive | derived once from mode Clock and recorded | derived/background |
| Exact Replay | recorded canonical occurrence | not decision authority |
| Accelerated Replay | recorded occurrence; same domain interval | not domain-time authority |
| Counterfactual latency | regenerated only for explicitly replaced families | not domain-time authority |
| Interactive Replay | regenerated under pinned policy | not domain-time authority |

Recorded and regenerated sources are mutually exclusive per timer family/run. ReplayClock, never host wall time, owns domain intervals.
