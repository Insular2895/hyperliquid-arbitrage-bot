# Calibration and Learned Items

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## 1. Purpose and Phase-14 authority

This review governs provenance and use of empirical values/artifacts. Phase 14 owns classification of human-policy decisions. Counts are derived inventory facts, never architecture invariants: its current residual OPEN ledger contains 13 `CALIBRATED` and 3 `LEARNED` items; the Formula/QF catalog separately exposes six explicitly learned mathematical interfaces. There is no frozen “60/6” target.

## 2. Definitions and four orthogonal axes

- `CALIBRATED`: a versioned value/policy candidate estimated or tuned under declared evidence.
- `LEARNED`: a versioned relation/distribution/coefficient artifact fitted from data.
- `LOCKED`, exchange rule, safety default, user-tightenable policy, commercial policy, external revalidation and implementation choice retain their own vocabularies; they are not one enum.

Every ledger item separates:

| Axis | Question | Examples |
|---|---|---|
| classification/provenance | what kind of fact is it? | CALIBRATED, LEARNED, LOCKED, EXTERNAL_REVALIDATION |
| evidence stage | when can valid evidence begin? | pre-implementation, Recorder, Replay, Shadow, Micro-live, Live, infra benchmark, offline training |
| activation requirement | when may a consumer use it? | consumer-specific M0–M5 plus critical dependencies |
| authority/owner | who defines/selects/promotes it? | Formula, Risk, Participants, Capital, Infra, Data, Validation, Commercial, Operations |

An observation stage is never an authority. Early evidence does not imply early activation.

## 3. Candidate → validation → promotion lifecycle

```text
measurement/offline learning
  -> immutable candidate artifact
  -> applicable validation and support checks
  -> EvidenceEligibility
  -> human approval only where governance requires it
  -> scoped CapabilityManifest entry
  -> CurrentReadiness ∩ RiskPermission
```

Candidate provenance starts before promotion: dataset/EvidenceId, time/point-in-time boundary, scope, method, feature/formula/schema/build Git versions, hyperparameters, seed where applicable, support, uncertainty, owner, creation time, validity, checksum, fallback and consumers. Promotion adds approval, effective scope, restrictions, validity/revalidation triggers and rollback. Existing EvidenceId, ModelReport, ValidationReport and RunManifest contracts carry this; no new runtime schema is created.

## 4. Calibration rules

Calibration may propose a tighter or broader candidate scope. Safety/config/demotion authority may apply a contraction. Any expansion requires its own consumer-specific evidence and explicit scoped promotion. Measurement alone never increases size, loosens Risk, expands markets/modes/models/profiles or grants permission.

Good evidence at q1 may justify an experiment proposal for q2 only. q2 requires its own Simulator, Execution, Risk, tail, inventory, model, infra and operations evidence. The same rule applies to new market, route, mode, model, feed, regime, maker or VPS scope.

## 5. Learned-artifact rules and exact targets

Learning supplies values/distributions/coefficients consumed by a canonical interface; it cannot redefine the equation, mathematical object, event target, units, signs, ownership, failure semantics or Risk rule.

| QF | Learned object | Exact interface boundary |
|---|---|---|
| QF-045 | Discrete Hazard | conditional bin hazard |
| QF-049 | Expected Edge at Arrival | conditional future-edge distribution expectation |
| QF-050 | Probability Above Threshold | probability from the same versioned future-edge distribution |
| QF-051 | Maker Fill Survival | conditional time-to-fill survival with source-specified target still OPEN where noted |
| QF-081 | Cross-Market Response | conditional target-market change |
| QF-083 | Competition Hazard | global edge-death hazard |

These six are typed interfaces, not a generic `MODEL-LEARNED` bucket. Horizons, cohorts, clipping, thresholds, windows, support/OOD limits and runtime budgets remain independently classified.

Labels preserve `AnyFill`, `FirstFill`, `FullFill`, `PartialFill`, `FilledQuantity`, `FillTime`, `AdverseSelection` and `RecoveryOutcome`. `PENDING`, `CENSORED`, `INVALID` and `UNKNOWN` are not silently zero/failure/negative.

## 6. Formula and Risk boundaries

Formula owns the canonical equation/object/units/sign/domain/undefined semantics and QF version. Calibration may supply allowed inputs but cannot mutate structure. A formula-level undefined result uses the canonical typed invalid/N/A/fail-closed path; it is not replaced by an arbitrary value.

Risk owns hard invariants, gate order, action classes and fail-safe behavior. Threshold values may be calibrated where the constitution permits, but calibration cannot remove/invert a safety rule, bypass OOD, reuse unknown capital or override `NO NEW RISK`.

## 7. Sizing and exact-q validity

The documentary `ValidatedQSet = {q : Gates(q)=TRUE}` is q-specific and potentially non-monotonic; QF-076's scalar `Q_validated = sup(ValidatedQSet)` is only its boundary. `q <= Q_validated` and membership in `size_range` do not prove q valid. Every capital-bearing q must be inside the manifest envelope, supported by linked evidence and pass current gates at that exact q. Grids/bands never create fictitious continuous permission.

## 8. Evidence stage versus activation maturity

A window calibrated in Replay is not therefore usable by a capital consumer at M2. The consumer remains bounded by all applicable critical-dependency maturity/evidence and the full permission intersection. Micro-live/Live evidence from one scope does not transfer automatically.

## 9. Offline learning; no self-promotion

Production runtime may collect immutable outcomes, monitor drift and trigger existing contraction/demotion authority. It may not retrain the Champion, mutate weights, expand support, promote a Challenger, retune Risk or self-promote. The path is offline training/calibration → temporal OOS → candidate → Challenger/Shadow → required Micro-live → explicit promotion → bounded inference.

## 10. Typed bounded fallbacks

“Conservative” is defined by the consuming canonical owner. A supported empirical model fallback operates only inside its own support; otherwise the dependent capability is disabled. Missing mandatory Risk calibration means the Risk-defined no-new-risk action, not `parameter=0`. Insufficient infra evidence retains the current validated profile or blocks promotion. A fallback never widens authority.

## 11. Freshness, expiry, invalidation and re-promotion

No universal expiry cadence exists. Each artifact declares versioned validity, drift/invalidation and revalidation triggers. Stale/expired/invalid/unsupported evidence contracts the affected scope. Restored health or a retrained candidate does not silently restore maturity; explicit evidence and re-promotion remain necessary.

## 12. Test tolerances

Operational/statistical tolerances may be calibrated with unit, population, method, uncertainty and consumer. Correctness tolerances cannot weaken exact identity/order, conservation/accounting, schema validity, deterministic Replay, Risk invariants or exact Formula goldens. Approximation is permitted only where the canonical contract explicitly defines it and evidence proves the bound.

## 13. Recorder and infrastructure

Queue/chunk/storage capacities, watermarks, sampling of noncritical analytics and operational windows may be calibrated. Append-only truth, critical evidence preservation, explicit loss/invalid regions, ordering, non-blocking hot path and no false completeness are not calibrable away.

InfraProfile distributions, uncertainty, freshness and economic comparison are evidence. Provider/region/network winners are benchmark-selected, not manually declared; faster median alone cannot promote. Current exchange/provider/node/API facts remain external revalidation, not internal calibration.

## 14. Commercial, user and human boundaries

Commercial policy is not an evidence stage. License entitlement and release policy may only intersect/reduce EffectiveCapability; premium access cannot promote a model, expand q/market/mode, weaken Risk or validate infra. User-tightenable parameters may tighten below validated maximum, never loosen beyond it.

A human may approve/narrow/defer/reject an evidence-eligible promotion where governance requires it. Human approval is not arbitrary parameter selection and cannot rescue failed evidence.

## 15. Documentation ledger

The [Phase-15 ledger](../_analysis/phase15_calibration_learned/CALIBRATION_LEARNED_LEDGER.md) records source IDs, classification, owner, evidence stage, activation maturity, provenance, support/uncertainty, fallback, promotion, consumers and invalidation triggers. Existing REQ/QF/OPEN IDs remain authoritative; no competing economic IDs are introduced.

## 16. Acceptance invariants

Observed improvement never auto-increases size. Learned safety cannot bypass Risk. Premium license cannot enable unvalidated capability. Calibration cannot alter Formula. Missing evidence is not guessed zero. Interior q is not automatically valid. Retraining does not deploy. Health recovery does not re-promote. Replay calibration does not imply Live use. A faster VPS does not cause an automatic switch. No numeric threshold or universal cadence is selected here.
