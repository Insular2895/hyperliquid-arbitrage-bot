# Node Resource and Interference Model

`STATUS: CURRENT FACT SNAPSHOT + MEASUREMENT CONTRACT`

The inspected official node snapshot publishes 16 cores, 128 GB RAM and 500 GB SSD for non-validator; latency guidance recommends at least 32 logical cores and 500 MB/s disk throughput; default output may approach 100 GB/day. These are dated external facts, not permanent requirements.

## Resource model

Measure node CPU/utilization/run queue, RSS/faults/swap, disk write/fsync/space/backlog, ingress/egress/peer stability, applied-block lag, output queue age, restarts/catch-up and build/flag/config. Correlate them with engine scheduler wait, hot-path tails, feed state age, Recorder backlog and reconnect/outage.

Treat node, bot and Recorder as three competing workloads. The experiment matrix isolates each and their combinations. A node that advances arrival but increases canonical-state invalidity, P99.9 compute, P0 evidence risk or operational fragility fails the guardrails.

No node process receives trading signer/API-wallet secrets by default. Public gossip ports and peer configuration require a dedicated threat review.
