# Risk Validation Map

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

SRC-006 lines 4550–4589 requires unit/property/fault testing per constitutional invariant and the explicit tests below. Exact performance/tolerance values are calibrated.

| Requirement | Unit/boundary | Property/adversarial | Fault/replay/shadow/micro-live evidence | Acceptance |
|---|---|---|---|---|
| All `INV-001..030` | Each parser/gate/transition boundary | Random event/order/size sequences | Relevant dependency failure injection | No invariant bypass; evidence ID per invariant |
| No stale trade | Age and boundary around threshold | Route age equals worst leg | Delayed/gapped feed, maker rest | No affected new send; reason recorded |
| Unknown state | Order/balance/account unknown cases | Unknown capital never reused | Lost HTTP/account disconnect/restart | No double spend; reconciliation restores truth |
| Hard inventory | Band boundary/quantization | No NEW_RISK outside hard band | Partial fill pushes existing exposure out | Only strict reducing action may improve violation |
| CVaR/ES gate | Alpha/limit/invalid distribution | Positive EV cannot bypass tail limit | Replay/stress tail scenarios | Exceeded bound rejects/resizes within support |
| OOD gate | Hard/soft boundaries, invalid/NaN | Mandatory hard OOD not bypassed by size | New regime/asset/size and missing artifact | Conservative fallback or dependent disable |
| Infra unsafe | State transitions/hysteresis | Unsafe cannot create new risk | Clock/feed/CPU/network/disk failures | Correct scope/action, safety work priority |
| Determinism | Stable serialization/version refs | Same snapshot/config/models → same decision | Replay with ordered concurrent events | Identical decision trace/hash |
| Performance | Gate/stage timing | Load and fast-reject path | Soak/stress with recorder | P50/P95/P99/P99.9 measured; bound evidence supplied |
| Risk-reducing exception | Strict improvement predicate | Cannot relabel risk increase as reduction | Recovery partial/failed exits | Known exposure + all RecoveryRiskPolicy bounds |
| Optimizer subordination | Eligible-set input | Rejected route never selected | Multi-opportunity/shared resources | Optimizer sees only safe set |
| Config/client floor | Range/order/provenance | Tighten only; no invariant disable | Malformed/mid-transition/update rollback | Invalid prevents READY; pinned version stable |
| Kill/degrade/reset | Each scope/action/latch | Narrow dependency isolation | Trigger, restart, reset/ack drills | No auto-retrade; readiness reruns |
| Reject/audit dataset | Reason enum/version | Every result attributable | Same-data/different-config replay | Accepted and rejected cases analyzable |
| Scaling | Candidate size grid/bound | `q*≤Q_validated`; no capital-only increase | Shadow/micro-live/tail/recovery/infra | Evidence-bound promotion only |

## Fault-injection minimum set

Stale/missing/corrupt market feed; crossed/gapped book; unknown balance/order; duplicate event/fill; lost submit response; model unavailable/NaN/OOD/drift; Simulator miscalibration; infrastructure/clock/scheduler degradation; invalid config; reservation inconsistency; disk full/recorder backlog; exchange disconnect; reconciliation failure.

## Definition of done

- 30/30 invariants have an applicable test mapping.
- Mandatory SRC-006 stale, unknown, hard inventory, CVaR, OOD, infra, determinism and percentile measurements are present.
- Reason, snapshot, config/model/schema versions and state transitions are replayable.
- Kill/reset and startup/shutdown paths cannot enter READY without reconciliation/risk health.
- Live/scaling permission is constrained by the validated capability manifest and a human promotion decision.
