# 16 — Validation Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

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
