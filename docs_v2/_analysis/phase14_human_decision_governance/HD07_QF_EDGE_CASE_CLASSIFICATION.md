# HD-07 QF Edge-case Classification

| OPEN | Nature | Disposition |
|---|---|---|
| 017, 018, 020, 024, 027, 028 | mathematically undefined/empty case plus encoding | typed invalid/N/A is semantic fallback; concrete representation is IMPLEMENTATION_CHOICE |
| 019, 021, 023, 026 | statistical estimator/parameter | CALIBRATED from evidence |
| 025 | censor-aware estimator/cohort | LEARNED from evidence |

No equation changes. Undefined division is never replaced with an arbitrary number; a safety/economic consumer fails closed until it has a valid result.
