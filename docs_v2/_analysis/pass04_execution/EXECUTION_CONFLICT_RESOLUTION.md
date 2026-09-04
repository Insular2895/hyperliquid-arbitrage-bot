# PASS 04 — Execution Conflict Resolution

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## Active-search results

| Prompt | Conflict found? | Historical tension | Canonical resolution | Register |
|---|---:|---|---|---|
| A market vs protected taker | yes | generic/market language could imply unbounded crossing | protected IOC/marketable limit with approved worst price; exact support external | existing CONFLICT-006 |
| B partial exceptional vs normal | yes | happy-path descriptions omit intermediate exposure | zero/full/partial are mandatory normal branches | CONFLICT-024 |
| C planned vs actual quantity | yes | precomputed route quantity could flow downstream | every later leg uses actual fills/fees/rounding | CONFLICT-025 |
| D retry on timeout vs no blind retry | yes | transport retry shorthand risks duplicate intent | stable CLOID, query/reconcile, never blind resend | CONFLICT-026 |
| E timeout failure vs unknown | yes | generic failure handling could imply no fill | possible transmission -> `UNKNOWN`/reconcile | CONFLICT-027 |
| F cancel sent vs canceled | yes | imperative cancel shorthand implies finality | cancel race is normal; finality requires exchange proof | CONFLICT-028 |
| G giant enum vs five machines | no genuine conflicting requirement found | older prose was compressed, not an explicit one-enum mandate | five coordinated machines are closure | no new conflict |
| H local authority vs exchange truth | yes | checkpoint/journal could be mistaken for truth | orders/fills/balances and reconciliation outrank local assumption | CONFLICT-029 |
| I finish route vs best Recovery exit | yes | early route narratives favour intended continuation | QF-079 best current portfolio action; sunk costs ignored | CONFLICT-030 |
| J single vs split Recovery | yes | single-exit examples are incomplete | split exits supported under shared reservations/Risk | CONFLICT-031 |
| K auto READY vs reconcile first | yes | naive process restart may admit risk | `BOOTING->SYNCING->RECONCILING`; only `CONSISTENT` permits READY | CONFLICT-032 |
| L early TM/MM vs supported-disabled | yes | generic mode matrix could imply enablement | representable, disabled, unvalidated pending explicit decision | CONFLICT-033 |
| M synchronous journal vs nonblocking | yes | durability wording could place disk writes in reducer | append-only async durable queue + exchange reconstruction | CONFLICT-034 |
| N planned maker fill vs actual partial | yes | maker plan may wait for full completion | each actual partial is immediate exposure/hedge/recovery input | CONFLICT-035 |

## Result

- Genuine conflicts/evolutions found: **13** (including existing CONFLICT-006).
- Resolved by closure/later authority: **13**.
- Remaining blocking contradictions: **0**.
- No conflict was invented for item G.

These resolutions do not decide numeric gates, provider choices, exact Data schemas, or Live activation.
