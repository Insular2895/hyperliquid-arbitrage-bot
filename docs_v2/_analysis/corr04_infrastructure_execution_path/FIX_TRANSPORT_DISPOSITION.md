# FIX Transport Disposition

`CURRENT DISPOSITION: NOT_CURRENT / REJECTED FOR V1`

Official Hyperliquid sources inspected on 2026-09-08 document HTTP `/exchange` and WebSocket post requests for order actions. No current official FIX order-entry support was found. Another exchange or system using FIX is not Hyperliquid evidence.

Existing `ExecutionTransport` remains protocol-abstract enough for a later adapter. If official FIX support appears, it becomes an external-revalidation Future candidate and must prove authentication, order/status/fill semantics, feature parity, latency/reliability, recovery, security, SDK/support and net economic value. No speculative FIX layer or code is added.
