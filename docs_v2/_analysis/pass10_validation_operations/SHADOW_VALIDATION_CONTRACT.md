# Shadow Validation Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Shadow runs the production Core against current live market/account observation and replaces only the execution effect boundary with `NullShadowTransport`. It records opportunities, forecasts, Risk decisions, plans, would-submit intents, latency, subsequent market evolution, stability and drift. `ActualAccountState` and `ShadowCounterfactualState` remain separate.

Shadow validates live feature availability/freshness, supported-market behavior, decision rates/reasons, latency tails, dependency health, would-size/would-execute logic, Challenger outputs and continuous operating stability. It must prove zero real order effect.

Shadow cannot validate our own causal impact, real queue position/fill, exchange ACK behavior, real fees/slippage, account mutation, cancel races with a real order, or realized Recovery. Those require Micro-live. A Shadow report records scope, duration and regime/sample sufficiency rather than passing merely because a fixed number of days elapsed.

Exit to M4 requires predeclared acceptance gates, no unresolved critical defects, complete evidence joins, current Risk/readiness, tested incident/safe-stop procedures, and explicit approval.
