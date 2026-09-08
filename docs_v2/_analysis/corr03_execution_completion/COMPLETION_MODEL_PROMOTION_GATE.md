# CORR-03 — Completion Model Promotion Gate

DOCUMENTATION STATUS: MAPPED TO EXISTING M0–M5 — NO AUTHORITY GRANTED

| CORR-03 stage | Existing maturity mapping | Permitted use | Required exit evidence |
|---|---|---|---|
| C0 Data only | M0/M1 | retain/reconstruct labels | schema, label golden fixtures, join integrity |
| C1 Offline baseline | M1/M2 | analytical constant/empirical benchmark | point-in-time data, support, temporal OOS |
| C2 Replay/OOS Challenger | M2 | compare candidates | calibration, baseline lift, OOD/fallback/runtime |
| C3 Shadow observe-only | M3 | emit/freeze forecasts; no decisions | stable joins/latency/drift; no actual fill claims |
| C4 Micro-live observe-only | M4 | calibrate on small real attempts | supported q/mode slices, actual labels, no safety regression |
| C5 Decision-affecting input | M4/M5 scoped promotion | only explicitly approved ranking/EV consumer | incremental economic value, stable calibration, support, safety and human/Risk governance |

Before C5: sufficient resolved support, low/understood unresolved/invalid fraction, temporal OOS calibration, performance over constant/simple baseline, slice stability, OOD/fallback, compatible hot-path latency, Shadow and capital-relevant Micro-live evidence. CORR-03 starts at observe/research/calibrate and creates no Risk threshold. Ranking, sizing, QF-056/057/063 or QF-076 integration remains CORR-05/human review.
