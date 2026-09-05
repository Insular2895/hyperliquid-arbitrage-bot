# SLO Catalog

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| SLO class | Good event / outcome | Why uptime alone fails |
|---|---|---|
| Feed/Book correctness | required market state valid, fresh and ordered | process can be alive on stale/corrupt books |
| Account reconciliation | required account/order/fill state consistent | process can be alive with unknown exposure |
| Decision integrity | eligible decisions have complete deterministic trace and current Risk | service can answer while making invalid decisions |
| Execution safety | no duplicate effects; unknown/partial/recovery handled within policy | availability can coexist with unsafe orders |
| Recovery/reconciliation | Recovery time and outcome reach a proven safe/consistent state | restart success does not prove economic recovery |
| Recorder/evidence | Recorder completeness makes critical events durably attributable with no unexplained loss | trading can continue while auditability disappears |
| Latency | stage/end-to-end distributions remain inside calibrated support | average/uptime hides tail failure |
| Model/simulator calibration | predictions remain calibrated by validated slice | model endpoint can be available but wrong |
| Risk enforcement | hard invariants and kill actions never bypassed | up service may be permissive in unsafe state |
| Deployment/security | current verified artifact, one owner, secrets protected | running untrusted/compromised code is not success |

Every SLO defines scope, indicator, numerator/denominator, invalid/missing handling, window, target, error budget, exclusions, owner, evidence source and action. Targets/windows are calibrated; hard safety invariants have no spendable error budget. SLO breach may demote capability even if process uptime remains high.
