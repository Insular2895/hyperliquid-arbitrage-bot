# AF_XDP Research

`STATUS: RESEARCH — NO PROTOTYPE AUTHORIZED`

Linux AF_XDP provides high-performance frame RX/TX through XDP, UMEM and user-space rings. It requires an XDP program, queue binding and a user-space application; zero-copy depends on driver/NIC support. Source: [Linux AF_XDP documentation](https://docs.kernel.org/networking/af_xdp.html).

AF_XDP does not itself provide TCP, TLS, WebSocket or Hyperliquid application semantics. A complete candidate would still need a compatible networking stack and secure connection lifecycle, or a narrower demonstrably useful boundary. Cloud/VPS driver support, queue control, capabilities, memory locking, observability and failure recovery must be verified.

Disposition: not V1 baseline, not a Docker-removal justification, not a security exception. Entry only through the kernel-bypass applicability gate and full production-equivalent benchmark.
