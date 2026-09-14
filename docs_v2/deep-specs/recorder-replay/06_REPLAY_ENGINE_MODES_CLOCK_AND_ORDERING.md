# Replay Engine Modes, Clock and Ordering

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

Replay replaces the source and ExecutionTransport; it does not replace Core. Market/account events, reducers, formulas, Strategy, Simulator, Risk, Execution, Recovery, Inventory and Reservations remain shared.

| Replay mode | Schedule | Permitted counterfactual |
|---|---|---|
| `EXACT RECEIVE-TIME` | Local recorded receive order/interval | None beyond declared Replay transport model |
| `ACCELERATED` | Same order/relative intervals at faster host speed | None |
| `COUNTERFACTUAL LATENCY` | Same historical market evidence; versioned own-path delay | Arrival/fill/inventory consequences |
| `INTERACTIVE` | Deterministic versioned branch schedule | Mechanical/participant market response |

EventTime (`exchange_ts`) is source chronology; ReceiveTime is bot knowledge. Late events are applied when received. At ReplayClock T, events with receive time greater than T are inaccessible. Timers are recorded/derived deterministically through Clock semantics, not host scheduler behavior.

The captured local order key is ascending `recorder_seq` in the fixed Recorder context. Receive monotonic time and source priority may resolve concurrency only before that sequence is assigned. Equal-time batches and persistence queues cannot reorder assigned Core evidence.

RunMode remains `Replay|Paper|Shadow|MicroLive|Live`. Replay mode, RunMode and Simulator fidelity/SimulationMode are independent fields and must all be reported where relevant.

Speculative/uncommitted input replays in a separate `NON-CANONICAL` source lane from committed events. Its local receive time permits research use from that time, but later commit/change/disappear labels are outcomes and cannot leak backward. A canonical DecisionTrace is unchanged when the speculative lane is disabled or discarded; reuse must match fresh canonical computation exactly.
