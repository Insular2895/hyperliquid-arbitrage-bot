# CORR-04 Validation Matrix

`STATUS: SPECIFIED — NOT EXECUTED`

| Family | Required tests | Expected invariant/evidence |
|---|---|---|
| public feed | ordering, book rebuild, gaps, reconnect, freshness, manifest | coherent source-labeled canonical state or fail closed |
| dual feed | one writer, challenger isolation, strict matching, clock uncertainty, gaps/source labels | no challenger canonical mutation; ambiguous pairs unmatched |
| node | lag, sync/catch-up, restart, disconnect, mismatch, resource contention, fallback | unsafe source cannot create new risk; transition reconciles |
| speculative | `S-01`–`S-10`, no-lookahead, ID/funnel isolation | canonical decisions/truth unchanged |
| reuse | speculative reuse versus fresh canonical calculation | exact semantic/numeric parity or discard |
| Docker/native | bridge/host/native with same semantics/security | correctness parity before latency result |
| CPU/scheduler | affinity/priority on/off, starvation and rollback | identical decisions; fills/account/reconciliation progress |
| IRQ/network | queue/steering/tuning on/off, loss/reconnect/tails | no reliability/correctness regression |
| kernel bypass | protocol-applicability and least-privilege review before prototype | complete TCP/TLS/WebSocket boundary proven |
| sequencing | current fact conformance; later controlled priority study only if supported | gossip/inclusion/price-time not conflated |
| failures | node/public/speculative loss, container network fault, CPU starvation, reconnect | affected state becomes safer, never more active |
| Recorder | dual-feed overload and disk pressure | no loss of P0/P1 account/execution evidence |
| economics | paired funnel/outcome/cost/uncertainty report | no latency-only promotion or double counting |

## Success-test coverage

- Node/public questions 1–15: baseline, writer, alignment, uncertainty, downstream/cost and demotion contracts above.
- Speculative questions 16–27: separate lane, exact reuse and S-matrix.
- Provider/Docker/CPU/IRQ/network/kernel questions 28–61: benchmark and primary research contracts.
- Sequencing/FIX/safety questions 62–78: fact audit and unchanged canonical authorities.
- Economic/CORR-05 questions 79–93: attribution, experiment and promotion contracts; completion evidence is consumable without redefining execution truth.

Passing tests do not authorize implementation or capital. Results map to existing M0–M5 and exact capability scope.
