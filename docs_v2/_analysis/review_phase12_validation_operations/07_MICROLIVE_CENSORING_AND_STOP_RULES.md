# Micro-live Censoring and Stop Rules

| Outcome class | Population treatment | Terminal statistic use |
|---|---|---|
| full completion / zero fill / partial fill | retain with actual values | eligible when joins valid |
| Recovery | retain separately from original completion | Recovery-specific statistics |
| experiment stop / Risk stop | retain stop cause and exposure | censored unless terminal truth exists |
| `UNKNOWN` | retain unresolved | never fabricate zero/failure |
| data loss / invalid observation | retain validity failure | exclude only from named estimator; include completeness denominator |
| right censoring | retain censor boundary | censor-aware estimators only |

Every pre-registered attempt remains auditable. Stop rules are part of the experiment and cannot improve reported performance by deleting adverse or incomplete observations.
