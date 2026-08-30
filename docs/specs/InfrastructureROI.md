# InfrastructureROI

## Purpose

Décider upgrades/downscales sur valeur économique marginale robuste.
## Responsibilities

Map latency to capture/PnL, full costs, LCB and decision report.
## Non-responsibilities

Ne confond pas correlation et causalité, ni efficiency ratio et objective.
## Inputs

Benchmarks, survival/opportunity universe, costs, strategy/capital assumptions.
## Outputs

Upgrade/keep/downscale recommendation with uncertainty.
## Dependencies

InfrastructureBenchmark, EdgeSurvivalEngine, AccountingEngine.
## State

Comparison study/version and assumptions.
## Algorithms / formulas

QF-085..093.
## Invariants

Same strategy/universe; no double costs; external prices dated.
## Failure modes

Selection bias, over-attribution, stale price, wide CI, regime dependence.
## Risk interactions

Security/reliability can veto positive ROI.
## Performance requirements

Offline analysis only.
## Metrics

ΔPnL/ΔCost/NetUpgrade/ROI/LCB/SF/capture and stability.
## Persistence

Study manifest/data/report/approval.
## Configuration

Horizon/confidence/SF/cost model versioned.
## Tests

Null/negative/zero-cost cases, bootstrap, sensitivity and double-count checks.
## Maturity requirement

M2 analysis; owner review before change.
## Open calibrated parameters

SF, confidence/horizon and causal attribution method.
