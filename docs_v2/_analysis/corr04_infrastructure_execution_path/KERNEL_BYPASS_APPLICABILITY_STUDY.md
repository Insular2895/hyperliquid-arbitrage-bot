# Kernel-Bypass Applicability Study

`STATUS: RESEARCH — NOT V1 BASELINE`

## Current boundary

Hyperliquid application traffic is documented over HTTP/WebSocket, therefore TCP, TLS for secure endpoints and WebSocket/application parsing remain in the path. A packet-I/O framework does not automatically supply compatible TCP, TLS, WebSocket, DNS, reconnect, certificate validation or client semantics.

## Entry gate

No prototype before all are true: profiles show material kernel/network cost after simpler application/Rust/connection/host fixes; candidate NIC/cloud/runtime supports the mechanism; a complete TCP/TLS/WebSocket integration design exists; semantic/security/operations ownership is explicit; benchmark predicts material capture/economic value; least-privilege deployment and rollback are credible.

Compare total event-to-usable-state and order-to-response paths, not packet RX alone. Include TLS, copies, syscalls, scheduling, parsing, queueing, reconnect, certificates, observability, upgrades and failure recovery. AF_XDP/DPDK/F-Stack stay Research even if a microbenchmark is faster.
