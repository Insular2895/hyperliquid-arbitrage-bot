# ReconciliationEngine

## Purpose

Aligner état local avec vérité exchange avant nouveau risque.
## Responsibilities

Fetch/stream sync, compare orders/fills/balances/fees/reservations and resolve.
## Non-responsibilities

Ne restaure pas un checkpoint ancien comme vérité.
## Inputs

Local ledgers/checkpoints and exchange account/open-order/fill evidence.
## Outputs

ReconciliationState/events, verified snapshot or escalation.
## Dependencies

ExecutionTransport, OrderStateMachine, Inventory/Accounting/Reservation.
## State

RECONCILE_REQUESTED/FETCHING/COMPARING/RESOLVING/CONSISTENT ou UNRESOLVED.
## Algorithms / formulas

Set/ledger comparison and idempotent missing-event application.
## Invariants

Exchange truth wins; no new risk until VERIFIED.
## Failure modes

API unavailable/inconsistent, pagination gap, duplicate, unresolved balance.
## Risk interactions

Forces RECONCILING/RECOVERY_ONLY/HALTED; may trigger recovery.
## Performance requirements

Correctness over latency; bounded retries/backoff and operator visibility.
## Metrics

Duration/discrepancies/resolutions/failures/retries.
## Persistence

Queries/evidence/diffs/actions and final proof.
## Configuration

Sources/backoff/escalation; no automatic optimistic resolution.
## Tests

Restart, lost response, late/duplicate fills, partial pages, outage.
## Maturity requirement

M2 emulator; M3 live account; M4 prerequisite.
## Open calibrated parameters

Retry/escalation time and evidence freshness.
