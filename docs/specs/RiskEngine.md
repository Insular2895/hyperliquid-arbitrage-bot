# RiskEngine

## Purpose

Appliquer la constitution, limites et kill switches.
## Responsibilities

Typed gates order→global, permissions by engine state, reasons/audit.
## Non-responsibilities

Ne maximise pas EV et ne transforme pas hard invariants en penalties.
## Inputs

All point-in-time states, proposal/plan, config/capability.
## Outputs

RiskDecision allow/reject/degrade/halt with evidence.
## Dependencies

Book/Fee/Metadata, Quant, Inventory, Reservation, Execution/Reconciliation.
## State

Limits/utilization, kills/latches, health and config version.
## Algorithms / formulas

Constitutional order, QF-059..066/075/076/109/110.
## Invariants

NO STALE/UNKNOWN/DOUBLE SPEND/BLIND RETRY; no PnL relaxation.
## Failure modes

Missing state, race, config drift, NaN, kill not latched.
## Risk interactions

Is the final policy authority before reserve/submit/continue.
## Performance requirements

Bounded deterministic evaluation; no network/disk.
## Metrics

Gate/reject/kill counts, limit utilization, evaluation latency.
## Persistence

Every decision/kill/config/ack and state refs.
## Configuration

Limits calibrated, versioned, reviewed; no implicit defaults.
## Tests

Invariant/property/concurrency/fault and all permission states.
## Maturity requirement

M2 before execution; M3 shadow; M4 real kill drills.
## Open calibrated parameters

All numeric limits, tail/confidence/drawdown thresholds.
