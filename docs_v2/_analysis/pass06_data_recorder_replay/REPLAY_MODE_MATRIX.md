# Replay Mode Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Replay mode | Market evidence | Clock/order | Own execution path | Market response | Primary claim |
|---|---|---|---|---|---|
| `EXACT RECEIVE-TIME` | Historical recorded | Actual receive order/relative timing | Versioned historical/sim transport | Baseline unchanged | Reproduce what bot knew/did |
| `ACCELERATED` | Same historical | Same order/relative intervals, faster host runtime | Same semantics | Baseline unchanged | Faster equivalent replay |
| `COUNTERFACTUAL LATENCY` | Historical market events | Versioned changed own-path timing | Arrival/fill/inventory may differ | Baseline market unchanged | Infra/execution timing sensitivity |
| `INTERACTIVE` | Historical baseline | Versioned branch order/clock | Simulated effects | Mechanical/participant response may change | Counterfactual branch research |

Separate axes:

- `RunMode`: `Replay`, `Paper`, `Shadow`, `MicroLive`, `Live`.
- `ReplayFidelity`: `F0Historical`, `F1LatencyMechanical`, `F2Queue`, `F3Responsive`, `F4Interactive`.
- `SimulationMode`: `ExogenousReplay`, `InteractiveCounterfactual`.

RunMode cannot change strategy/formula/risk/state-machine logic. Exact receive-time follows ReceiveTime, not exchange EventTime. Every mode enforces No Lookahead and records its timing/simulator assumptions in the run/branch manifest.

## Full mode contract

| Mode | Purpose | Market source | Execution transport | Clock | Ordering | RNG | Counterfactual response? | Deterministic? | Limitation | RunManifest label | Source authority |
|---|---|---|---|---|---|---|---|---|---|---|---|
| EXACT RECEIVE-TIME | Reproduce actual bot knowledge | Recorded historical | ReplayTransport/emulator version | ReplayClock at recorded intervals | Receive/order key | Seeded | No baseline response change | Yes for same manifest | Cannot know alternate market reaction | exact mode + dataset/fidelity | SRC-005 §101–109 |
| ACCELERATED | Equivalent replay faster | Same recorded | Same as exact | Accelerated ReplayClock | Identical to exact | Same seed | No | Yes; equal to exact semantics | Host speed cannot change domain time | accelerated factor/policy | SRC-005 §103/289 |
| COUNTERFACTUAL LATENCY | Test own timing/infra | Historical market unchanged | Versioned delayed transport | Counterfactual ReplayClock policy | Historical receive order + own effects | Seeded if simulation | Own fill/inventory only | Yes per manifest | Exogenous market future remains fixed | latency policy/version | SRC-005 §103/170–174 |
| INTERACTIVE | Research plausible changed response | Historical baseline + branch | Interactive simulator transport | Branch ReplayClock | Versioned deterministic branch order | Seed/path ID | Yes, calibrated mechanical/participant | Yes per seed/path | Not exact alternate-world truth | BranchId/model/fidelity | SRC-005 §103/168–175; SRC-008 |
