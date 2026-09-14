# Recovery Transport Authorization Matrix

| Action | New strategy | Existing continuation | Recovery | Cancel/query/reconcile |
|---|---|---|---|---|
| `ALLOW` | eligible with all gates | eligible if matching | OPEN for Recovery-specific meaning | independent safety context |
| `ALLOW_REDUCED_SIZE` | eligible up to cap | eligible up to cap | OPEN for Recovery-specific meaning | independent safety context |
| `ALLOW_RECOVERY_ONLY` | forbidden | forbidden if risk-increasing | eligible only after full Recovery-context proof; Boolean mapping OPEN | does not forbid safety effects |
| `REJECT` | forbidden | forbidden | no order; containment/re-evaluate | safety effects remain |
| `HALT_*` | forbidden in scope | forbidden in scope | only separately permitted bounded risk reduction if constitution proves it | safety effects remain where possible |

Every order-effect row also requires matching Engine/Recovery state, `RISK_REDUCING` classification for Recovery, current decision, reservation, market/rules/protection and immutable plan lineage. Ambiguity fails closed.
