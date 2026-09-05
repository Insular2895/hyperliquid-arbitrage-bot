# Infrastructure Validation Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Evidence family | Required measurements | Gate |
|---|---|---|
| feed/network | paired first arrival, feed age validity, API/WS RTT, loss/routes, reconnect stages | distributions and clock uncertainty; healthy-feed semantics |
| compute | real hot-path stages, scheduler jitter, contention/steal/frequency | P50/P95/P99/P99.9/MAX, representative workload |
| memory/storage | RSS/pressure/swap, write/fsync/compression, free space/backlog | headroom and no unsafe Recorder interference |
| runtime | native/container treatments and security profile | identical build/workload; performance and hardening both valid |
| clock | offset, uncertainty, dispersion, step/loss behavior | invalid clock invalidates cross-host timing and latency-sensitive decisions |
| stability | outages, reconnects, tail events, degradation/unsafe intervals | time/regime coverage and recovery proof |
| economics | CaptureRatio, InfraLostPnL/RecoverablePnL, cost, NetUpgradeValue/LCB | technical improvement plus robust economic value |
| operations | diagnostic, cold recovery, host move, single owner, rollback | no-new-risk until health/reconciliation/current capability |

Infrastructure identity includes provider/region/offer/resources/OS/kernel/runtime/network mode. A material move invalidates inherited evidence. More capital is not an infrastructure promotion trigger. Exact thresholds and observation windows are calibrated and versioned.
