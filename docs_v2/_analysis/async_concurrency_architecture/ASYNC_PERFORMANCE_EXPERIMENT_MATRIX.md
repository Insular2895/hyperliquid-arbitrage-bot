# Async Performance Experiment Matrix

`DOCUMENTATION STATUS: BENCHMARK SPECIFICATION — NO RESULTS YET`

All candidates preserve Formula/Risk/Execution semantics. Measurements bind commit/build, Dataset/order, config/formulas/models/routes, host/profile, worker/queue policy and instrumentation. Numerical configuration is calibrated by experiment.

| ID | Candidate | Hypothesis | Correctness oracle | Primary measurements | Tail/pressure treatments | Capture/economic evidence | Status |
|---|---|---|---|---|---|---|---|
| A | mostly inline ordered Core | lowest coordination overhead on small fanout/2-vCPU | canonical DecisionTrace | EventToDecision/Send P50/P95/P99/P99.9, compute, CPU, allocations | burst, large L2, account/fill interruption, Recorder pressure | funnel/capture/RAEV/PnL where material | `BASELINE REQUIRED` |
| B | cheap inline filters + bounded route worker pool | reduces high-fanout tail | A exact results under same policy | queue wait, compute, handoff, scheduler, stale/deadline, context switches | fanout distribution, worker flood, 2-vCPU oversubscription | routes evaluated/missed, state age, capture/economics | `CANDIDATE` |
| C | parallel q-grid | independent q work shortens sizing tail | same q results and deterministic chosen q | per-q compute, fan-in, queue wait, allocations | sparse/dense grids, deadline, stale state | chosen-size/capacity/economic parity | `CANDIDATE` |
| D | precomputed/snapshot model forecast | removes optional inference from decision critical path | artifact/input/support parity | cache age/hit, inference/refresh, stale/OOD/fallback | model unavailable, drift, burst | calibration and incremental economic value | `CANDIDATE` |
| E | CPU worker-count variants | find minimum robust tail without starving I/O | same results/DecisionTrace | CPU, scheduler delay, switches, queues, I/O delay | 1/2-vCPU-like quotas, Recorder/exporter, panic | capture/economics plus safety-event latency | `CALIBRATED` |
| F | `BATCH_SELECT` | fuller candidate set improves allocation enough to offset delay | policy-versioned deterministic result | wait/fan-in/deadline/state age/EventToSend | one slow/no-return worker, burst, stale inputs | selection opportunity cost, fill/capture/economics | `CALIBRATED / REPLAY + SHADOW` |
| G | deterministic `EARLY_COMMIT` | bounded earlier commit preserves edge | declared priority/admissibility; never completion order | time-to-eligible/commit/send, later-better candidates | permuted completion, starvation/fairness, capacity conflict | missed-better-route versus capture/economics | `CALIBRATED / REPLAY + SHADOW` |

Every row also reports queue saturation, deadline misses, stale results, Recorder interference and state age at send. Semantic parity is evaluated before performance; policy F/G intentionally have versioned scheduling semantics and therefore compare both behavior and economics rather than claiming identical DecisionTrace.
