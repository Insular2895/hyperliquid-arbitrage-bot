# 01 — Maturity Model M0–M5 and Dependencies

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Exact levels

| Level | Name | Evidence boundary |
|---|---|---|
| M0 | SPECIFIED | complete contract and planned evidence |
| M1 | UNIT VALIDATED | local unit/property/golden behavior |
| M2 | REPLAY VALIDATED | deterministic point-in-time realistic Replay |
| M3 | SHADOW VALIDATED | current live observation with no effects |
| M4 | MICRO-LIVE VALIDATED | bounded real execution calibration |
| M5 | LIVE VALIDATED | sustained accepted behavior in exact scope |

## Dependency ceiling

`Maturity(c) <= min Maturity(CriticalDependencies_c)`. Each capability lists critical dependencies and evidence identities. A dependency downgrade immediately removes unsupported dependent permission even if its previous report remains historically valid.

## Scope and skipping

Maturity keys strategy/capability, market/route family, size band, execution mode, model versions and restrictions. Build/config/formula/schema/infra changes are linked impact dimensions. Capital-bearing capabilities move sequentially. Only components with no independent live behavioral effect may mark Shadow/Micro-live not applicable, with rationale and contract proof.

M5 is not an absorbing state. Drift, incidents, evidence expiry or material change can demote it. Re-promotion is explicit.
