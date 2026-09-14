# Replay Mode Consistency Matrix

| Mode | Order | Clock/timers | RNG | Truth class |
|---|---|---|---|---|
| exact | recorded sequence | recorded TimerEvents/ReplayClock | seed if active | REPLAY |
| accelerated | same | same domain intervals | same | REPLAY |
| counterfactual latency | same exogenous evidence; pinned branch | versioned replacement policy | required if active | COUNTERFACTUAL |
| interactive | pinned branch order/policy | generated under ReplayClock | required | SIMULATED/COUNTERFACTUAL |

All use the same reducers; none mutates ActualAccountState.
