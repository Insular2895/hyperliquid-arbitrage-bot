# ExchangeEmulator

## Purpose

Émuler réception, validation, ordre, fill, partial, cancel et unknown.
## Responsibilities

Arrival timing, precision/rules, order lifecycle and account effects.
## Non-responsibilities

Ne génère pas la réponse générale du marché.
## Inputs

ExecutionPlan, ShadowBook, latency distributions, exchange rules.
## Outputs

Order/Fill/Account events identiques aux contrats live.
## Dependencies

PrecisionEngine, FeeEngine, OrderStateMachine, ClockAndRng.
## State

Per-run orders, fills, nonces and account ledger.
## Algorithms / formulas

QF-084 arrival; fill mechanics by declared fidelity.
## Invariants

No atomic batch assumption; fills dedupable; cancel sent≠cancelled.
## Failure modes

Lost response, duplicate/partial fill, reject, timeout, disconnect.
## Risk interactions

Scenarios exercise recovery/reconciliation and reservations.
## Performance requirements

Deterministic for seed; accelerated replay capable.
## Metrics

Outcome rates, timing, rule rejects, parity error.
## Persistence

Emulated events and rule/model versions.
## Configuration

Latency/failure distributions and external rules verified.
## Tests

All state transitions, races, restart, property and live calibration.
## Maturity requirement

M2 before execution core; actual parity improves at M4.
## Open calibrated parameters

Latency/failure/fill distributions and exchange mechanics.
