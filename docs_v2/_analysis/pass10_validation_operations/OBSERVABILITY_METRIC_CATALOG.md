# Observability Metric Catalog

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Family | Mandatory signals | Safety use |
|---|---|---|
| runtime | EngineState, process liveness, readiness and reason, restart/recovery count | distinguish alive from permitted |
| market/data | FeedHealth, BookAge/freshness, gaps, invalid/crossed books, source quality, recorder sequence/backlog/loss | block stale/invalid state |
| decision | opportunities, would/allowed/reduced/rejected, RejectReason, candidate q/Q_validated, trace completeness | detect policy/model behavior changes |
| execution | active executions, order/fill/partial/zero, send→ACK/fill/cancel distributions, UnknownOrders, reconciliation and Recovery count/loss | scope no-new-risk and reconstruct |
| account/capital | AccountReconciled, balances/reservations/exposure, inventory bands, stranded/dust, capital utilization | prevent unknown/double-spent capacity |
| economics/risk | PnL by route/Recovery/inventory/global, drawdown, ES/CVaR coverage, RiskState/kills | never let aggregate PnL hide failure |
| models/simulator | versions, support/OOD, calibration error, Brier/LogLoss, disagreement, drift, coverage, SimulationConfidence | degrade model-dependent capability |
| infrastructure | InfraState, feed arrival, API/WS RTT, hot-path/sign latency, jitter, clock, CPU/memory, disk/fsync/free, network, reconnect | Risk eligibility and operations |
| deployment/security | digest/config/schema/capability identity, owner, license, update/rollback status, redaction failures | integrity/authority/readiness |

Latency and reliability metrics report count plus P50/P95/P99/P99.9/MAX and invalid intervals where applicable. Metrics are non-blocking and use bounded-cardinality dimensions such as market family, mode, reason class, version and instance. Raw order, wallet or execution IDs belong in traces/logs, not unbounded metric labels.

Metric value, unit, event/observation time, scope, validity, source and threshold/config version are explicit. Missing is not healthy and never coerced to zero.
