# ExecutionTransport

## Purpose

Envoyer/query/cancel via une interface identique live/emulator.
## Responsibilities

Persistent connections, request correlation, typed errors and responses.
## Non-responsibilities

Ne déduit jamais non-fill d'un timeout et ne retry pas une intention aveuglément.
## Inputs

Signed actions/queries/cancels.
## Outputs

Transport evidence/events to OrderStateMachine.
## Dependencies

Feed/HTTP clients, Signer, Recorder, ClockAndRng.
## State

Connection/session/rate-limit health, request IDs.
## Algorithms / formulas

Protected IOC/ALO encoding per official verified rules.
## Invariants

No blind retry; persistent ready connection; request/intent correlation.
## Failure modes

Timeout/lost response/disconnect/rate limit/reject/malformed response.
## Risk interactions

Ambiguity → UNKNOWN/reconcile; health affects readiness.
## Performance requirements

No connection setup on opportunity; latency instrumented.
## Metrics

Send/response/ack latencies, errors/rate limits/reconnects.
## Persistence

Request/response raw evidence and timestamps.
## Configuration

Endpoints/connections/rate policies external-verified.
## Tests

Mock loss/duplication/timeout/rate/reconnect and official fixtures.
## Maturity requirement

M2 emulator; M3 shadow query; M4 protected submit.
## Open calibrated parameters

Timeout/backoff/connections and current exchange limits.
