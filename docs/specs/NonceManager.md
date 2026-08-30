# NonceManager

## Purpose

Fournir un ordre de signature compatible exchange sans collision.
## Responsibilities

Ownership, monotonic issuance, persistence/reconcile and contention rejection.
## Non-responsibilities

Ne signe pas et n'invente pas les règles exchange.
## Inputs

Signer/account ID, Clock, persisted/exchange evidence.
## Outputs

Nonce lease/value or hard failure.
## Dependencies

Signer, ReconciliationEngine, ClockAndRng.
## State

Single-writer last/leased nonces and process ownership.
## Algorithms / formulas

Selon règle officielle revalidée; monotonic/idempotence contract.
## Invariants

One active writer per account; never reuse/collide silently.
## Failure modes

Clock rollback, concurrent process, lost persistence, exchange rejection.
## Risk interactions

Anomaly disables submits/new risk and reconciles.
## Performance requirements

Bounded local issuance; no remote lookup per opportunity.
## Metrics

Issuance latency, gaps/collisions/rejects/ownership changes.
## Persistence

Durable nonce/ownership journal as required.
## Configuration

Account scope and official nonce policy.
## Tests

Concurrency/crash/clock/restart/duplicate processes.
## Maturity requirement

M1 official fixtures; M3 shadow signing; M4 live.
## Open calibrated parameters

Persistence batching/lease only if exchange contract permits.
