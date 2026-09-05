# 03 — Risk, Capital, Model and Infrastructure Metrics

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Risk/capital/economics

Observe RiskState and scoped kills, reconciliation, actual/available/reserved balance, exposure, inventory bands, shared capacity, Q_validated, utilization, rejects, route/Recovery/inventory/global PnL, drawdown and tail-risk coverage. Total PnL never masks losing Recovery or unsafe exposure.

## Models/Simulator

Observe model/fidelity/support versions, prediction/invalid counts, OOD/disagreement, Brier/LogLoss and calibration curves, fill/slippage/latency/Recovery/PnL error/coverage, drift by slice and SimulationConfidence. Champion and Challenger metrics are separate.

## Infrastructure/deployment

Observe InfraState, feed arrival/age, RTT/reconnect, compute/sign/send tails, jitter/contention, CPU/memory/network/clock, disk/fsync/free/backlog, runtime/digest/config/schema/capability/owner/license and update state. Provider labels remain bounded and installation-scoped.

Every signal includes unit, observation/event time, scope, source/version and validity. Threshold policy consumes the signal but does not change its meaning.
