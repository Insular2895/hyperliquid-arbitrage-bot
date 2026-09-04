# 11 — Execution transport and Replay/Shadow/Live parity

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## Interface and effect boundary

SRC-005 defines conceptual `ExecutionTransport.submit`, `.cancel`, and `.query`. Its listed implementations are `HyperliquidHttpTransport`, `HyperliquidWsTransport`, `ReplayTransport`, `PaperTransport`, and `NullShadowTransport`. `TransportRequest` contains only `signed_intent`, `transport_type`, `request_id`, optional `send_at`.

The core emits effect requests and consumes typed events. It never branches to easier fill, Risk, reservation, or recovery logic based on mode. Transport success/failure is not automatically economic state.

## Mode matrix

| Exact `RunMode` | Effect target | Events returned | Actual account mutation | Evidence role |
|---|---|---|---:|---|
| `Replay` | `ReplayTransport` -> exchange emulator | same Order/Fill schemas | no | deterministic historical/counterfactual tests |
| `Paper` | paper transport/emulator policy | same schemas with declared provenance | no | integration/mechanics evidence with limits |
| `Shadow` | `NullShadowTransport` | `WouldSubmitEvent`; simulated facts remain shadow | no | live-decision comparison without orders |
| `MicroLive` | real promoted transport | real exchange events | yes, calibrated tiny authority | intervention/calibration/fault evidence |
| `Live` | real promoted transport | real exchange events | yes | production authority within limits |

“Paper” is not a synonym for Shadow or Replay. Shadow counterfactual inventory never overwrites `ActualAccountState`.

## Same-machine rule

Replay feeds `OrderIntent` into `HyperliquidExchangeEmulator`, which emits `OrderEvents`/`FillEvents` in the same schema as Live. Identical reducers then apply reservations, order states, partials, recovery, reconciliation, inventory, and accounting. Replay cannot assume full recovery, ignore double-spend, or fill at theoretical time/price.

`DecisionTrace = F(OrderedEvents, ResolvedConfig, ModelArtifacts, FormulaVersion, Seed)`. Replay uses `ReplayClock`, recorded `TimerEvent`s, stable event order, explicit seed, and versioned state. Stochastic simulator outcomes are reproducible when seed/input manifest is identical.

## Simulated responses and truth labels

Emulator Order/Fill events carry source/mode provenance and are truth only inside their run. Real account events always outrank simulated state for actual exposure. Shadow produces “would submit,” not “did submit” or fill evidence. Micro-live actual fills take precedence over model predictions and feed calibration.

## Direct, batched, HTTP, WebSocket

These are transport implementation candidates. The coordinator stays compatible with direct low-latency and batching and may separate maker/taker batches where externally valid, but does not hardcode a cadence. Benchmark P50/P99/stability and current API facts decide deployment; no transport choice may alter intent economics or state semantics.

## Required parity tests

Given the same ordered event fixture, assert identical intents, state transitions, Risk-decision references, fill application, recovery selection, reservation/accounting outputs, and trace hash across supported non-effecting runs. Inject lost/duplicate/out-of-order transport events, clock/timer replay, crash/restart, and stale worker versions. Any hidden wall-clock, random source, or mode-specific shortcut fails parity.
