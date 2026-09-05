# Replay Engine Modes, Clock and Ordering

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Replay replaces the source and ExecutionTransport; it does not replace Core. Market/account events, reducers, formulas, Strategy, Simulator, Risk, Execution, Recovery, Inventory and Reservations remain shared.

| Replay mode | Schedule | Permitted counterfactual |
|---|---|---|
| `EXACT RECEIVE-TIME` | Local recorded receive order/interval | None beyond declared Replay transport model |
| `ACCELERATED` | Same order/relative intervals at faster host speed | None |
| `COUNTERFACTUAL LATENCY` | Same historical market evidence; versioned own-path delay | Arrival/fill/inventory consequences |
| `INTERACTIVE` | Deterministic versioned branch schedule | Mechanical/participant market response |

EventTime (`exchange_ts`) is source chronology; ReceiveTime is bot knowledge. Late events are applied when received. At ReplayClock T, events with receive time greater than T are inaccessible. Timers are recorded/derived deterministically through Clock semantics, not host scheduler behavior.

The local order key is `(recv_monotonic_ns, source_priority, recorder_seq)` and recorder sequence is the definitive final tie-break. Equal timestamp batches use the same key. Priority queues for persistence cannot reorder Core economic evidence.

RunMode remains `Replay|Paper|Shadow|MicroLive|Live`. Replay mode, RunMode and Simulator fidelity/SimulationMode are independent fields and must all be reported where relevant.
