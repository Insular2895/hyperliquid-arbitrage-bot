# 09 — Runtime Inference and Cross-Domain Contracts

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Runtime principle

Live Participant inference is an incremental feature update plus small bounded model evaluation. Heavy model fitting, parameter sweeps, large Monte Carlo, Hawkes simulation, deep networks and explicit agent worlds remain outside the hot path.

Precomputed feature dependencies, sparse response neighbourhoods, empirical tables, quantiles and size candidates can reduce work. Any optimization still needs numerical parity, determinism where required, latency distributions and ModelValue evidence.

## Logical inference envelope

Every forecast must be attributable to:

```text
forecast_id
model_id / model_version
feature_schema_version
formula_version set
event_time / as_of_time / generated_time
input sequence or snapshot lineage
market / route / size / side
feed fidelity and active P-level
supported horizons
confidence / OOD / validity / reason
```

Exact names, types, units and serialization belong to the Data Contracts pass. PASS 02 defines the semantic minimum only.

## Inputs

- valid point-in-time books/trades and feature snapshots;
- route/opportunity state with authoritative net edge and size;
- measured latency distribution or identified infrastructure profile;
- optional intervention features for response forecasts;
- model registry selection and support metadata;
- clock/feed/data-quality state.

Inference may not fetch remote data, perform mass address lookups or scan unbounded history in the decision path.

## EdgeSurvivalForecast

Source contract semantics include survival at horizons, `p_survive_arrival`, edge half-life, expected arrival edge, edge quantiles and confidence. The canonical schema remains in the Data Contracts pass. PASS 02 additionally requires supported horizon, threshold provenance and OOD/validity so consumers cannot misread a partial forecast.

## LiquidityForecast

Source contract semantics include expected arrival depth, depth quantiles, probability of depth loss, expected replenishment, spread forecast and confidence. It represents a distribution, not guaranteed capacity. Mechanical impact is not duplicated inside participant response.

## CrossMarketForecast

Source contract semantics include source market, affected responses and confidence. Targets are sparse, horizon-specific and versioned. Missing/unsupported neighbours are not interpreted as certain zero response.

## Maker forecast

SRC-007 conceptually defines fill probabilities at horizons, expected fill time, partial-fill probability, adverse selection, cleanup cost and confidence. The authoritative Data schema is not yet closed by PASS 02. Until PASS 06, treat `MakerForecast` as a semantic interface proposal, not a redefined Data Contract.

## Freshness and compatibility

A forecast is invalid if any of these holds:

- source book/feature state is stale or sequence-invalid;
- clock quality cannot support its horizon;
- model and feature schema mismatch;
- requested market, route, size, regime, fidelity or horizon is unsupported;
- artifact integrity fails or output is non-finite/incoherent;
- model age/drift policy invalidates use.

Consumers use the reasoned invalid/degraded state. They do not substitute neutral probabilities or reuse a stale forecast silently.

## Risk consumer

Risk consumes direct survival/threshold probabilities, arrival-edge and liquidity tails, maker adverse-selection/partial risk, cross-market consistency, OOD, disagreement and confidence. Participant forecasts can only tighten, reduce or reject risk. `MODEL_KILL` disables dependent strategies; it need not stop unrelated safe functions.

## Execution consumer

Execution consumes arrival-edge, fill-time, cancellation/toxicity, second-leg and cross-market forecasts when its state machine reaches the applicable decision. It rechecks time-of-check/time-of-use freshness and reassesses immediately after any maker fill. Exact state transitions remain Execution-owned.

## Simulator consumer

Simulator draws or applies participant-response distributions after the deterministic exchange/mechanical layer. It owns Monte Carlo branches, queue counterfactuals, historical reconciliation, partial-fill/recovery and PnL distributions. `EXOGENOUS_REPLAY` and `INTERACTIVE_COUNTERFACTUAL` remain distinguishable.

## Sizing and slicing consumers

Sizing combines current/future depth, survival, impact, recovery and Risk constraints. OOD sizes are reduced or rejected. Slicing weighs replenishment against decay/competition/inventory; it never waits on replenishment alone. Optimization remains owned by later Sizing/Simulator passes.

## Infrastructure consumer

Infrastructure provides latency distributions by measured profile. Participant survival integrates them with QF-048/QF-085. Infrastructure upgrades are judged by net robust economic improvement, not milliseconds alone. PASS 01 remains unchanged and authoritative for measurement.

## Market Atlas and Recorder consumers

Recorder/Data persists immutable episodes, forecasts/outcomes, feature/model lineage and censored observations. Market Atlas may aggregate survival, half-life, correction velocity, replenishment, toxicity, competition and response strength by time window and version. Atlas output helps HOT/WARM/COLD selection but creates no execution permission.

## Failure/degraded behaviour

```text
valid supported forecast -> normal consumer evaluation
low confidence / disagreement -> uncertainty penalty, reduced size or reject
OOD / stale / mismatch -> invalid; safe fallback if supported
model unavailable/corrupt -> conservative empirical fallback or strategy disable
feed fidelity degraded -> lower P-level and recalibrate/disable unsupported features
```

All transitions emit stable reason codes and provenance through Data/Execution/Risk-owned contracts. No network request or heavy recovery calculation is introduced into the participant hot path.

## Runtime validation

- Python/Rust golden parity for features and model outputs;
- latency P50/P95/P99/P99.9 under realistic load;
- bounded memory/CPU and no history scan;
- stale/schema/artifact/NaN/fidelity fault injection;
- deterministic lookup/inference where the architecture requires it;
- forecast-to-consumer end-to-end freshness and TOCTOU tests;
- ModelValue after added latency and recorder interference.

## Sources

SRC-002 architecture; SRC-004 formula order/registry; SRC-005 Data/Risk contracts; SRC-006 validation; SRC-007 runtime and forecast interfaces; SRC-008 Simulator boundaries; PASS 01 Infrastructure master/deep specs.
