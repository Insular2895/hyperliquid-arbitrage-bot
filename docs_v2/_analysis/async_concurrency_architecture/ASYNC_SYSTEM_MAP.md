# Async System Map

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

## Concurrency classes

| Class | Name | Meaning | Canonical mutation? |
|---|---|---|---|
| `C0` | `ORDERED_CANONICAL_COMMIT` | total-order consumption, current-version decision and single-owner mutation | yes, by owning ordered reducer only |
| `C1` | `INLINE_BOUNDED_HOT_PATH` | cheap deterministic work on the coordinator path | no independent writer; result consumed inline |
| `C2` | `SNAPSHOT_PARALLEL_COMPUTE` | bounded pure/isolated CPU work on immutable versioned inputs | no; proposal only |
| `C3` | `ASYNC_EXTERNAL_EFFECT` | persistent network I/O, transport, query or external control effect | no; result re-enters as event |
| `C4` | `BACKGROUND_RUNTIME` | local durability, aggregation, health, maintenance and control work | no economic mutation; typed health/control event only |
| `C5` | `OFFLINE_RESEARCH` | Replay campaigns, training, search, Monte Carlo research and reporting | no Live state or authority |

The classes are architectural responsibilities, not required Rust enums, threads or crates. A logical operation may cross classes through typed boundaries; each function row in the matrix names its primary execution class.

## Initial process topology

```text
one OCI client container
└── one main Rust modular-monolith process
    ├── C3 persistent market/account/metadata I/O
    ├── ordered ingress → C0 coordinator
    │   ├── canonical reducers
    │   ├── C1 pair_to_routes / BBO / FastL1 / full-L2 baseline
    │   ├── current Risk → Reservation → immutable plan
    │   └── ordered acceptance/rejection of C2 proposals
    ├── bounded C2 snapshot compute pool
    ├── C3 order/cancel/query effect executor
    ├── bounded Recorder handoff → C4 writer/checkpoint/metrics
    └── local admin, readiness and safe-shutdown control

separate process/resource envelope
└── C5 Replay campaigns / Monte Carlo / training / discovery / search
```

## State and message law

1. Concurrent adapters timestamp and normalize observations, then enter one explicit canonical ordering boundary.
2. Only `C0` mutates `Book`, `Account`, `Fill`, `Inventory`, `Reservation`, Risk, Execution, Recovery, Reconciliation or Accounting truth.
3. `C1` is cheap, bounded and deterministic. It does not block on network, disk or remote services.
4. `C2` receives immutable snapshots plus complete versions, deadline and generation; it returns a proposal. The coordinator may accept only after current-state revalidation.
5. `C3` executes an intention without mutating Core. ACK, timeout, fill and query responses become normalized ordered events.
6. `C4` receives bounded handoffs. Loss or failure is handled by evidence criticality; it never silently blocks the economic coordinator.
7. `C5` is isolated from Live resources and returns only versioned evidence/artifact candidates through existing promotion authority.

## Canonical authorities

| Truth | Only commit authority |
|---|---|
| book/metadata/fee/precision/graph | ordered domain reducer |
| account/fills/inventory/reservations | ordered account/economic reducers |
| Risk state and final permission | Risk owner using current bounded snapshot |
| plan/order/recovery/reconciliation | Execution-family state owners under the ordered coordinator |
| realized accounting | Accounting owner from unique reconciled events |

There is one logical commit order even if domain reducers are distinct modules. Locks, atomics, channels or worker pools cannot create a second authority.

## Baseline versus challengers

| Concern | Initial baseline | Evidence-gated challenger |
|---|---|---|
| affected-route lookup | inline `pair_to_routes` | bounded fanout jobs |
| exact route economics | inline FastL1 eligibility/full L2 | bounded route workers after profiling |
| q-grid | small deterministic inline scan | bounded parallel q evaluations + ordered selection |
| Participant/Simulator | conservative cached/simple bounded path | snapshot inference; F2/F3 worker jobs |
| signing | bounded local inline | only measured local alternative |
| route selection | ordered deterministic set | `BATCH_SELECT` or deterministic `EARLY_COMMIT`, calibrated |

Full L2 remains the economic oracle. Parallelism may change where it is computed, never its semantics.
