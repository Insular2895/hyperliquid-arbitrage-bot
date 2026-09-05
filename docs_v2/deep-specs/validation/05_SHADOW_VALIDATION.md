# 05 — Shadow Validation

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Shadow is the production Core on live market/account observation with `NullShadowTransport`. Mode differences exist at source/transport/effect/config boundaries, not in strategy formulas, state machines or Risk logic.

Required records: current books/features, opportunities, Champion/Challenger forecasts, Simulator outputs, Risk decisions, plans, would-submit intents/sizes/modes, latency traces, later market outcomes, rejects and reason codes. Actual and counterfactual account/inventory states are isolated.

Acceptance addresses live input validity, supported scopes, decision stability, performance distributions, data completeness, dependency health, prediction/outcome joins, safe alerting and zero real account/order effect. Duration is driven by sample/regime/stability sufficiency; no arbitrary fixed period substitutes for it.

Shadow cannot validate actual ACK/fill/fees/queue position, our causal market response, real cancel races, account mutation or real Recovery. Those omissions are explicit in the promotion report.
