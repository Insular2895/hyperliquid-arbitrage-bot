# 12 — Runtime Data Contracts and Determinism

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW — PASS 03 REVIEW COMPLETE`

## Same core, different boundary

Replay, Paper, Shadow, Micro-live, and Live use the same reducers, strategy, formulas, Risk, Execution State Machine, Recovery, Inventory, and Reservation logic. Source/transport changes: recorded events + `ReplayTransport`; live events + `NullShadowTransport`; or live events + real transport. Explicit Risk config/capital may differ. `RunMode` may not silently enable easier fills, thresholds, or math.

## Determinism identity

```text
DecisionTrace = F(OrderedEvents, ResolvedConfig,
                  ModelArtifacts, FormulaVersion, Seed)
```

Same inputs reproduce the deterministic trace; same stochastic contract reproduces sampled paths. Event order is explicit, based on replay/receive time and versioned tie-break rules. `recv_ts` answers what the bot knew; no event with future receive time is visible. `ReplayClock` replaces hidden `SystemTime::now()`.

`TimerEvent` represents strategic time: Risk recheck, maker expiry, unknown-resolution timeout, reconciliation trigger, and other versioned timers. `RngProvider` uses the seed recorded in `RunManifest`; important live stochastic outcomes are recorded, while Live should prefer deterministic expected values/quantiles.

## Required semantic contracts

| Contract | Simulator use |
|---|---|
| `RunMode` | Environment/source/transport provenance. |
| `SimulationMode` | `ExogenousReplay` or `InteractiveCounterfactual`. |
| `ReplayFidelity` | `F0Historical`…`F4Interactive`. |
| `ExecutionForecast` | Consolidated completion/PnL/tail/confidence output. |
| `ConfidenceState` | Decomposed support/freshness/OOD/agreement/latency causes. |
| `BranchId`, `MonteCarloPathId`, `CounterfactualRejoinEvent` | Branch/path/rejoin trace. |
| Participant forecasts | Calibrated survival/liquidity/maker/cross-market inputs. |
| `LatencyTrace` | Observed/composed latency and calibration lineage. |
| `GoldenDataset` | Fixed deterministic expected trace and PnL. |
| `DecisionTrace` | Ordered decisions, intents, transitions, Risk decisions. |
| `RunManifest` | Run/build/config/data/models/formulas/schemas/seed. |
| `ModelArtifact` / `ModelVersion` | Point-in-time model and training/support provenance. |
| State hashes | Replay identity, checkpoints, and comparison. |

Exact fields/types/serialization remain PASS 06. Every number used to decide requires meaning, unit, timestamp, version, and source.

## Concurrency and stale results

Critical states have one logical writer and immutable versioned snapshots. Parallel simulation/inference may run on snapshots, but output carries `input_state_version` and validity/TTL. A result computed on stale state is discarded or revalidated; it cannot commit a decision against materially changed state. An ordered coordinator commits economic transitions.

## Tests and failure

Golden replay hash, 100-run determinism, multi-thread transition equality, clock/timer tests, seed repeatability, schema roundtrip, duplicate event/fill rejection, invalid region handling, point-in-time model/fee/config checks, and restart reconstruction are mandatory before authority. Any missing version/seed/fidelity/mode makes a result non-reproducible and therefore non-canonical evidence.

## CORR-01 forecast-label binding

Every `ExecutionForecast` used by a plan binds its horizon, route objective and `ForecastLabelVersion`. `p_full`, `p_partial`, `p_recovery` and `p_failure` are predictions and may be treated as one partition only when the label version defines mutually exclusive exhaustive actual classes. Plan-time output is immutable; later evaluation is a separately labeled counterfactual. See [Predicted vs Actual Capture Calibration](../../_analysis/corr01_capture_observability/PREDICTED_ACTUAL_CAPTURE_CALIBRATION.md).

## CORR-03 resolved route-outcome profile

`ROUTE_OUTCOME_RESOLVED_V1` partitions eventual real-attempt terminal outcomes into original-route completion without Recovery (`p_full`), non-completion with strategy fill and no Recovery (`p_partial`), non-completion with Recovery entry (`p_recovery`), and residual resolved zero-fill/no-Recovery non-completion (`p_failure`). UNKNOWN/unresolved at an analysis cutoff is missing terminal observation, not failure mass. Other label versions retain separate-binary semantics unless their partition is proven. See [ExecutionForecast Probability Audit](../../_analysis/corr03_execution_completion/EXECUTION_FORECAST_PROBABILITY_AUDIT.md).

## CORR-04 source/profile determinism

Replay/Shadow results link canonical/challenger role, `FeedProfileId`, `InfraProfileId`, node build/flags and event-alignment version. Speculative events replay separately and never enter committed ordered input unless a later canonical event independently does so. Exact reusable precompute output must equal fresh canonical recomputation; otherwise it is discarded.
