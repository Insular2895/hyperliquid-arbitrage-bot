# Clock and Time Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Concept | Authority/meaning | Required use | Failure/uncertainty behavior |
|---|---|---|---|
| `exchange_ts?` | Optional source-asserted time | Market chronology research | Never invent; never use as receive fallback |
| `recv_wallclock_ts` | Local wall clock | History and cross-machine correlation | Attach clock quality/uncertainty |
| `recv_monotonic_ns` | Local monotonic instant | Local order, latency differences, timers | Reset/domain boundary must be identified |
| `ClockQualityRecord` | offset, uncertainty, source count, timestamp | Qualify wall-clock comparison | Invalid/unknown comparison cannot support precise claim |
| `LiveClock` | Runtime clock implementation | Live/Paper/Shadow/MicroLive Core time | Health feeds Infra/Risk |
| `ReplayClock` | Dataset-driven clock | Exact/accelerated/counterfactual replay | Must preserve declared domain intervals/order |
| `TestClock` | Controlled fixture clock | Unit/property/fault tests | Explicit manual schedule |
| `RngProvider` | Sole random source abstraction | Any stochastic operation | Seed/output provenance required |
| `replay_time` | Current ReplayClock knowledge cutoff | Gate event visibility and domain timers | Future receive events inaccessible |
| logical timer time | Explicit TimerEvent schedule from Clock | Risk rechecks, expiries, reconciliation, metrics | Host scheduler timing cannot alter decisions |

Cross-machine timing is valid only under a versioned rule such as observed separation exceeding combined uncertainty. `SystemTime::now()` and implicit RNG are forbidden inside Core reducers/decision logic.

Exact Hyperliquid timestamp provenance, units, ordering guarantees, source sequence/block semantics and reconnect behavior require external revalidation before implementation.

PASS 01 cross-link: [Infrastructure clock and measurement contract](../../deep-specs/infrastructure/04_CLOCK_AND_MEASUREMENT_CONTRACT.md). PASS 06 owns domain/replay time meaning; PASS 01 owns synchronization measurement and benchmark validity.
