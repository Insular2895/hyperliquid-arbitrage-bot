# CORR-03 — External Harjus Failure Research

DOCUMENTATION STATUS: COMPARATIVE EXTERNAL EVIDENCE — NOT SOURCE AUTHORITY

Research cutoff: 2026-09-08. Repository HEAD observed: `09816b3da2a393795250e38c8b49869b57ba4d6f` (commit date 2026-03-04). Release tag `releases/4.0.0`: `106f855de9af40c5333f605525d25b4622b852b9` (commit date 2026-02-17).

## Primary sources

| Source | Date/version | Exact observed claim/data | Direct vs inference | Binance-specific? | General execution lesson | Confidence |
|---|---|---|---|---|---|---|
| [Harjus repository](https://github.com/ValtteriL/harjus) | HEAD above, observed 2026-09-08; release tag above | README identifies a Binance Spot triangular-arbitrage bot; code uses Fill-Or-Kill and balance updates from execution reports | mechanics directly visible; no Hyperliquid inference allowed | yes | actual order reports, not planned trades, determine balances | high |
| [Releases 1–3 write-up](https://shufflingbytes.com/posts/binance-triangular-arbitrage/) | published 2025-07-21 | 69 hours: 156 opportunities, one completed execution; orders expired without fill and unwanted assets needed manual disposal at loss | counts/inventory direct; exact causal latency and order-level partials not proved | experiment yes | attempts/full completion need distinct denominators; incomplete routes can strand inventory | high |
| [Release 4.0.0 write-up](https://shufflingbytes.com/posts/harjus-release-4.0.0/) | published 2026-03-03; tag/commit above | 74 hours: 84 opportunities, zero completed routes, 18 executions with some trades filled, 24 trades filled; all attempts failed due to expiry; holdings materially reallocated | route-level partial execution direct; exact affected leg/order-level partial fill not identified | experiment yes | retain zero/later-leg/incomplete-path evidence and actual holdings | high |
| [v4 production raw log](https://gist.github.com/ValtteriL/b438a17c3c0eb61d4000ce93e9f1e39c) | published 2026-03-02; events 2026-02-27 to 2026-03-01 | `EXPIRED` with `usedQty=0`, other reports `FILLED`, sequences ending `Failed execution`, internal `UNKNOWN` preceding FILLED/EXPIRED | event lines direct; `UNKNOWN` is not proved lost-submit ambiguity; cause not proved | yes | preserve ordered event path and avoid interpreting intermediate status as final truth | high for events; low for cause |

## Directly evidenced scenario classes

- `HJ-001`: known zero-fill expiry is directly observed (`EXPIRED`, `usedQty=0`).
- `HJ-003`: incomplete triangles after one or more filled trades and a later expired order are directly stated and visible in production evidence.

`HJ-002`, `HJ-004`–`HJ-010` are project failure scenarios inspired by general real-world failure patterns. Repository enums/tests show that partial/cancel states are technically represented, but that is not a production incident. The author’s manual unwinding of unwanted inventory supports the need for recovery evidence, not this project’s exact `RecoveryState` behavior.

## General lesson retained

Detected opportunities, real attempts and fully completed routes can differ by orders of magnitude. An incomplete multi-leg path can leave economically material inventory. Negative and incomplete outcomes therefore belong in the evidence population. No Binance FIX/FOK, AWS, C++, F-Stack, latency or asset-selection choice is imported as project authority.
