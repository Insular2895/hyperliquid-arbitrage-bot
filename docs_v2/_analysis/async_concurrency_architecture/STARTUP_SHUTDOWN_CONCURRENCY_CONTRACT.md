# Startup and Shutdown Concurrency Contract

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

## Startup

```text
BOOT
→ load/verify local build, config, schemas, formula and required artifacts
→ initialize bounded queues/pools and state owners
→ start Recorder/journal and I/O adapters
→ establish clock/feed/book/account/rule health
→ query orders → fills → balances
→ restore compatible checkpoint + journal only as acceleration/evidence
→ reconcile canonical state and ownership
→ validate Risk/capability/readiness
→ READY
```

Required artifacts are local, hash-verified and compatible before READY. A remote model, archive, licensing service or telemetry backend is not a synchronous hot-path prerequisite. Licensing follows its cached/fail-safe commercial policy; it never blocks cancellation, Recovery, Reconciliation or safe shutdown.

No adapter or worker callback can independently publish READY. Starting tasks concurrently is allowed only where dependencies permit; readiness transition is one ordered decision after all required evidence. Background/model/Atlas failure disables or contracts the dependent optional capability rather than inventing state.

## Shutdown

1. Enter ordered `DRAINING`: stop new opportunities/risk-increasing intents.
2. Keep account/fill ingress, safety timers, cancel, Recovery and reconciliation alive.
3. Cancel/supersede optional C2 work; correctness remains protected by generation checks.
4. Resolve or explicitly retain `UNKNOWN`, active orders, exposure and reservations.
5. Capture coherent checkpoint cursor if safe; drain P0 Recorder evidence within a bound.
6. Close manifests/artifacts only when complete; mark incomplete otherwise.
7. Stop external adapters/effect executor after safety work and record unresolved external effects.
8. Release fenced ownership last. Deadline expiry escalates; it never produces false clean shutdown.

Restart after crash, shutdown during execution or `UNKNOWN` always returns through reconciliation. Persisted READY, worker memory or queue contents are not trusted.
