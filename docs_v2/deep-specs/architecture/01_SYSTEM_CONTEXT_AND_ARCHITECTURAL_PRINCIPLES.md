# 01 — System Context and Architectural Principles

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Product boundary

The system is an isolated, client-operated Hyperliquid spot routing/arbitrage engine. It receives public market and authenticated account facts, computes bounded evidence-supported actions and submits protected effects through the client signer. The client owns the VPS, account, signer and capital; the vendor supplies artifacts and optional licensing, not custody or centralized execution.

## Scope layers

- **Initial:** same-venue Hyperliquid spot, OWA/TT and Triangle/TTT structures; TT first and TTT separately evidenced.
- **Progressive:** empirical Participants, F2/F3 Simulator, maker intelligence, MT/MTT, Portfolio and Bridge when promoted.
- **Future/Research:** cross-exchange, perp hedging, node, standby, F4 and explicit agents.

Interfaces are final-capable, but capability is narrowed by configuration, evidence, license, readiness and Risk. Future support cannot impose synchronous V1 cost or permission.

## Governing order

`Safety > StateConsistency > ExistingExposure > RiskLimits > ExpectedPnL > Opportunity` is both a decision order and a dependency rule. An expected-value improvement cannot compensate for stale state, unresolved exposure or hard-Risk failure.

The remaining principles are: one `NetConvert`; size-dependent economics; broad cheap knowledge/selective expensive compute; reserve first; exchange/actual-fill truth; first-class Recovery/Reconciliation; same Core across modes; non-blocking Recorder/observability; and progressive activation on final interfaces.

## Trust boundaries

The exchange is authoritative for orders/fills/balances but its payload is untrusted until normalized and validated. The host controls the container and therefore remains in the trust model. The signer is a least-privilege boundary. Registry/license/operator inputs are control-plane data; none may directly mutate economic state or bypass Risk.
