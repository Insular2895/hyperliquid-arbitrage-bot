# 03 — Test Families: Golden, Property and Integration

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Common test contract

Every test binds requirement IDs, scope/versions, owner, preconditions, input provenance, oracle, expected state/permission/effect, actual result, artifacts/hashes, repeatability, deviations and cleanup. Missing evidence is not a pass.

## Families

- Unit: calculations, guards, reducers and reason mappings.
- Golden: permanent formulas, book-walk, precision/schema and Replay fixtures.
- Property: generated invariant cases with retained minimal counterexamples.
- Integration/contract: adapters, transport/signer, persistence, schema compatibility and external boundaries.
- Fuzz: malformed payloads, serialization, state transitions, overflow and rounding boundaries.
- Load/performance: representative throughput, headroom and tail distributions.

Golden evidence is versioned; intentional authority change creates a reviewed new golden version and preserves the old expected result. Property tests target direction, conservation, monotonicity, idempotence, determinism, no double-spend/effect and safe failure. Integration tests assert economic state and side effects, not just status codes.

Rust/Python parity uses the same canonical vectors and numeric contract. PASS11 owns exact formula-expression/unit audit.
