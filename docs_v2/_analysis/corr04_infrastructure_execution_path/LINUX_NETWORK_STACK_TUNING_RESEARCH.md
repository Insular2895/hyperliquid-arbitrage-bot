# Linux Network Stack Tuning Research

`STATUS: RESEARCH — NO SYSCTL CHANGE AUTHORIZED`

The application path is persistent TCP + TLS + WebSocket/HTTP. Each treatment must identify a measured boundary and the actual Rust/client defaults before proposing a change.

| Candidate | Potential mechanism | Main failure/limit |
|---|---|---|
| socket buffer sizing | absorb bursts/reduce drops | oversized queues can increase memory and latency |
| `TCP_NODELAY` | disable Nagle for small writes | may already be set; verify the socket/client |
| busy polling | poll device queue in receive path | CPU/power/starvation; driver/config support required |
| quick ACK | temporary ACK behavior | not a permanent universal low-latency mode |
| congestion control | path-dependent send behavior | small persistent messages may not be bottlenecked there |
| offload/coalescing | throughput/CPU tradeoff | can add batching latency; cloud control may be absent |

Primary references: [`tcp(7)`](https://man7.org/linux/man-pages/man7/tcp.7.html) and [Linux network sysctls](https://docs.kernel.org/admin-guide/sysctl/net.html). The legacy `tcp_low_latency` setting is not a current optimization basis. No giant sysctl list is canonical. Each experiment records before/after, kernel/client versions, correctness/loss/reconnect/resource guardrails and rollback.
