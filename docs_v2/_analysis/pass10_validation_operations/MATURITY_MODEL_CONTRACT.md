# Maturity Model Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Level | Exact name | Required evidence | Permission boundary |
|---|---|---|---|
| M0 | SPECIFIED | purpose, inputs, outputs, invariants, formulas, schemas, failure states, planned tests, performance budget | design only |
| M1 | UNIT VALIDATED | compiling implementation plus applicable unit, property and golden evidence | no claim of realistic market behavior |
| M2 | REPLAY VALIDATED | deterministic historical, failure and counterfactual Replay; no lookahead; reproducible manifest | simulated evidence only |
| M3 | SHADOW VALIDATED | production core on current live data, no order submission, would-decide/would-execute evidence and stability | observe-only |
| M4 | MICRO-LIVE VALIDATED | real orders/fills/account under strict limits; predicted/actual execution, recovery and PnL calibration | bounded real-capital probe scope |
| M5 | LIVE VALIDATED | sustained acceptable economic, risk, calibration and operational evidence in the exact promoted scope | bounded Live authority, continuously reviewable |

Promotion is sequential. A purely technical component with no capital, order, Risk, fill or live-market behavioral consequence may document why Shadow/Micro-live are not applicable. Decision-affecting capabilities do not skip them.

`Maturity(component) <= min(Maturity(critical dependencies))`.

Maturity is scoped, not a global badge. The scope includes capability, markets/routes, sizes, mode, models, formulas/schemas/config, release and infrastructure. Implementation, enablement, license entitlement and Stable release are not validation evidence. M5 can be demoted immediately when evidence expires, dependencies regress, drift appears, incidents invalidate assumptions or scope changes materially.
