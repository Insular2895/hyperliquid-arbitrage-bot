# DPDK and F-Stack Research

`STATUS: RESEARCH — NOT V1 BASELINE`

DPDK is a user-space packet/data-plane framework requiring supported devices/drivers, hugepages and commonly VFIO/device permissions; it is not itself TCP, TLS or WebSocket. Source: [DPDK Linux Getting Started Guide](https://doc.dpdk.org/guides/linux_gsg/).

F-Stack layers a FreeBSD-derived user-space TCP/IP stack and coroutine API over DPDK, which makes it more protocol-relevant than raw DPDK. It still does not prove compatibility with the Rust HTTP/WebSocket client, TLS/certificate behavior, reconnect semantics, current Hyperliquid endpoints, cloud NIC, container hardening or operational support. Source: [F-Stack repository](https://github.com/F-Stack/f-stack).

Any study must measure whole application paths and account for hugepage/device access, capabilities, memory, single-core polling, packet steering, certificate/TLS library, patch cadence, observability, crash isolation, upgrades and rollback. `--privileged` is never an acceptable baseline. A native/DPDK result cannot inherit V1 maturity.
