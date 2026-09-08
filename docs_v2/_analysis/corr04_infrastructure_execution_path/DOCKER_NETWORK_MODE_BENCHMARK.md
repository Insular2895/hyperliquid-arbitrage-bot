# Docker Network Mode Benchmark

`BASELINE: OCI/Docker — MODE SELECTION OPEN`

Official Docker semantics at retrieval: bridge uses a software bridge with isolation and typically NAT/masquerading; host mode shares the host network namespace, removes NAT/userland-proxy handling and ignores published-port mappings, while reducing network isolation. Sources: [network drivers](https://docs.docker.com/engine/network/drivers/), [bridge](https://docs.docker.com/engine/network/drivers/bridge/), [host](https://docs.docker.com/engine/network/drivers/host/).

| Treatment | Security posture | Evidence |
|---|---|---|
| user-defined bridge | standard hardened baseline | application RTT, matched arrival, reconnect, hot-path and CPU tails |
| host network | same non-root/read-only/capability/secret controls; explicit port/bind audit | incremental technical gain and enlarged exposure |
| native reference | equivalent service/config/security behavior where possible | upper-bound diagnostic, not promotion |

Hold binary/build, host, workload, connections, endpoints, resources, logging and TLS constant. Record Docker/runtime/kernel versions. No privileged mode, Docker socket, secret broadening or disabled firewall/TLS to improve a result. Report correctness/reliability/security guardrails and economic relevance, not microbenchmark delta alone.
