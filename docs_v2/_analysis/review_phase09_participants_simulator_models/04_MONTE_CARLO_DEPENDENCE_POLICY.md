# Monte Carlo Dependence Policy

| Variables | Plausible | Allowed treatment | Tail consequence when unknown |
|---|---:|---|---|
| latency / survival | yes | conditional/joint or coherent resampling | lower confidence/q or reject |
| fill / adverse selection | yes | condition on fill event/state | stress/reject maker claim |
| partial / Recovery | yes | joint scenario outcomes | conservative Recovery tail |
| volatility / liquidity | yes | regime-conditional vectors | stress ES/VaR |
| local / linked response | yes | supported sparse joint model | no causal/independent claim |

Every pair declares supported joint, coherent resampling, supported independence, unknown, or immaterial. No arbitrary copula.
