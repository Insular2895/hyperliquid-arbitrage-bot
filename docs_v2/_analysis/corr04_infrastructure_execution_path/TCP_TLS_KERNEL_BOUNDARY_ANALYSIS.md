# TCP / TLS / Kernel Boundary Analysis

`STATUS: CURRENT APPLICATION BOUNDARY`

WebSocket is layered over TCP and secure `wss` adds TLS; TCP supplies reliable ordered byte streams, TLS authenticates/encrypts, and WebSocket supplies framing/control. Sources: [RFC 6455](https://datatracker.ietf.org/doc/html/rfc6455), [TLS 1.3 RFC 8446](https://datatracker.ietf.org/doc/html/rfc8446), [`tcp(7)`](https://man7.org/linux/man-pages/man7/tcp.7.html).

Observed latency can include NIC/IRQ/softirq, kernel TCP, wakeup/scheduler, socket/client queues, TLS record/crypto, WebSocket framing, decoding, application queueing, exchange processing and response generation. ACK or first byte cannot be assigned to one layer by subtraction without valid endpoints.

Profile syscalls/wakeups/CPU, socket/client options, TLS handshake/resumption/record behavior, connection persistence and application timing before selecting a lower-level technology. Never disable certificate verification or encryption for a production-equivalent comparison. A kernel-bypass proposal must replace or integrate every required layer explicitly.
