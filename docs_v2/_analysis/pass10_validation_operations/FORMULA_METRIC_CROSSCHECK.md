# Formula and Metric Crosscheck

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

PASS 10 consumes Formula authority and does not rewrite equations.

| Reference | PASS 10 use | Owner / status |
|---|---|---|
| QF-007–027 | conversion, route, comparator and profitable-size golden evidence | PASS08 interface; exact audit PASS11 |
| QF-043–047 | survival/response inputs | PASS02 model evidence |
| QF-054–062 | adverse selection and Simulator outcomes | PASS02/03 calibration |
| QF-064–080 | inventory, reservations, sizing, Recovery and PnL evidence | PASS04/07; exact audit PASS11 |
| QF-084–093 | infrastructure latency/economic comparison | PASS01 validation/economics |
| QF-095 | Brier score | probabilistic calibration |
| QF-096 | LogLoss | probabilistic sharpness/error with numeric clipping per Formula authority |
| QF-099 | fill calibration error | predicted versus observed fill by bucket/slice |
| QF-100 | EconomicLift | comparable model versus baseline after costs |
| QF-101 | ModelValue | economic gain net of latency and operational cost |
| QF-102 | disagreement | uncertainty evidence, never permission |
| QF-103 | OODScore | model-dependent support distance; mapping calibrated |
| QF-105–108 | capital/portfolio/sizing interfaces | PASS07 evidence and scaling gates |

Metrics not backed by a locked formula are operational indicators with explicit definition/version/unit. Numeric thresholds, sample minima, windows, confidence methods and aggregation rules remain calibrated unless a source contract freezes them. PASS 11 has not begun.
