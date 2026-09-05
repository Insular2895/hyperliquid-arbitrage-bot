# 06 — Startup, Preflight, Readiness and Onboarding

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Startup state machine

```text
BOOTING -> CONFIGURING -> CLOCK_CHECK -> CONNECTING
        -> SYNCING -> RECONCILING -> RISK_CHECK -> READY
                                      |-> DEGRADED
                                      |-> RECOVERY_ONLY
                                      `-> HALTED
```

Startup verifies image/digest, platform/runtime hardening, exclusive owner, mounts/capacity, ResolvedConfig/schema, signer presence/scope, network/exchange access and clock health. It then acquires metadata, books, account, orders and fills and reconciles in the Execution/Data-owned sequence. Checkpoint/journal state is evidence, never authority over exchange truth.

Any unknown/incompatible/missing prerequisite removes new-risk permission and exposes a stable reason. Recovery can remain available if exposure exists and the required safe authority is present.

## Onboarding gates

`INSTALL` creates/checks declared runtime assets without producing/uploading a key or silently starting Live. `PREFLIGHT` checks correctness and safety. `DIAGNOSTIC` benchmarks CPU, scheduler, memory, disk, clock, feed/API RTT and Docker overhead. `SYNC`/`RECONCILE` establish current truth. `SHADOW` proves no-effect parity. `MICRO-LIVE` proves tightly bounded real behavior. `LIVE` requires explicit promotion.

Unsupported evidence restricts capability rather than being overridden by commercial entitlement. A host can be acceptable for Replay/Shadow yet unvalidated for Live.

## DoD interface

Each gate yields a versioned result tied to installation, digest, config hash, infrastructure identity and time. Promotion is explicit and auditable; evidence expiry or material version change demotes capability and requires re-evaluation. PASS10 owns final evidence thresholds and CapabilityManifest promotion.
