# OrderStateMachine

## Purpose

Représenter sans ambiguïté le lifecycle d'une intention/ordre.
## Responsibilities

Transitions, dedupe, CLOID mapping, fills/cancel/unknown/terminal evidence.
## Non-responsibilities

Ne décide pas route/recovery et ne libère pas seul les resources.
## Inputs

OrderIntent, transport responses, order/fill/account events.
## Outputs

OrderState events and actual filled totals.
## Dependencies

ExecutionTransport, Recorder, ReconciliationEngine.
## State

Per OrderIntent/CLOID/exchange ID plus append-only fill set.
## Algorithms / formulas

`CREATED→NONCE_ASSIGNED→SIGNED→SENT→PENDING_RESOLUTION`, branches
`RESTING/PARTIALLY_FILLED/FILLED/CANCEL_REQUESTED/CANCELED/REJECTED/UNKNOWN`,
puis `TERMINAL_RECONCILED`; reducers idempotents.
## Invariants

SENT may fill; cancel sent≠cancelled; fill applied once; no blind retry.
## Failure modes

Duplicate/out-of-order event, missing ACK, cancel race, late fill.
## Risk interactions

UNKNOWN retains exposure/reservation and requests reconcile.
## Performance requirements

Bounded event apply and lookup.
## Metrics

Transitions, time-in-state, duplicates, unknown/late fills.
## Persistence

Intent, transitions, fill ledger and correlations.
## Configuration

Timeouts only trigger uncertainty actions, not non-fill assumptions.
## Tests

Exhaustive transition/property/race/restart/idempotence.
## Maturity requirement

M2 emulator; M3 live event shadow; M4 real.
## Open calibrated parameters

ACK/cancel/expiry timers.
