# RunMode Architecture Matrix

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Dimension | Replay | Paper | Shadow | MicroLive | Live |
|---|---|---|---|---|---|
| Market source | Recorded ordered data | live or replay | live | live | live |
| Account source | recorded/simulated | synthetic | live observed or no-effect projection | live exchange | live exchange |
| Execution transport | recorded/simulated | paper simulator | no-effect shadow | real protected | real protected |
| Real orders | No | No | No | Yes, probe only | Yes, validated scope |
| Real capital | No | No | No | bounded approved probe | bounded current M5 scope |
| Clock | `ReplayClock` + recorded time domains | source-appropriate | live monotonic/wall | live monotonic/wall | live monotonic/wall |
| Recorder | required for trace/evidence | required | required | required P0–P3 | required P0–P3 |
| Risk semantics | same constitutional gates on mode facts | same; synthetic evidence cannot claim Live | same; no effect permission | same + strict experiment limits | same + exact scope |
| Core reducers/formulas/ESM | identical contracts | identical contracts | identical contracts | identical contracts | identical contracts |
| Capability | M2 relevant scope | configured non-capital | M3 relevant scope | M4 exact scope | M5 exact scope |
| What it proves | determinism/history/failure | logic without exchange truth | live-input stability/forecasts | actual transport/fills at probe q | sustained exact-scope behavior |
| What it cannot prove | current/live intervention | exchange fills/impact | fills, queue, own impact, Recovery reality | other q/market/mode | unsupported/general scale |

`RunMode`, Simulator `SimulationMode` and `ReplayFidelity` are independent provenance axes. Mode differences live in event sources, transport, clock and permissions; no mode may replace formulas, ease fills, skip Risk, create planned inventory or alter state-machine truth.
