# 18 — Operations and Monitoring

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## 1. Purpose and boundary

Operations makes runtime health, permissions, evidence, alerts, runbooks, incidents and revalidation actionable. It does not replace Risk, mutate strategy logic from dashboards, implement a monitoring stack or turn a metric into permission.

## 2. Operating objective

Keep economic state known, prevent unsafe new risk, preserve cancel/reconciliation/Recovery paths, detect drift/failure early, retain reconstructible evidence and restore only through proven readiness and capability.

## 3. Canonical runtime states

At minimum observe `EngineState`, `RecoveryState`, `ReconciliationState`, `FeedHealth`, `AccountReconciled`, `RiskState`, `InfraState`, active executions, unknown orders and current CapabilityManifest scope. Missing/invalid state is explicit; it is not coerced to healthy.

## 4. Liveness

Liveness means the process/control loop is alive enough to report and progress. It says nothing about feed freshness, account truth, Risk permission, model validity or trading readiness.

## 5. Readiness

Readiness means required configuration, artifact/owner, clock, feeds/books, account/orders/fills, reconciliation, models, infrastructure, validated capability and Risk are currently sufficient for a declared action/scope. A process can be live but not ready.

## 6. Capability health

Health is scoped. One market/model/mode may be degraded or suspended while unrelated safe capabilities remain available. Global halt is used when authority, account truth or shared critical dependency cannot be scoped safely.

## 7. Safe action classes

Operations distinguishes new risk, risk-reducing Recovery, cancel, reconciliation, persistence/evidence and read-only diagnostics. A no-new-risk state must not disable the mechanisms needed to understand or reduce existing exposure.

## 8. Market and data metrics

Mandatory signals include feed connection/health, BookAge/freshness, gaps/reorder/corrupt/crossed books, snapshot/version/source quality, receive/exchange times and clock uncertainty, recorder sequence/backlog/loss and data-invalid intervals.

## 9. Decision metrics

Track opportunities, accepted/reduced/rejected counts, reason classes, would-versus-actual decisions, candidate size/Q_validated, decision latency, trace completeness, stale-result rejection and dependency/capability version.

## 10. Execution metrics

Track active executions/orders, zero/partial/full fills, send→ACK/first/last fill/cancel distributions, unknown orders and resolution, reconciliation state/time, Recovery count/path/loss, dust/buffer, duplicate/late events and reject reason.

## 11. Risk, capital and economics metrics

Track RiskState/kills, account reconciliation, balances/reservations/exposure, inventory bands, shared capacity, capital utilization, Q_validated, PnL separately for route/Recovery/inventory/global, drawdown and ES/CVaR coverage. Global PnL cannot hide component failure.

## 12. Model and Simulator metrics

Track artifact/support versions, prediction counts, missing/invalid output, OOD/disagreement, Brier/LogLoss/calibration error, distribution coverage, predicted/actual bias/tails, drift and SimulationConfidence by validated slice.

## 13. Infrastructure metrics

Track feed arrival/age, API/WS RTT, reconnect stages, hot-path/sign/send tails, scheduler jitter, CPU/frequency/steal/run queue, packet loss/route change, clock offset/uncertainty, RAM/pressure/swap, disk write/fsync/free, Recorder backlog and runtime identity.

## 14. Deployment/security metrics

Expose active/previous digest, build/config/schema/model/capability identity, release/update/migration state, owner/lease status, license health, secret/redaction failures, runtime hardening drift and readiness reasons—without revealing credentials or unbounded sensitive IDs.

## 15. Metric semantics and cardinality

Each metric defines unit, scope, observation/event time, validity and source/version. Latencies use count, P50/P95/P99/P99.9/MAX where applicable. Labels are bounded (market family, mode, reason class, version, instance); raw order/wallet/execution IDs remain in traces/logs.

## 16. Alert record

An alert includes stable type, severity, scope, state, first/last seen, evidence window, value/validity, threshold/config version, automated action, runbook, acknowledgement and IncidentId when escalated. Delivery failure cannot block the hot path.

## 17. P0

P0 is an active or credible critical safety, security, ownership or exposure failure. Default posture is immediate affected/global no-new-risk, evidence preservation, human paging and reconciliation/containment.

## 18. P1

P1 is serious degradation likely to become unsafe or materially invalidate a capability. Scope-degrade/disable immediately as required and escalate urgently.

## 19. P2

P2 is persistent non-critical degradation, calibration/evidence issue or reduced margin. Investigate within a calibrated window; it never authorizes automatic widening.

## 20. P3

P3 is informational, maintenance or trend evidence without direct safety effect. Retain for review; do not change capital permission solely from P3.

## 21. Locked alert actions

Unknown order/account/reconciliation and critical feed/book failures remove affected new risk; unhealthy clock removes latency-sensitive decisions; infra unsafe removes new risk; failed Recovery escalates exposure; secret compromise/split brain fences authority; critical persistence failure protects evidence and escalates Risk. Safe cancel/reconcile/Recovery remain where possible.

## 22. Calibrated thresholds and hysteresis

Numeric thresholds, observation windows, hold times, escalation targets and response objectives are versioned calibrated parameters. Recovery requires sustained valid evidence and required reconciliation; one good sample does not erase a failure interval.

## 23. Critical alert classes

Canonical closure examples are `BOOK_STALE`, `ACCOUNT_UNRECONCILED`, `UNKNOWN_ORDER`, `RECOVERY_FAILED`, `CLOCK_UNHEALTHY`, `DISK_CRITICAL`, `INFRA_UNSAFE`, and `MODEL_DRIFT`. Infrastructure aliases map to these semantics without inventing competing permission logic.

## 24. SLO architecture

SLO classes cover feed/book correctness, account reconciliation, decision integrity, execution safety, recovery, recorder/evidence, latency, model/simulator calibration, Risk enforcement and deployment/security. Each defines indicator, population, validity, window, target/error budget, owner and breach action.

## 25. Why uptime is insufficient

A running process may consume stale books, hold unknown orders, lose audit data, use a drifted model or be unable to reconcile. Process uptime is therefore a liveness signal, not a trading-system success SLO.

## 26. Hard invariants and error budgets

Hard Risk/authority invariants have no spendable error budget. Statistical service targets may have calibrated budgets, but budget availability cannot permit duplicate orders, known unsafe new risk or secret exposure.

## 27. Runbook structure

Every runbook states trigger/scope, immediate safety posture, automated and human steps, evidence to pin, decision tree, escalation, verification, reconciliation, revalidation and exit criteria. It never tells an operator to guess a book/order/account state.

## 28. Feed/Book Desync runbook

Stop affected new risk; pin feed/clock/sequence evidence; identify gap/corruption/snapshot mismatch; reconnect/resubscribe; obtain valid snapshot; replay ordered deltas; rebuild dependent features/routes; reconcile if decisions/orders were affected; resume only after sustained health and readiness.

## 29. Unknown Order runbook

Freeze affected reservation/capital; do not resend blindly; query by CLOID/OID and obtain fills/orders/account; deduplicate/apply actual fills; resolve terminal/remainder state; reconcile balances/reservations; keep scope blocked if ambiguity remains.

## 30. Crash/Reboot runbook

Record forced stop where possible; start non-ready; prove single owner; validate artifact/config/clock/feed; load checkpoint plus journal; query orders/fills/balances; reconstruct executions/recovery/inventory; reconcile; run readiness gates before any new risk.

## 31. Disk Pressure runbook

Pin incident/critical evidence; enforce Recorder priority and account for any invalid region; rotate/archive/expand through approved operations; monitor backlog/write/fsync; escalate Risk if critical durability fails; resume only after stable storage and evidence-quality review.

## 32. Model Drift runbook

Scope affected model/capabilities; preserve predictions/outcomes and support slices; fallback, reduce size or disable; verify data/feature/model versions; reproduce with point-in-time data; recalibrate offline; run temporal OOS, Shadow and required Micro-live; explicitly re-promote.

## 33. Update Failure runbook

Stop new risk according to transactional update state; reject incomplete/unverified candidate; preserve current safe owner before stop or restore known previous digest afterward; respect migration markers; never rewind exchange truth; restart non-ready and reconcile.

## 34. Secret Compromise runbook

Risk-off and fence signer/owner; revoke/rotate scoped credentials; preserve sanitized evidence; inspect artifact/config/log/export paths; verify no unauthorized orders; reconcile account; rebuild from clean trusted artifacts; obtain security and capability approval before resume.

## 35. IncidentId and IncidentRecord

IncidentId groups related events. IncidentRecord contains severity, affected markets/executions, start/end, triggers, actions and resolution. Incidents are domain objects linked to alerts, evidence, decisions and postmortems—not generic log strings.

## 36. Incident package and timeline

Package manifests/build/config/models/formulas/schemas/capability, checksummed RAW/quality windows, ordered events/state hashes, decisions/intents/journal, actual orders/fills/account/reconciliation/PnL, predictions, metrics/alerts/logs, runbook actions and remediation. Timeline uses canonical sequence plus source/receive timestamps and clock uncertainty.

## 37. Redaction and client control

Exclude secrets, seeds, tokens, raw environments, unnecessary identifiers/history and memory dumps. Build locally from allowlisted fields; run denylist/entropy/canary checks; fail closed; provide inclusion manifest/hash; require explicit client export.

## 38. Incident demotion and resume

An incident may demote M5 immediately. Resume requires containment, current exchange truth/account reconciliation, verified fix or rollback, affected test/Replay proof, Shadow/Micro-live where assumptions changed, operator review and explicit scoped re-promotion.

## 39. Operational reviews

Mandatory layers are continuous safety response, recent operator review, periodic model/simulator/capacity/incident review, monthly/periodic capability/SLO/infra/security review, release/change review and incident postmortem. Exact calendar cadence is calibrated.

## 40. Drills

Restore drills prove backups/state/evidence are usable. Reconciliation drills prove orders→fills→balances→reservations and unknown-capital locking. Safe-stop, crash, rollback, signer/secret and split-brain drills apply by deployed profile. Each produces immutable evidence and remediation.

## 41. Safe shutdown

Disable new risk; cancel/resolve resting orders per Risk; complete or bound active executions/Recovery; persist coherent journal/checkpoint/evidence; release ownership; record any unresolved exposure. A timeout causes escalation, never a false clean stop.

## 42. Safe restart and readiness

Every crash/reboot/update/rollback returns through BOOT/config/clock/feed/book/account/order/fill/reconciliation/Risk/capability gates. Persisted READY is never trusted. Ambiguous owner or account state prevents new risk.

## 43. Continuous calibration

Continuously join predictions to outcomes, monitor support/error/coverage/economics, and create evidence for offline recalibration. It does not mean live self-modifying weights, thresholds, Risk rules or uncontrolled promotion.

## 44. Open/calibrated operations choices

Telemetry backend, dashboard product, paging provider, numeric thresholds, windows, response-time objectives, retention capacities, exact cadence and final command/API spellings remain calibrated/open. Their chosen implementations must honor these contracts and client isolation.
