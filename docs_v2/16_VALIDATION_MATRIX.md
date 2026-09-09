# 16 — Validation Matrix

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

## 1. Purpose and authority

This master defines what evidence must exist before a module, strategy, model, execution mode, market family, size band, infrastructure profile or release can advance. SRC-006 Validation closure is primary; SRC-005 Risk/Data and SRC-004 Formula/Execution retain their domain authority. Earlier ideas supply context only when compatible.

## 2. Constitutional validation rule

Code support, configuration enablement, license entitlement, release stability and validation are separate facts. None implies another. No capital-bearing behavior is permitted without scoped evidence and current Risk/readiness.

## 3. Validation object

Validation applies to an exact tuple: capability/strategy, markets/routes, size range, execution mode, model versions, formula/schema/config identity, release/build, infrastructure profile, evidence interval and restrictions. A broader tuple is a new claim.

## 4. Maturity ladder

The exact ordered levels are `M0 — SPECIFIED`, `M1 — UNIT VALIDATED`, `M2 — REPLAY VALIDATED`, `M3 — SHADOW VALIDATED`, `M4 — MICRO-LIVE VALIDATED`, and `M5 — LIVE VALIDATED`.

## 5. M0 — SPECIFIED

M0 requires purpose, inputs, outputs, invariants, formulas, schemas, error states, planned tests and performance budget. It may precede implementation and confers no runtime permission.

## 6. M1 — UNIT VALIDATED

M1 requires compiling implementation and applicable unit, property and golden evidence, including invalid/boundary/failure cases. It proves local behavior, not realistic Replay or market interaction.

## 7. M2 — REPLAY VALIDATED

M2 requires deterministic point-in-time Replay of historical, failure and counterfactual scenarios, complete RunManifest/version provenance, no lookahead, realistic reducers/transports and reproducible trace evidence.

## 8. M3 — SHADOW VALIDATED

M3 runs the production Core continuously on current live observation through a no-effect transport. It proves feature/support availability, would-decide/would-size/would-execute behavior, latency/stability and drift while producing zero real order effect.

## 9. M4 — MICRO-LIVE VALIDATED

M4 uses real transport, orders, fills and account mutation under strict calibrated limits. It compares predictions with actual latency, fill, slippage, fee, response, Recovery and PnL. It is a calibration probe, not a profit stage.

## 10. M5 — LIVE VALIDATED

M5 requires sustained acceptable economic value after costs, Risk/tail behavior, model/simulator calibration and operational stability in the exact scope. It is bounded, reviewable, reversible and never permanent.

## 11. Critical dependency rule

```text
Maturity(component) <= min(Maturity(critical dependencies))
```

A model cannot outgrow its data/feature contracts; sizing cannot outgrow Simulator/Risk/inventory support; execution cannot outgrow reconciliation; a release cannot outgrow deployment integrity/readiness.

## 12. Level skipping

Decision-affecting or capital/order/Risk/fill capabilities cannot skip Replay, Shadow or Micro-live. A purely technical component such as a parser/config loader may mark live stages not applicable only with documented rationale, contract tests and proof that it cannot change live economic behavior independently.

## 13. Evidence sufficiency

Elapsed time, one aggregate score or one successful path is never sufficient by itself. Evidence covers representative scope/regimes, negative outcomes, missing/invalid intervals, uncertainty, tails, failure recovery and dependency health. Sample sufficiency is declared before results and calibrated to the claim.

## 14. EvidenceId and immutable package

An EvidenceId identifies an immutable package containing claim/scope, requirements, test version, inputs/datasets, run/build/config/model/formula/schema/infra identity, timestamps, seed where relevant, expected and observed results, exclusions/validity, hashes, deviations, reviewer and disposition. Later evidence appends; it does not overwrite the original.

## 15. CapabilityManifest

Source-backed `ValidatedCapability` fields are `strategy`, `market_scope`, `size_range`, `execution_mode`, `model_versions`, `validation_level`, `valid_from`, `last_review`, and `restrictions`. A release carries zero or more entries linked to evidence. Other version identities remain in linked manifests unless Data governance extends the schema.

## 16. Runtime capability intersection

```text
EffectiveCapability = CompiledSupport
                    ∩ ConfiguredEnablement
                    ∩ LicenseEntitlement
                    ∩ ReleaseChannelPolicy
                    ∩ ValidatedCapability
                    ∩ CurrentReadiness
                    ∩ RiskPermission
```

Missing exact coverage yields a machine-readable rejection of new risk. Runtime cannot round up size, substitute a model silently or infer permission from installed code.

## 17. Promotion decision

Promotion is explicit, scoped and audited. The decision references evidence, dependencies, restrictions, validity/review triggers, target maturity, approver, fallback and rollback. Unknown or missing evidence means no promotion.

## 18. Promotion progression

M0→M1 requires local deterministic tests; M1→M2 realistic deterministic Replay; M2→M3 live no-effect evidence; M3→M4 readiness plus bounded intervention plan; M4→M5 supported sustained real evidence. Scope expansion repeats the affected gates.

## 19. Demotion

Invariant failure, UNKNOWN/reconciliation failure, security compromise, artifact incompatibility, model/simulator drift, exchange-rule change, material infrastructure change, incident or expired evidence may reduce size, disable a market/mode/model or demote maturity. Restored health does not silently re-promote.

## 20. Test families

Required families, as applicable, are Unit, Golden, Property, Integration/contract, Replay, Fault Injection, Load, Performance, Shadow, Micro-live and Chaos/drills. Each declares oracle, expected permission/state, evidence artifact and failure behavior.

## 21. Fault-injection standard

Inject stopped, late, stale, lying/corrupt, duplicate, reordered and OOD behavior for each meaningful dependency. Assert economic exposure, state transition, permission, reservation/accounting, alert, evidence and recovery. Merely observing no process crash is not a safety proof.

## 22. Deterministic Replay

```text
DecisionTrace = F(OrderedEvents, ResolvedConfig,
                  ModelArtifacts, FormulaVersion, Seed)
```

Repeated runs compare ordered events, state transitions, Risk decisions, intents, final state/PnL and trace hashes. Parallel completion cannot change ordered commits. Accelerated/checkpoint Replay must equal full Replay in the same semantic mode.

## 23. No-lookahead validation

At decision time T, every event, metadata/fee rule, config, model, formula/schema and feature must have been available by T. Audit lineage to RAW manifests and training/availability boundaries. Historical truth and later-model counterfactual runs carry distinct labels/manifests.

## 24. Shadow validation

Shadow changes only the effect boundary. It records live opportunities, forecasts, decisions, would-submit actions, latency and outcomes while keeping actual and counterfactual accounts separate. It cannot prove real queue fills, causal impact, ACKs, fees, cancel races or real Recovery.

## 25. Micro-live validation

Micro-live uses the same engine with small calibrated Risk/capital limits. The historical EUR 40–50 example is illustrative, not a fixed threshold. Every attempt records predicted and actual execution. Evidence at one size/market/regime/mode cannot authorize another.

## 26. Predicted-versus-actual contract

Compare arrival latency/book/edge, fill probability/quantity/time, slippage/fees, survival, participant response, Recovery and PnL distributions by market, mode, size/depth, spread, volatility, regime, model/fidelity and infrastructure. Include count, missing joins, bias, quantiles, coverage and tails—not just means.

## 27. Model validation

Random row splits are forbidden. Use chronologically ordered train/validation/test and walk-forward OOS; enforce `training_end < validation_start`; retain a naive constant-survival baseline. Required evidence includes Brier, LogLoss, integrated Brier where applicable, calibration curves, safe OOD/fallback, runtime, stability and positive comparable EconomicLift.

## 28. Champion/Challenger and drift

Champion alone may affect decisions; Challenger sees the same features but remains observe-only. A simpler Champion remains if complexity lacks robust incremental value. Feature/support, calibration, error, OOD/disagreement and economic drift are monitored by slice; recalibration and promotion occur offline.

## 29. Simulator validation

F0 validates exogenous history; F1 arrival/mechanical execution; F2 local ShadowBook intervention; F3 calibrated stochastic response; F4 agent-based research. Each level proves only included mechanisms. F3 requires temporal OOS and Micro-live distribution calibration; F4 is not production truth.

## 30. Risk validation

Each applicable invariant has unit/property/fault proof. Same RiskSnapshot/config/models produces the same decision. UNKNOWN reduces capability; rejected opportunities and later outcomes are retained. Kill/reset, hard inventory, CVaR/ES, OOD, config rollback and unsafe-infra cases are mandatory.

## 31. Execution validation

Prove zero/full/partial fills, actual-size propagation, later-leg failure, bounded Recovery, lost submit response without duplicate, fill dedupe, cancel races, crash at journal boundaries, feed loss, reconciliation and restart. No affected READY while orders/balances/reservations are unresolved.

## 32. Data, Recorder and evidence validation

Prove schema roundtrips/compatibility/invalid rejection, immutable RAW/checksums, ordered IDs/time, point-in-time lineage, RunManifest/DecisionTrace reproducibility, non-blocking Recorder priority/backpressure, journal/checkpoint reconstruction and incident-window retention. No notebook-only result supports promotion.

## 33. Graph, formula and inventory validation

Directed conversion/book-side, route continuity, OWA comparator, Triangle closure, topology invalidation and formula parity use properties/golden Replay. Inventory/sizing proves actual balances/reservations, terminal viability, all-gates q search, shared-capacity races and separate route/Recovery/inventory/global PnL.

## 34. Infrastructure validation

B01–B12 evidence covers feed arrival/age, RTT/reconnect/stability, hot-path CPU, jitter/contention, Recorder/storage/RAM and container overhead. Report distributions and clock uncertainty under comparable workload. Upgrade/downgrade also requires attributable robust economic evidence, not technical score or capital alone.

## 35. Deployment/release validation

Prove artifact provenance/integrity, least privilege/read-only runtime, secret absence, config/schema rejection, reconciliation-first startup, safe stop/crash, transactional update/rollback/migration, one owner, license safety, local/redacted diagnostics and client lifecycle. Trading-logic changes require Shadow and Micro-live; exact affected-scope analysis governs other changes.

## 36. Domain Definition of Done

DoD is evidence-backed completion of a declared scope, not a global project label. The canonical domain matrix is [DOMAIN_DEFINITION_OF_DONE_MATRIX.md](_analysis/pass10_validation_operations/DOMAIN_DEFINITION_OF_DONE_MATRIX.md). A missing mandatory test, unresolved critical deviation or unhealthy dependency fails DoD.

## 37. Q_validated and scaling

`Q_validated` is the largest q that passes every gate in current support. Increase only q1→q2→q3-style evidence steps with next-band Simulator, execution, impact/tail/inventory and operational proof. It shrinks on drift, incidents or lost support. Larger account capital and raw book depth do not increase it.

## 38. Market/mode/capital expansion

New markets repeat metadata/formula/Graph/model/Replay/Shadow/Micro-live evidence. MT/MTT requires maker queue/fill/adverse-selection and cancel/Recovery proof. Bridge requires all paths plus STAY, terminal viability and realized relocation/exit evidence. Parallel scale requires shared-capacity/portfolio race proof.

## 39. Incidents and revalidation

Critical incidents can demote M5 immediately. Resume requires containment, current exchange/account reconciliation, fix/rollback proof, affected tests and Replay, then Shadow/Micro-live when assumptions or live behavior changed, followed by explicit re-promotion.

## 40. Revalidation triggers

Triggers include material code/build/config/model/formula/schema/data change, host/runtime/network move, exchange-rule/feed change, size/market/mode expansion, expired evidence, drift/SLO breach, security issue and incident. Model changes revalidate model dependents; FormulaVersion changes revalidate every consumer/golden result; host changes revalidate infra/readiness; exchange changes revalidate affected adapters/markets/modes.

## 41. Scientific reporting

Predeclare hypothesis, primary/guardrail metrics, scope, validity rules and stop/go criteria. Preserve accepted/rejected attempts, negative results and exclusions. Report provenance, uncertainty and counterfactual assumptions. Reproduction must resolve artifacts and recreate the original result/trace.

## 42. PASS boundary and remaining work

PASS 10 defines evidence maturity and operations contracts. The later build/validate/scale journey owns implementation sequencing; the Formula audit owns exact equation/unit verification. Current exchange/platform/security facts require external revalidation. Thresholds, windows, sample sufficiency and tool choices remain calibrated/open.

## 43. CORR-01 — Capture observability validation

M1/M2 evidence must cover deterministic stage projection, unique-ID counts, every rejection/disposition boundary, fan-out/fan-in correlation, episode segmentation/censoring, missing/inferred joins, named timing endpoints/clock validity, non-overlap and denominator-zero/small-sample behavior. Fixtures include proven pre-send failure, ambiguous send, known reject, zero/partial/full fills, intermediate exposure, `UNKNOWN` with late resolution, Recovery success/failure, reconciliation delay and complete positive/zero/negative PnL.

Shadow validates `would_*` completeness/latency only. MicroLive/Live validation freezes decision-time predictions, joins exact actual labels and reports join completeness, calibration, coverage/tails and bias by comparable slice. Instrumentation is tested disabled/enabled under normal/stress load for latency, scheduler, drops, backlog and correctness. Optimization promotion requires the full technical→funnel→economic chain and no safety/replay regression. Details: [Capture Funnel and Latency Attribution](deep-specs/operations/11_CAPTURE_FUNNEL_AND_LATENCY_ATTRIBUTION.md).

## 44. CORR-02 — Performance correctness gates

Correctness evidence is evaluated before performance. Mandatory gates are: C2 safe-reject proof against full L2 over its declared domain; exact FastL1/full QF-016 parity with ineligible fallback; reverse-index membership/order/invalidation and dense↔canonical round-trip; exact-tuple dedup with no distinct state loss; allocation/reuse poison, capacity and failure-semantic tests; queue ordering/loss/duplicate/overflow/shutdown/backpressure stress; and deterministic `DecisionTrace` parity for transparent changes.

Compiler/PGO changes repeat golden/property/Replay/Shadow evidence. A future C++ kernel additionally requires Rust-oracle equality, ABI tests, fuzzing, sanitizers, fault behavior and full escalation approval, never direct Live promotion. Microbenchmark improvement alone cannot promote a change; representative end-to-end, capture and economic evidence is required when material. See the [CORR-02 Validation Matrix](_analysis/corr02_hot_path_performance/CORR02_VALIDATION_MATRIX.md).

## 45. CORR-03 — Failure, label and completion-model validation

M1/M2 must prove authoritative label derivation, pending/censored/invalid handling, immutable point-in-time joins and HJ-001..010 state/inventory/reservation/Recovery/Reconciliation outcomes. Duplicate fills are idempotent; UNKNOWN becomes neither zero nor failure before resolution; recovered and strategy-completed remain distinct.

Completion models use chronological/walk-forward OOS, episode-aware leakage control, constant and simple empirical comparators, QF-095/096 with counts/support, reliability and slice diagnostics, OOD/fallback/runtime tests, immutable artifacts and drift demotion. Random row splits, success-only samples, naïve leg-rate products and decision use based only on AUC/accuracy fail validation. Shadow remains observe-only; actual calibration begins with scoped Micro-live TT, then TTT and maker modes separately. See [CORR-03 Validation Matrix](_analysis/corr03_execution_completion/CORR03_VALIDATION_MATRIX.md) and [Promotion Gate](_analysis/corr03_execution_completion/COMPLETION_MODEL_PROMOTION_GATE.md).

## 46. CORR-04 — Infrastructure/feed validation

M1/M2 prove public-feed ordering/book/gap/reconnect/freshness, strict cross-feed alignment, one canonical writer, deterministic source/epistemic Replay, `S-01..S-10` safety and exact speculative-reuse parity. M3 supplies paired node/challenger Shadow evidence. M4 is possible only after the challenger becomes a validated canonical candidate with one economic owner; no dual-account-owner A/B is permitted.

Docker bridge/host/native and CPU/scheduler/IRQ/network treatments require semantic parity before performance, starvation/resource/reconnect/security guardrails and rollback. Kernel bypass cannot prototype before complete TCP/TLS/WebSocket applicability and least-privilege review. Promotion follows N1–N9/P1–P9 and end-to-end capture/economic evidence, never advertised latency. See [CORR-04 Validation Matrix](_analysis/corr04_infrastructure_execution_path/CORR04_VALIDATION_MATRIX.md).

## 47. CORR-05 — Economic-composition validation

M1/M2 add E0–E9 label goldens, F/P/R/X partition and unresolved-coverage tests, probability-conditioning lint, scenario probability/cashflow exact-once vectors, Recovery-entry/success/loss separation, inventory/exit/stranded and Bridge ownership fixtures, q/state support grids, QF-027/QF-076 divergence cases, disjoint accounting reconciliation and prediction-versus-realized provenance tests.

No product of QF-048/QF-085 and `p_full` passes without an explicitly validated joint decomposition. Infrastructure profiles compare one coherent distribution and incremental cost once. OOD/demotion contracts capacity; positive RAEV never overrides Risk. See [CORR-05 Validation Matrix](_analysis/corr05_economic_integration/CORR05_VALIDATION_MATRIX.md).

## 48. CORR-06 — Priority and infrastructure-profile fixtures

Priority fixtures are mandatory if the capability is implemented: `HP-001` compares the same candidate under zero and nonzero typed policy, changes only supported sequencing/outcomes and charges cost once; `HP-002` preserves zero fill for IOC and therefore zero IOC priority charge when filled notional is zero; `HP-003` uses ALO resting-notional-at-placement and queue semantics rather than IOC logic; `HP-004` tests cancel/ALO/IOC precedence only to documented scope; `HP-005` proves a higher-cost policy may lose economically despite capture improvement.

Infrastructure fixtures are: `VP-001` authoritative paired-event alignment; `VP-002` lead below clock uncertainty gives `INCONCLUSIVE`; `VP-003` stored profile on a new Dataset labels `COUNTERFACTUAL`; `VP-004` stale profile cannot promote; `VP-005` lower mean but worse tails/outages is ranked by declared net/reliability objective; `VP-006` same manifest/profile/seed reproduces; `VP-007` FastL1/full-L2 economic divergence fails; `VP-008` brief challenger refresh creates a new version without permanent rental; `VP-009` Micro-live contradiction overrides simulated fill claim; `VP-010` critical Recorder loss invalidates the experiment and fails safe.

QF-106/QF-108 fixtures include bridge-free equality and nonzero-Bridge global QF-106 reconciliation. Formula count remains 110, equation changes zero. See the [CORR-06 final consistency audit](_analysis/corr06_final_consistency/FINAL_REVIEW_PACKAGE_CONSISTENCY_AUDIT.md).
