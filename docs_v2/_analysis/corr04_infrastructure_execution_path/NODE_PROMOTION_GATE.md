# Node Promotion Gate

`STATUS: SPECIFIED — NOT PASSED`

These labels map into existing M0–M5; they are not a new maturity ladder.

| Gate | Required proof |
|---|---|
| `N1` | current node/feed semantics, software, flags and limitations externally revalidated |
| `N2` | correct state reconstruction, ordering, gap and resync behavior |
| `N3` | valid event alignment and arrival/state-age evidence |
| `N4` | deterministic Replay and source/epistemic provenance |
| `N5` | paired Shadow comparison over supported regimes |
| `N6` | acceptable resource, Recorder and engine interference |
| `N7` | plausible/measured capture effect, not latency alone |
| `N8` | robust positive incremental value after node/host/storage/network/ops cost and uncertainty under QF-086–QF-091 |
| `N9` | deployment, security, readiness, single-owner and rollback validation |

Only after N1–N9 may a bounded node feed become a canonical Micro-live candidate. Account size, advertised latency or richer data cannot substitute. Demote on lag, gaps, parity failure, contention, instability, security issue, invalid evidence or vanished economic value. Fallback to public feed requires an explicit feed-profile transition, rebuild and reconciliation.
