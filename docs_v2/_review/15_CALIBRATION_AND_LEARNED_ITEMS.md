# Calibration and Learned Items

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

The final target map contains 60 `CALIBRATED` requirement rows and 6 `LEARNED` rows. They are not hidden defaults. Each promoted value/artifact must identify dataset, scope, method, confidence/support, version, owner, review date, fallback and consumers.

| Evidence phase | What becomes eligible for calibration/learning | Typical artifact | Blocks |
|---|---|---|---|
| PRE-IMPLEMENTATION CONFIG DEFAULT | harmless capacities, bounded queue/config defaults and test tolerances | reviewed config schema/default rationale | coding only where a concrete bound is required |
| RECORDER | throughput, event volume, chunk size, storage/retention envelope, backpressure | soak/capacity report | trusted capture and storage profile |
| REPLAY | feature windows, deterministic tolerances, candidate q grids, reconstruction quality | ReplayReport/calibration dataset | the consuming deterministic component |
| SHADOW | live latency/freshness/health windows, support, route/Atlas thresholds | ShadowRun and distribution report | affected live-input readiness |
| MICRO-LIVE | fills, slippage, adverse selection, tail loss, Recovery, exact Risk and size bands | pre-registered MicroLiveRun | affected capital probe/promotion |
| LIVE | continuously observed drift, capacity, operating/error budgets and next-band support | scoped ValidationReport | renewal/expansion of M5 scope |
| INFRA-BENCHMARKED | provider/region/network ranking, LCB/alpha/safety factor, upgrade economics | comparable InfraBenchmark | infrastructure selection/promotion |
| MODEL-LEARNED | survival, response, maker coefficients, horizons, cohorts, OOD/drift and clipping | immutable ModelReport/artifact | model-dependent manifest only |
| COMMERCIAL POLICY | license grace/revocation, consent/export and support retention policies | approved policy/threat model | distribution/telemetry scope only |

Calibration may only narrow or parameterize an already approved mechanism. A learned artifact is not a decision until promoted. Unsupported data returns UNKNOWN/LOW/OOD or the documented conservative fallback; it never becomes a guessed zero or increased permission.
