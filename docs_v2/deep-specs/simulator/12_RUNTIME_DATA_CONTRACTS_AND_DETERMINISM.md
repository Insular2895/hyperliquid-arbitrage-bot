# 12 — Runtime Data Contracts and Determinism

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

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
