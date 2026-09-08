# 05 — Shadow Validation

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

Shadow is the production Core on live market/account observation with `NullShadowTransport`. Mode differences exist at source/transport/effect/config boundaries, not in strategy formulas, state machines or Risk logic.

Required records: current books/features, opportunities, Champion/Challenger forecasts, Simulator outputs, Risk decisions, plans, would-submit intents/sizes/modes, latency traces, later market outcomes, rejects and reason codes. Actual and counterfactual account/inventory states are isolated.

Acceptance addresses live input validity, supported scopes, decision stability, performance distributions, data completeness, dependency health, prediction/outcome joins, safe alerting and zero real account/order effect. Duration is driven by sample/regime/stability sufficiency; no arbitrary fixed period substitutes for it.

Shadow cannot validate actual ACK/fill/fees/queue position, our causal market response, real cancel races, account mutation or real Recovery. Those omissions are explicit in the promotion report.

CORR-04 uses Shadow as the primary public-versus-node challenger stage: one public canonical reducer, one isolated node comparison state, strict matched-event evidence and no real effects. Record alignment failures, state parity/age, gaps/reconnect/lag, resource interference, would-opportunities/funnel and profile provenance. Earlier arrival alone cannot pass.
