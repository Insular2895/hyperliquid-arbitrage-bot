# Validation and Operations Review

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Maturity and permissions

| Level | Meaning | Capital |
|---|---|---:|
| M0 | specified contracts, risks and planned tests | none |
| M1 | component correctness/conformance | none |
| M2 | integrated deterministic Replay | none |
| M3 | sustained live-input Shadow with no strategy effects | none |
| M4 | bounded real-effect probe with complete reconciliation | probe only |
| M5 | validated exact scope, continuously monitored and reversible | bounded validated only |

Maturity belongs to a versioned capability scope, never the whole bot. `CapabilityManifest` binds dependencies and their maturity, market/route/mode/q band, artifacts, evidence, expiry and demotion rules. A dependency regression, drift, incident or semantic change demotes or disables dependent scopes.

## Required evidence progression

Specification → component tests → deterministic Replay → live-input Shadow → pre-registered predicted-versus-actual plan → bounded Micro-live → scoped validation. Fault injection must cover stale/gap data, malformed events, slow/full disk, backpressure, disconnect, ambiguous submit, partial fill, cancel races, crash/restart, reconciliation mismatch, unsafe infrastructure and model OOD/drift.

Shadow uses the same Core but cannot emit strategy effects. Micro-live is a tiny bounded intervention with declared market/mode/q/time/loss/exposure/stop limits and complete intent→fill→fee→recovery→PnL joins. Prediction-versus-actual metrics and stops are frozen before the probe.

## Operations

P0–P3 incident severity is distinct from `InfraState = HEALTHY / DEGRADED / UNSAFE`. Runbooks must exist for feed gaps, order UNKNOWN, reconciliation mismatch, stuck exposure, risk trip, disk/recorder degradation, clock problems, secret/security incidents, deployment rollback and capability demotion. Alert ownership, escalation and evidence preservation are explicit.

M5 is not permanent. It requires continuous calibration, observed support and reversible demotion. Larger size, new market, new mode, new model, new infrastructure or semantic version is a new evidence scope. Rollback never rewinds exchange truth.

CORR-06 adds HP-001–005 priority fixtures and VP-001–010 profile/Replay fixtures. They test typed IOC/ALO mechanics, cost once, cancel scope, adverse economics, event alignment, clock uncertainty, actual/counterfactual labels, profile expiry, tail-aware ranking, deterministic Replay, FastL1 parity, brief refresh, actual Micro-live precedence and critical Recorder preservation. Approval remains documentary; none of these tests has been implemented or passed in runtime code.

The async gate additionally requires bounded queues/tasks, stale/deadline/cancellation dispositions, no direct worker/effect mutation, no network/disk coordinator wait, deterministic scheduler permutations and safety-event priority under worker/Recorder pressure. Benchmark candidates report P50/P95/P99/P99.9 plus queue, compute, scheduler, state-age, stale/deadline, capture and economic evidence. No runtime test has yet been implemented or passed.
