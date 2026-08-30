# Signer

## Purpose

Signer des intents normalisés avec le secret client isolé.
## Responsibilities

Canonical payload, domain separation, key access and zeroization best effort.
## Non-responsibilities

Ne choisit pas ordre/nonce et ne logge jamais le secret.
## Inputs

Normalized order/action, nonce, account/domain.
## Outputs

Signed payload or typed secure failure.
## Dependencies

NonceManager, PrecisionEngine, Deployment secret provider.
## State

Key handle minimal; no secret serialization.
## Algorithms / formulas

Official signing specification revalidated/versioned.
## Invariants

Exact payload signed; environment/account bound; secrets never persisted/logged.
## Failure modes

Missing/revoked key, wrong domain, memory/log leak, malformed payload.
## Risk interactions

Failure disables submit/new risk; compromise invokes incident runbook.
## Performance requirements

Measured/bounded; no external SaaS call.
## Metrics

Sign latency/errors without sensitive material.
## Persistence

Only audit metadata/fingerprint/version, never key.
## Configuration

Secret path/provider/permissions and environment identity.
## Tests

Official vectors, wrong domain, permissions, redaction, rotation.
## Maturity requirement

M1 vectors/security; M3 shadow; M4 live.
## Open calibrated parameters

Key backend/zeroization implementation and latency budget.
