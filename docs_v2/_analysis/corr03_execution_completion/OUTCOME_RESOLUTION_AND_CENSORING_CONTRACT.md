# CORR-03 — Outcome Resolution and Censoring Contract

DOCUMENTATION STATUS: ANALYTICAL FINALITY CONTRACT

| Status | Meaning | Binary fit | Reporting |
|---|---|---|---|
| `RESOLVED` | authoritative terminal outcome and required reconciliation evidence exist | eligible if label valid | included |
| `PENDING` | normal order/Recovery/reconciliation lifecycle has not yet closed at cutoff | no | count and age |
| `RIGHT_CENSORED` | declared observation window ended before outcome was observed and the analytical design treats later event time as unknown | not in simple binary fit | count, horizon and censor policy |
| `INVALID_EVIDENCE` | gaps/conflicts make actual label untrustworthy | no | count and reason; remediation required |
| `EXCLUDED_BY_PREDECLARED_POLICY` | excluded by a policy fixed before outcomes, with exact reason/scope | no | count; never hide business-negative cases |

`UNKNOWN` is an Order/path state, not a censoring class or failure label. It remains in the attempt cohort. When later evidence proves no fill or a fill, the label advances to the corresponding resolved class while `UnknownOrderOccurred=true` remains.

TT/TTT normally resolve through canonical terminal/reconciliation states; CORR-03 creates no arbitrary 100 ms label horizon. Maker modes may later require explicit time-to-event/horizon analysis because resting/cancel timing is material. Every analysis records cutoff, resolution policy/version, maturity distribution and label revisions.

Binary model fitting uses authoritatively resolved labels only, but study-quality reporting always includes unresolved/censored/invalid fractions. A high unresolved fraction can invalidate promotion even if the resolved subset scores well.
