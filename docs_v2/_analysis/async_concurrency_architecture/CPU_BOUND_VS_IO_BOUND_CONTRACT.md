# CPU-Bound versus I/O-Bound Contract

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

## Separation

| Work type | Runtime treatment |
|---|---|
| persistent socket wait, reconnect, order/cancel/query | asynchronous I/O tasks; never compute pool blocking |
| ordered reducers/current Risk/Reservation | bounded coordinator compute, prioritized over optional work |
| cheap pair lookup/BBO/FastL1/full-L2 baseline/small q-grid | inline until profiling shows a material bottleneck |
| heavy route fanout, advanced features, Participant inference, F2/F3, portfolio proposal | bounded CPU pool proposals; never I/O executor work |
| Recorder encode/compress/checkpoint/archive | background budgets distinct from Core safety processing |
| Replay/MC/training/discovery/search | separate process/resource envelope from Live |

## Small-VPS rule

On a two-vCPU-class initial host, oversubscription can worsen tails through run-queue delay, context switches, cache eviction and background interference. Worker count, queue capacity, affinity and budgets are therefore calibrated; the architecture does not freeze “two workers” or any other number. One shared bounded CPU pool may be studied, but priority and starvation behavior must be proved before promotion.

Account/fill events, cancels, Recovery, reconciliation and ordered commits outrank optional opportunity/model work. Worker flooding cannot starve them. Tokio or another async runtime is an I/O concurrency mechanism, not a license to run unbounded CPU loops or blocking filesystem work on executor threads.

## Evidence

Measure CPU utilization by responsibility, run-queue/scheduler delay, context switches, migrations/steal where valid, queue wait, compute tails, cache/allocations where useful, I/O event handling delay, Recorder interference, stale/deadline rates and EventToDecision/Send. Compare cold, warm and steady workloads, including bursts, account events during worker flood and failure/shutdown.

Only a profile showing a real CPU-bound bottleneck justifies more parallelism. A microbenchmark win that worsens end-to-end tails, state age, safety processing or robust economics fails.
