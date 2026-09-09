# 19 — Build / Validate / Scale Journey

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

## 1. Purpose

This document explains the evidence journey from an empty data directory to sustained, scoped Live trading. It defines what the project must observe, reconstruct, learn and validate before capital permission can expand. It is not a calendar, capital target or implementation authorization.

## 2. Why this differs from the implementation roadmap

[Technical Implementation Roadmap](17_IMPLEMENTATION_ROADMAP.md) answers **what to build and in which dependency order**. This journey answers **when evidence has earned the right to trust a specific capability with capital**. Technical Phase 3 Recorder serves nearly every later evidence stage; Stage 10 Micro-live requires many technical phases. The two axes are deliberately not 1:1.

## 3. Scientific philosophy

```text
Hypothesis → Measurement → Experiment → Evidence → Decision
```

No serious model claim without target data. No complexity before a simple baseline. No model/release/size is promoted because it looks sophisticated. Negative evidence, rejects, partials, UNKNOWN, Recovery, bad capacity increases and failed Bridge decisions remain useful results.

## 4. Evidence before capital

```text
SPECIFICATION → IMPLEMENTATION → EVIDENCE
→ VALIDATED CAPABILITY → CAPITAL
```

Implemented does not mean validated. More capital does not mean more size. Capital cannot increase `Q_validated`; evidence can increase or decrease it. The CapabilityManifest is the bridge between evidence and a precise market/mode/size/model/infra/version permission. Risk still decides every action.

Permanent roadmap shorthand: **Recorder first**; **Replay before advanced models**; same Core across Replay/Shadow/Live; Micro-live as a measurement instrument; **M5 reversible**. There is **no coding before human approval** after PASS 13–16 review.

## 5. Stage overview

| Stage | Name | Capital ceiling |
|---:|---|---|
| 0 | SPECIFY | None |
| 1 | OBSERVE / RECORD | None |
| 2 | RECONSTRUCT | None |
| 3 | MAP | None |
| 4 | IDENTIFY | None |
| 5 | REPLAY | None |
| 6 | SIMULATE | None |
| 7 | SHADOW LIVE | None |
| 8 | PREDICTED VS ACTUAL PREPARATION | None |
| 9 | LEARN COMPETITION / SURVIVAL | None normally |
| 10 | MICRO-LIVE | Probe |
| 11 | VALIDATE TT | Validated bounded |
| 12 | VALIDATE TTT | Separate probe→validated bounded |
| 13 | MAKER INTELLIGENCE | None / dedicated measurement probe |
| 14 | VALIDATE MT / MTT | Separate probe→validated bounded |
| 15 | CAPITAL INTELLIGENCE | Existing validated scopes |
| 16 | PORTFOLIO ALLOCATION | After separate promotion |
| 17 | BRIDGE / CAPITAL RELOCATION | Separate probe→validated bounded |
| 18 | HORIZONTAL SCALE | Scaled validated |
| 19 | VERTICAL SCALE | Scaled validated |
| 20 | INFRASTRUCTURE SCALE | No direct capital grant |

## 6. Stage 0 — SPECIFY

- **OBJECTIVE / WHY:** eliminate critical ambiguity before code can crystallize accidental architecture.
- **WE MUST ALREADY KNOW:** source authority, project scope and which facts remain external/open.
- **COMPONENTS / ACTIVATE:** domain masters, Formula/Risk/Execution/Data/Validation contracts, requirement ledger and test plans; activate no runtime capability.
- **RECORD / MEASURE / LEARN:** decisions, assumptions, open items, expected inputs/outputs/invariants/failures, traceability and planned evidence. Learn whether the capability can be implemented without invention.
- **CAPITAL / M0–M5:** none; exit is M0 for the declared scope.
- **DATA / FORMULAS / MODELS:** no market dataset required; QF dependencies and units are mapped, not implemented; no predictive model.
- **FAILURE / EXIT / NEXT:** critical ambiguity, missing owner or contradiction stops. Exit when purpose/contracts/formulas/schemas/errors/tests/performance budget are explicit. Next stage receives an implementable final-interface scope.
- **LIMITATION:** M0 proves specification completeness, not correctness or usefulness.

## 7. Stage 1 — OBSERVE / RECORD

- **OBJECTIVE / WHY:** create trustworthy source evidence before prediction; data that was never captured cannot be reconstructed later.
- **WE MUST ALREADY KNOW:** Phase-1 envelopes/clock/order and adapter boundary.
- **COMPONENTS / ACTIVATE:** Hyperliquid adapters, Recorder, Clock/source quality; live observation only.
- **RECORD / MEASURE / LEARN:** raw market/metadata/account/clock events, receive order, gaps, checksums, throughput, activity, topology and feed quality. Learn source rates, availability and failure modes.
- **CAPITAL / M0–M5:** none; M1 capture foundations and continuing soak.
- **DATA / FORMULAS / MODELS:** `RawEvent`, `RawChunkManifest`; no alpha formula or model authority.
- **FAILURE / EXIT / NEXT:** silent loss, ambiguous order or critical durability stops. Exit with admissible data/quality support. Next receives source truth for reconstruction.
- **LIMITATION:** RAW proves local observation, not exchange correctness.

## 8. Stage 2 — RECONSTRUCT

- **OBJECTIVE / WHY:** derive valid books and boundary state before searching for economics.
- **WE MUST ALREADY KNOW:** ordered RAW and current/historical metadata/fee/precision interpretation.
- **COMPONENTS / ACTIVATE:** Normalizer, Book, Metadata, Fee, Precision and checkpoints; no strategy effect.
- **RECORD / MEASURE / LEARN:** normalized events, snapshots/diffs, gaps/resync, BookVersion, rule versions and state hashes. Measure divergence/freshness/coverage and learn which regions are valid.
- **CAPITAL / M0–M5:** none; M1 reconstruction.
- **DATA / FORMULAS / MODELS:** DatasetId and point-in-time boundary data; QF-001–016 inputs; no predictive model.
- **FAILURE / EXIT / NEXT:** gaps, silent repair, invalid/crossed book, rule ambiguity or nondeterminism stop. Exit with reproducible RAW→normalized→BookState. Next receives point-in-time state.
- **LIMITATION:** a correct book is not an opportunity.

## 9. Stage 3 — MAP

- **OBJECTIVE / WHY:** know legal structures and supported market places before selecting where to trade.
- **WE MUST ALREADY KNOW:** valid metadata and reconstructed books.
- **COMPONENTS / ACTIVATE:** venue-aware Graph, precomputed Direct/Route2/Cycle3, `pair_to_routes`, Watcher and early structural Atlas.
- **RECORD / MEASURE / LEARN:** topology, dependencies, route counts, capital reachability, basic liquidity/support and changes. Learn what can exist, not what is profitable.
- **CAPITAL / M0–M5:** none; M1/M2 map capability.
- **DATA / FORMULAS / MODELS:** GraphVersion/RouteDefinition/AtlasVersion; QF-017–023; simple structural rules only.
- **FAILURE / EXIT / NEXT:** invalid continuity, comparator confusion, duplicate/stale route or future leakage stops. Exit with reproducible legal universe. Next receives route candidates.
- **LIMITATION:** a route is structure; an opportunity is current size-specific economics.

## 10. Stage 4 — IDENTIFY

- **OBJECTIVE / WHY:** detect exact economic candidates and their rejection reasons without claiming execution success.
- **WE MUST ALREADY KNOW:** coherent book, graph, fees, precision and FormulaVersion.
- **COMPONENTS / ACTIVATE:** NetConvert/Formula Core and Basic Opportunity Engine.
- **RECORD / MEASURE / LEARN:** affected-route evaluations, BBO C1–C4 dispositions, full-L2/FastL1/fallback counts, exact direct/indirect/triangle output, `Edge(q)`, fees/rounding/minimum failures and opportunity episodes. Learn frequency, safe-filter quality and size dependence.
- **CAPITAL / M0–M5:** none; M1 formulas and M2 opportunity evidence.
- **DATA / FORMULAS / MODELS:** QF-001–027; no advanced Participant model required.
- **FAILURE / EXIT / NEXT:** parity/unit/sign/precision/depth or comparator failure stops the economic claim. Exit with reproducible candidate/reject episodes. Next receives a measurable deterministic baseline.
- **LIMITATION:** positive theoretical/executable-book edge is not Risk permission or realized PnL.

## 11. Stage 5 — REPLAY

- **OBJECTIVE / WHY:** prove what the same Core would decide using only information available at each historical instant.
- **WE MUST ALREADY KNOW:** valid DatasetId, resolved config, formula/model/schema versions and deterministic order.
- **COMPONENTS / ACTIVATE:** ReplayClock, RNG, RunManifest, same reducers/Core, simulated transport and DecisionTrace.
- **RECORD / MEASURE / LEARN:** opportunities, rejects, Risk decisions, plans, execution/recovery traces, final state/PnL, hashes and checkpoints. Learn historical behavior and failure response.
- **CAPITAL / M0–M5:** none; M2.
- **DATA / FORMULAS / MODELS:** point-in-time data and all configured QFs; only declared baseline models.
- **FAILURE / EXIT / NEXT:** nondeterminism, lookahead, invalid region, hidden clock/RNG or separate strategy logic stops. Exit with repeatable trace/hash and checkpoint parity. Next receives trusted experimental substrate.
- **LIMITATION:** Replay cannot prove counterfactual causal market response.

## 12. Stage 6 — SIMULATE

- **OBJECTIVE / WHY:** estimate distributions of execution outcomes under explicit F0/F1 assumptions before capital.
- **WE MUST ALREADY KNOW:** deterministic Replay, actual exchange mechanics contracts and candidate q.
- **COMPONENTS / ACTIVATE:** F0 Historical then F1 latency/mechanical Simulator, arrival book, partial/failure/Recovery scenarios.
- **RECORD / MEASURE / LEARN:** full/partial/failure/recovery probabilities, latency, fills, slippage, fees, PnL quantiles/tails and confidence. Learn hypotheses to test in reality.
- **CAPITAL / M0–M5:** none; M2 by fidelity.
- **DATA / FORMULAS / MODELS:** QF-009–016, 026–027, 040–043, 056–063, 076, 079–080, 084–085, 095–104; empirical latency/mechanics.
- **FAILURE / EXIT / NEXT:** single deterministic PnL, unsupported mechanics/bias or inflated fidelity stops. Exit with reproducible distributions and stated limitations. Next receives pre-live forecasts.
- **LIMITATION:** F0/F1 cannot prove maker queue or participant response.

## 13. Stage 7 — SHADOW LIVE

- **OBJECTIVE / WHY:** prove the full real-time Core, state and operations without placing strategy orders.
- **WE MUST ALREADY KNOW:** critical components M2, real deployment/readiness and no-effect transport.
- **COMPONENTS / ACTIVATE:** live adapters/books/opportunity/Risk/sizing/plans/reconciliation with Shadow transport.
- **RECORD / MEASURE / LEARN:** would-trade/size/submit decisions, live latency/staleness/rejects, state/trace completeness, opportunity outcomes and stability. Learn real-time support and false positives.
- **CAPITAL / M0–M5:** none; M3.
- **DATA / FORMULAS / MODELS:** `ShadowRun`, live point-in-time events, configured formulas and baseline models.
- **FAILURE / EXIT / NEXT:** strategy account mutation, leak/instability, stale state, incomplete evidence, owner/rollback/readiness failure stops. Exit with sustained scoped Shadow validation. Next receives credible pre-intervention forecasts.
- **LIMITATION:** Shadow cannot prove real fill, queue priority, causal impact, ACK/cancel races, actual fees or Recovery.

## 14. Stage 8 — Predicted-versus-Actual preparation

- **OBJECTIVE / WHY:** prevent post-hoc success criteria by declaring comparisons before any real probe.
- **WE MUST ALREADY KNOW:** Shadow forecast fields, intended TT scope and all stable correlation IDs.
- **COMPONENTS / ACTIVATE:** ValidationPlan, evidence joins, guardrails/stopping rules, no capital yet.
- **RECORD / MEASURE / LEARN:** declare predictions for arrival, fill/partial/time, slippage, fees, Recovery, PnL and `Q_validated`; define support slices, missingness, bias, quantiles, coverage and tails.
- **CAPITAL / M0–M5:** none; M3 preparation.
- **DATA / FORMULAS / MODELS:** QF-095–104 error/calibration contracts and QF-105–110 accounting identities.
- **FAILURE / EXIT / NEXT:** unjoinable predictions, missing source of truth or unbounded probe stops. Exit with approved pre-registration and rollback. Next receives an auditable experiment.
- **LIMITATION:** a plan is not evidence that predictions are correct.

## 15. Stage 9 — Learn Competition / Survival

- **OBJECTIVE / WHY:** learn how opportunities die and whether they can be captured, after episodes exist.
- **WE MUST ALREADY KNOW:** point-in-time opportunity episodes, censoring, microstructure and live Shadow observations.
- **COMPONENTS / ACTIVATE:** Survival/Capture/Liquidity/Cross-Market simple Champion and observe-only Challengers.
- **RECORD / MEASURE / LEARN:** duration, hazard, correction velocity, cause, survival, capture, resilience and sparse cross-market response by support. Learn whether predictions outperform a naive constant baseline.
- **CAPITAL / M0–M5:** none normally; M2 temporal OOS, M3 Shadow.
- **DATA / FORMULAS / MODELS:** QF-044–050, 081–083, 095–104; simple empirical model first.
- **FAILURE / EXIT / NEXT:** absent labels, leakage, poor calibration/OOD or no EconomicLift retains baseline. Exit only for supported slices. Next receives calibrated competition evidence.
- **LIMITATION:** learning may run in parallel; it does not block initial opportunity recording or necessarily the first conservative TT probe.

## 16. Stage 10 — MICRO-LIVE

- **OBJECTIVE / WHY:** observe real exchange intervention under minimal, bounded and recoverable exposure.
- **WE MUST ALREADY KNOW:** Recorder/Risk/ESM/transport/Recovery/Reconciliation/accounting/ops/Shadow/rollback are current and the experiment is predeclared.
- **COMPONENTS / ACTIVATE:** first normal execution is same-venue Hyperliquid spot TT, OWA only with valid direct comparator.
- **RECORD / MEASURE / LEARN:** prediction→intent→send→ACK→fills→fees→slippage→remaining→Recovery→actual PnL→reconciliation. Learn real transport, partials, tails and model error.
- **CAPITAL / M0–M5:** probe only; M4 candidate. The historical `€40–50` example is illustrative, not a fixed/minimum/production size.
- **DATA / FORMULAS / MODELS:** `MicroLiveRun`, all TT execution/accounting QFs; conservative supported models/fallbacks.
- **FAILURE / EXIT / NEXT:** safety incident, unresolved UNKNOWN, recovery/reconcile/accounting/evidence/security failure, OOD or unsupported tail stops immediately. Exit with usable real calibration evidence, not automatic Live. Next receives TT actuals.
- **LIMITATION:** tiny probes measure mechanics; they do not validate large size.

## 17. Stage 11 — Validate TT

- **OBJECTIVE / WHY:** promote the simplest taker→taker capability before adding a third leg or maker uncertainty.
- **WE MUST ALREADY KNOW:** sufficient supported TT probes and current dependency health.
- **COMPONENTS / ACTIVATE:** TT direct/OWA scopes one market/route/size/regime/version at a time.
- **RECORD / MEASURE / LEARN:** real slippage/fill/latency/partial/Recovery/PnL errors, tails, state consistency and capacity by q. Learn `Q_validated` for the exact scope.
- **CAPITAL / M0–M5:** validated bounded; M4 then sustained scoped M5 only by explicit promotion.
- **DATA / FORMULAS / MODELS:** QF-016–027, 044–063, 073–080, 095–110 as consumed.
- **FAILURE / EXIT / NEXT:** insufficient sample/support, rising error, tail/recovery/ops degradation or incident blocks/demotes. Exit with CapabilityManifest TT scope. Next gains a trusted baseline and comparison anchor.
- **LIMITATION:** TT evidence does not validate TTT, MT, other markets or larger q.

## 18. Stage 12 — Validate TTT

- **OBJECTIVE / WHY:** separately validate the extra leg, latency and intermediate exposure of taker→taker→taker.
- **WE MUST ALREADY KNOW:** TT is validated; TTT route closure, ESM and per-leg Recovery are M3-capable.
- **COMPONENTS / ACTIVATE:** Triangle TTT through Replay→Shadow→separate Micro-live probes.
- **RECORD / MEASURE / LEARN:** prediction/arrival/output/fill per leg, completion probability, intermediate inventory, partial/failure/recovery and terminal/tail PnL. Learn TTT-specific q/support.
- **CAPITAL / M0–M5:** separate probe then validated bounded; M4/M5 scoped.
- **DATA / FORMULAS / MODELS:** QF-021–023 plus execution/outcome/risk/accounting families; advanced Participant model only if that TTT capability explicitly consumes it.
- **FAILURE / EXIT / NEXT:** applying TT evidence to TTT, planned instead of actual output, unresolved intermediate exposure or unsupported tail stops. Exit with separate TTT CapabilityManifest scope.
- **LIMITATION:** TTT can be detected/replayed/shadowed before sophisticated models; model dependency is capability-specific, not universal.

## 19. Stage 13 — Maker Intelligence

- **OBJECTIVE / WHY:** collect and validate queue/fill/adverse-selection evidence before maker-led execution.
- **WE MUST ALREADY KNOW:** maker arrival/rest/cancel/fill evidence can be labeled; L2 uncertainty is explicit.
- **COMPONENTS / ACTIVATE:** maker observe/Shadow, F2 queue modes and simple empirical fill Champion; no normal MT Live.
- **RECORD / MEASURE / LEARN:** queue proxy/observability, fill survival, time/quantity/partial, cancel/expiry, edge survival while resting, adverse selection and later-leg/recovery conditions.
- **CAPITAL / M0–M5:** none normally; separately approved measurement probes only; M2/M3.
- **DATA / FORMULAS / MODELS:** QF-051–055, 058, 095–104; pessimistic/optimistic sensitivity plus calibrated probabilistic baseline.
- **FAILURE / EXIT / NEXT:** ALO availability without data, severe queue ambiguity, miscalibration/OOD or no lift stops promotion. Exit with supported maker forecast. Next receives MT/MTT experiment inputs.
- **LIMITATION:** code support and order-type support are not behavioral validation.

## 20. Stage 14 — Validate MT / MTT

- **SEPARATE GATES:** `VALIDATE MT` and `VALIDATE MTT`; one mode's evidence never promotes the other.
- **OBJECTIVE / WHY:** validate maker→taker and maker→taker→taker as distinct capabilities.
- **WE MUST ALREADY KNOW:** maker forecast/F2 support, cancel/expiry handling, taker continuation and Recovery are proven.
- **COMPONENTS / ACTIVATE:** MT first where supported; MTT separately; TM/MM remain default-disabled.
- **RECORD / MEASURE / LEARN:** actual maker fill/time/partial/adverse, edge at fill, actual output, later-leg fills, cancel/recovery, fees and terminal PnL by mode/q.
- **CAPITAL / M0–M5:** separate probe then validated bounded; M4/M5 per exact mode.
- **DATA / FORMULAS / MODELS:** maker QFs, QF-025 ExecutionAlpha, outcome/tail/sizing/recovery/accounting families.
- **FAILURE / EXIT / NEXT:** fill/adverse/recovery miscalibration, unsupported queue/regime or using MT proof for MTT stops. Exit with mode-specific CapabilityManifest.
- **LIMITATION:** successful ALO placement alone proves nothing about profitable/safe maker execution.

## 21. Stage 15 — Capital Intelligence

- **OBJECTIVE / WHY:** learn where capital is productive, reachable and safely exit-capable after real opportunity statistics exist.
- **WE MUST ALREADY KNOW:** actual inventory/reservations, Atlas history, terminal viability, current `Q_validated` and exits.
- **COMPONENTS / ACTIVATE:** enriched Atlas, Inventory, Sizing, capital utility and action taxonomy; only existing validated strategy scopes use capital.
- **RECORD / MEASURE / LEARN:** capital reachability, opportunity/capture per capital-time, exit/stranded/idle cost, utilization, bands and capacity drift. Learn which states are useful, not merely liquid-looking.
- **CAPITAL / M0–M5:** no new strategy permission; existing bounded scopes only.
- **DATA / FORMULAS / MODELS:** QF-064–077 and QF-105–108; empirical utility/exit models.
- **FAILURE / EXIT / NEXT:** raw route count/balance, missing exit or no point-in-time support blocks conclusion. Exit with supported capital-state and q curves. Next receives allocation inputs.
- **LIMITATION:** Strategy, Bridge, Rebalance, Recovery and Stay remain distinct.

## 22. Stage 16 — Portfolio Allocation

- **OBJECTIVE / WHY:** move from one opportunity at a time to jointly constrained choices only after individual validity.
- **WE MUST ALREADY KNOW:** each candidate is viable/Risk-eligible with size curves; shared balances/depth/inventory/Risk are modeled.
- **COMPONENTS / ACTIVATE:** simple greedy/one-op Champion and QF-078 optimizer Challenger.
- **RECORD / MEASURE / LEARN:** requested/allocated/reserved q, conflicts, unused resources, deterministic solution, latency and EconomicLift. Learn whether complexity adds robust value.
- **CAPITAL / M0–M5:** none during Replay/Shadow; validated bounded only after separate M4 promotion.
- **DATA / FORMULAS / MODELS:** QF-073–078; simple baseline and optional optimizer.
- **FAILURE / EXIT / NEXT:** double allocation, Risk bypass, instability/runtime excess or no lift rejects Challenger. Exit with scoped allocation evidence. Next receives joint capital context.
- **LIMITATION:** portfolio optimization is not needed for initial one-route TT.

## 23. Stage 17 — Bridge / Capital Relocation

- **OBJECTIVE / WHY:** determine whether an intentional move to another capital state beats STAY after all costs and risks.
- **WE MUST ALREADY KNOW:** Atlas opportunity history, terminal viability, exits, sizing, Risk, portfolio/resource state and future utilization labels.
- **COMPONENTS / ACTIVATE:** Bridge research then Shadow and separate bounded probes with hysteresis/cooldown.
- **RECORD / MEASURE / LEARN:** every permitted path plus STAY, BridgeCost, ExpectedExitCost, relocation risk, EV_destination/EV_stay, break-even cycles and realized utilization/exit. Learn persistent relocation value.
- **CAPITAL / M0–M5:** separate probe then validated bounded; M2→M4/M5.
- **DATA / FORMULAS / MODELS:** QF-068–072, 073–078, 105–108; point-in-time future-opportunity model.
- **FAILURE / EXIT / NEXT:** transient edge, missing history/exit/support, flip-flop, unsafe terminal or STAY superiority rejects. Exit with separate Bridge capability evidence.
- **LIMITATION:** Bridge is not OWA/arbitrage and never inherits strategy alpha validation.

## 24. Stage 18 — Horizontal Scale

- **OBJECTIVE / WHY:** capture more independent validated opportunities before forcing size through finite depth.
- **WE MUST ALREADY KNOW:** each added market/route/instance repeats required support and shared/correlation constraints are known.
- **COMPONENTS / ACTIVATE:** more validated routes, markets, regimes or strategy instances.
- **RECORD / MEASURE / LEARN:** incremental capture, shared-resource collisions, correlation, aggregate tails, operations load and economic lift. Learn diversification versus complexity cost.
- **CAPITAL / M0–M5:** scaled validated only; each capability remains scoped M5/reversible.
- **DATA / FORMULAS / MODELS:** current QF/Risk/portfolio/capacity evidence for each scope.
- **FAILURE / EXIT / NEXT:** hidden shared depth/capital/risk, lost support or operations degradation stops/demotes. Exit only when added scope is independently validated.
- **LIMITATION:** horizontal-first is a guiding heuristic, not a mathematical theorem; evidence may favor another choice.

## 25. Stage 19 — Vertical Scale

- **OBJECTIVE / WHY:** increase q on an existing capability only when the next size region is empirically supported.
- **WE MUST ALREADY KNOW:** size-dependent fill, slippage, impact, completion, tails, Recovery, confidence, inventory and operations at/near next band.
- **COMPONENTS / ACTIVATE:** one reversible q-band expansion at a time.
- **RECORD / MEASURE / LEARN:** next-band predicted↔actual distributions, capacity drift, tail/recovery and capital efficiency. Learn the new `Q_validated` boundary.
- **CAPITAL / M0–M5:** scaled validated; q never exceeds current QF-076 result.
- **DATA / FORMULAS / MODELS:** QF-026–027, 040–043, 056–080, 095–110 as applicable.
- **FAILURE / EXIT / NEXT:** slippage/tail/recovery/OOD/infra/inventory degradation shrinks or revokes the band. Exit with explicit larger scope; poor evidence produces hold/downscale.
- **LIMITATION:** `€50 worked → €5,000 works` and automatic compounding are invalid.

## 26. Stage 20 — Infrastructure Scale

- **OBJECTIVE / WHY:** buy/deploy speed or resilience only when attributable economics justify the complexity/cost.
- **WE MUST ALREADY KNOW:** opportunity survival/capture and same-event benchmark can attribute recoverable loss.
- **COMPONENTS / ACTIVATE:** candidate host/network/runtime/feed/node/standby profiles in Shadow first; no direct trading grant.
- **RECORD / MEASURE / LEARN:** B01–B12 metrics, clock uncertainty, first arrival/decision readiness, CaptureRatio, InfraLostPnL, NetUpgradeValue, InfraROI, stability and downgrade comparison.
- **CAPITAL / M0–M5:** existing exact capability only after host revalidation; infra change cannot raise q by itself.
- **DATA / FORMULAS / MODELS:** QF-084–094 plus capture/survival evidence.
- **FAILURE / EXIT / NEXT:** faster ping without robust recoverable economics, instability, unsafe clock/runtime or negative LCB gate rejects. Exit with validated profile or documented rejection.
- **LIMITATION:** private node, second server, hot standby, bare metal or similar systems may never be economically required.

## 27. Continuous calibration

Recorder, Replay, Shadow and Micro-live do not end. Production continuously joins predictions to actuals, preserves trade/incident windows, monitors support/error/tails/economics and feeds offline recalibration. Production collects; research recalibrates; Validation decides. There is no uncontrolled self-modifying production model.

## 28. Capability demotion / rollback

Promotion is not monotonic. Drift, OOD, state inconsistency, security/infra failure, rising Recovery, unsupported tails or incident can shrink q, fall back a model, disable a market/mode, revert a release or demote M5. Alert clearance never auto-promotes. Resume requires reconciliation, fix/rollback evidence and explicit scoped re-promotion.

## 29. Data / evidence evolution

```text
Broad RAW
→ Replay datasets
→ Opportunity/reject episodes
→ Shadow forecasts/plans
→ Micro-live executions
→ Live execution/calibration evidence
→ Incident and revalidation evidence
```

Canonical artifacts include `RawChunkManifest`, `DatasetId`, `RunManifest`, `DecisionTrace`, `ReplayReport`, `ShadowRun`, `MicroLiveRun`, `ModelReport`, `InfraBenchmark`, `ValidationReport`, `CapabilityManifest` and `IncidentId`.

## 30. M0–M5 mapping

Typical progression is SPECIFY→M0, Unit/Golden→M1, Replay→M2, Shadow→M3, Micro-live→M4 and sustained scoped Live→M5. Different components occupy different levels simultaneously. M5 is bounded and reversible, never one global project number.

## 31. CapabilityManifest

Implementation flows into evidence, not capital. Only an explicit CapabilityManifest/ValidatedCapability scope identifies strategy, market, size range, execution mode, models, validation level, restrictions and versions that may be considered. Runtime permission further intersects configuration, license/channel, readiness and Risk.

## 32. Capital permission matrix

The stage-by-stage authority is [CAPITAL_PERMISSION_MATRIX.md](_analysis/pass12_build_validate_scale/CAPITAL_PERMISSION_MATRIX.md). Stages 0–9 carry no normal strategy capital. Stage 10 allows only an explicitly approved probe. Later capital remains bounded by the narrow current validated scope and can be withdrawn.

### Scaling evidence matrix

PASS 12 reuses and cross-links PASS 10's [SCALING_EVIDENCE_MATRIX](_analysis/pass10_validation_operations/SCALING_EVIDENCE_MATRIX.md) rather than duplicating its mathematical gates. Sequencing is explicit: `HORIZONTAL SCALE` widens independent validated opportunities; `VERTICAL SCALE` widens q only through `Q_validated`; `STRATEGY SCALE`, `MARKET SCALE` and `MAKER SCALE` repeat the changed capability's evidence; `CAPITAL RELOCATION` requires separate Bridge/STAY proof; `INFRA SCALE` requires attributable robust economics. Every mode supports hold, shrink and demotion.

## 33. Stop conditions

The authoritative PASS 12 map is [STOP_CONDITION_MATRIX.md](_analysis/pass12_build_validate_scale/STOP_CONDITION_MATRIX.md). A failure is global, market-, strategy-, mode-, model-, size- or infra-scoped. Independent safe research may continue, but no affected promotion bypasses the stop.

## 34. Learning dependency graph

[LEARNING_DEPENDENCY_GRAPH.md](_analysis/pass12_build_validate_scale/LEARNING_DEPENDENCY_GRAPH.md) makes causal order explicit: data before labels, labels before serious models, predictions before actuals, actuals before calibration, and calibrated support before `Q_validated`, Bridge or InfraROI.

## 35. Technical-phase mapping

[TECHNICAL_PHASE_TO_EVIDENCE_STAGE_MAP.md](_analysis/pass12_build_validate_scale/TECHNICAL_PHASE_TO_EVIDENCE_STAGE_MAP.md) maps all 26 technical phases to primary and continuing evidence stages. Recorder, Replay, Shadow and Micro-live remain recurring tools.

## 36. What remains FUTURE

Cross-exchange trading/transfers, private node dependency, distributed hot standby/fencing, dense response graphs, explicit competitor-agent F4 worlds, complex portfolio optimizers without lift, and TM/MM activation are not prerequisites for initial validated TT. They require their own specs, evidence and approval.

## 37. Final path to sustained M5

The path is: specify final contracts; record source truth; reconstruct state; map; identify; deterministic Replay; explicit-fidelity simulation; Shadow; predeclare forecasts; bounded Micro-live; calibrate; promote narrow TT; validate TTT separately; learn maker behavior; validate MT/MTT; learn capital productivity; validate Portfolio/Bridge; scale horizontally; increase q only with `Q_validated`; upgrade infra only with robust economics; continuously monitor, demote and revalidate.

## 38. Cross-links

- [Technical Implementation Roadmap](17_IMPLEMENTATION_ROADMAP.md)
- [Roadmap deep specs](deep-specs/roadmaps/README.md)
- [Evidence Stage Matrix](_analysis/pass12_build_validate_scale/EVIDENCE_STAGE_MATRIX.md)
- [Exit Criteria](_analysis/pass12_build_validate_scale/EVIDENCE_STAGE_EXIT_CRITERIA.md)
- [Experiment and Data Map](_analysis/pass12_build_validate_scale/EXPERIMENT_AND_DATA_REQUIREMENT_MAP.md)
- [Validation Matrix](16_VALIDATION_MATRIX.md)
- [Operations and Monitoring](18_OPERATIONS_AND_MONITORING.md)
- [PASS 12 report](_analysis/pass12_build_validate_scale/PASS12_FINAL_REPORT.md)

## 39. CORR-01 — Evidence journey integration

CORR-01 adds no evidence stage. Stage 0 freezes funnel/metric/label/timing definitions; Stage 1 records bounded evidence; Stage 2 proves deterministic reconstruction and episode derivation; Stages 4–6 identify opportunities and forecasts without conflating them with attempts; Stage 7 reports only `would_*`; Stage 8 freezes join/calibration policy; Stage 10 obtains actual fills/reconciliation/economics under existing authority; Stages 11–20 use comparable funnel and economic evidence for capability/scale decisions.

The recurring doctrine is `measure -> attribute -> change -> remeasure -> capture-stage effect -> actual economic effect`. A technically faster system that cannot prove a comparable funnel/economic improvement remains unvalidated for scale.

## 40. CORR-02 — Optimization evidence loop

Every performance change follows:

`BASELINE → PROFILE → IDENTIFY HOTSPOT → FORM HYPOTHESIS → MAKE SEMANTICALLY SAFE CHANGE → PARITY → MICROBENCH → REPLAY → SHADOW → CAPTURE COMPARISON → ECONOMIC VALIDATION IF MATERIAL`.

Stages 1–4 establish realistic event, book, graph, BBO and NetConvert workloads; Stage 5 supplies deterministic parity; later stages establish behavior under forecasts, Shadow and bounded capital only through their existing gates. A transparent optimization must retain the same DecisionTrace. A scheduling/coalescing change is explicitly semantic, versioned and human-reviewed. A local latency win without stable end-to-end, capture and robust economic evidence cannot justify promotion or infrastructure/language escalation. See the [Profiling and Bottleneck Protocol](_analysis/corr02_hot_path_performance/PROFILING_AND_BOTTLENECK_PROTOCOL.md).

## 41. CORR-03 — Observe, resolve, calibrate, then consider influence

The completion sequence is `observe real attempts → reconcile → derive path and terminal labels → build constant/simple empirical baseline → chronological OOS → Shadow observe-only → Micro-live actual calibration → compare Challengers → explicitly promote only if useful → recalibrate or demote on drift`. TT, TTT and maker modes do not inherit one another’s evidence; q/infra/policy distribution changes trigger support review.

The model remains data/offline baseline until the [Promotion Gate](_analysis/corr03_execution_completion/COMPLETION_MODEL_PROMOTION_GATE.md) is passed. CORR-03 adds no hard Risk gate, formula integration, sizing authority or online learning. Harjus is comparative evidence only. CORR-04 may later compare infrastructure against actual completion evidence; CORR-05 owns economic composition and double-count review.

## 42. CORR-04 — Public baseline to evidence-gated infrastructure scale

`PUBLIC BASELINE -> MEASURE -> NODE/FEED CHALLENGER OBSERVE-ONLY -> STRICTLY ALIGN/COMPARE -> PROVE CORRECTNESS AND CAPTURE -> PROVE ROBUST NET VALUE -> EXPLICITLY PROMOTE -> ONLY THEN CONSIDER DEEPER OS/NETWORK COMPLEXITY`.

Speculative data remains a separate Research lane through parity/Replay/Shadow and cannot affect real send without a future explicit design. Docker stays baseline; native, affinity, scheduler/IRQ/network tuning and AF_XDP/DPDK/F-Stack do not inherit maturity and cannot block early V1. QF-084–QF-093 stay authoritative; CORR-05 section 43 now reconciles survival, actual completion, infrastructure capture and any future priority cost without double counting.

## 43. CORR-05 — Calibrate economics before scaling

The evidence loop is `freeze candidate and distribution semantics -> validate scenario probabilities/cashflows -> validate q/state support -> validate tails and external penalties -> enforce Risk gates -> reconcile predicted versus actual economics -> promote a versioned model -> scale only inside Q_validated`. Shadow produces counterfactual evidence; only reconciled Micro-live/Live events produce realized PnL.

Model demotion selects only a supported declared fallback and may contract capacity. Profile or capital scaling cannot outrun completion, fidelity, OOD or accounting evidence. Bridge and infrastructure decisions use their separate economic/accounting boundaries. See [CORR-05 Roadmap Impact](_analysis/corr05_economic_integration/CORR05_ROADMAP_IMPACT.md).
