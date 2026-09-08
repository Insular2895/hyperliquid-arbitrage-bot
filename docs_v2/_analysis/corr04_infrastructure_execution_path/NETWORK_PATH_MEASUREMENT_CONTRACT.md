# Network Path Measurement Contract

`STATUS: SPECIFIED`

## Layers

Record DNS resolution/cache state, TCP connect, TLS handshake/resumption, WebSocket handshake/subscription, persistent application ping/request RTT, request-to-first-byte/complete, disconnect/reconnect, route/hop changes when observable, loss/resets and matched feed arrival. Separate cold connection setup from steady persistent operation.

ICMP is a diagnostic, not order latency. Advertised bandwidth is capacity context, not the primary KPI. Public feed and node peers may traverse different upstream topologies; report end-to-end path effect rather than attributing it to protocol alone.

Use monotonic time for one-host durations; cross-host results require clock quality. Report P50/P95/P99/P99.9/max, sample/invalid counts, time-of-day/regime, endpoint and connection state. Preserve TLS/security settings and production-equivalent payloads. Any route/DNS/TLS/runtime change creates or versions the treatment.
