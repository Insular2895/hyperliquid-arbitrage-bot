# Market, Data and Account Eligibility Gates

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Fast eligibility path

Before costly forecasts, Risk checks system health, data validity, account consistency, resource availability and hard inventory. Any hard failure returns a machine-readable reject/halt action and stops expensive work.

## Valid market state

Every required leg must have a valid, sequenced, non-crossed and sufficiently fresh authoritative book plus known market/asset metadata, fees and precision rules. Missing data is not defaulted. A feed gap or corruption invalidates the affected state until snapshot/resync; no missing live event is guessed.

`Age_book = Now - LastValidUpdate`; `Age_route = max(Age_leg)`. Both use the approved clock contract. The rule and worst-leg aggregation are hard; thresholds and clock-health bounds are calibrated.

Cross-market edges involving a suspicious leg are treated as possible bad data. Extreme edge outside historical/model support strengthens checks; it does not increase allowed size.

## Account consistency

New risk requires reconciled orders, fills and balances. `UNKNOWN` order/account state keeps affected capital reserved. Available balance cannot be negative, spent twice or committed before reservation. Shared depth and shared balances are reserved atomically across competing plans.

Exchange observations outrank local expectations. Partial/late fills immediately create economic exposure. Reconciliation and safe cancellation remain available when new risk is forbidden.

## Resources and health

Capital, inventory room, API/action/connection budget, clock, feeds, compute and infrastructure must support the action. Cancel, recovery and reconciliation capacity has priority over new orders. Recorder/storage pressure may shed noncritical work but must not block execution; loss of required auditability escalates according to policy.

## Outcome

Eligibility produces explicit metrics, reason codes and one of the canonical Risk actions. Unknown safety means no new risk, not necessarily global shutdown: scope follows the affected dependency while known-exposure safety actions remain governed by RecoveryRiskPolicy.

Source: SRC-005 lines 243–1032, 2900–3070 and 4396–4458.
