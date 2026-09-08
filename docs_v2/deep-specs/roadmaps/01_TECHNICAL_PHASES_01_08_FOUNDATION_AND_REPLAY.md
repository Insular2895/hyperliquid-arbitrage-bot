# Technical Phases 01–08 — Foundation and Replay

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

## Boundary

These phases create the smallest final-contract vertical slice from external observation to deterministic historical Core behavior. They intentionally end before strategy sophistication, real order effects or capital.

## Contract chain

```text
typed domain
→ external event boundary
→ immutable RAW
→ valid BookState + rule versions
→ structural route
→ exact formula output
→ deterministic Replay trace
```

| Phase | Producer contract | Consumer guarantee | Forbidden shortcut |
|---:|---|---|---|
| 1 | Strong IDs/units/events/versions/Clock/RNG/RunManifest | Values cannot cross domains without explicit conversion/provenance | Strings/floats/ambient time as hidden domain truth |
| 2 | Typed adapter events/errors | Invalid external payload cannot mutate Core | Parsing inside Book/strategy reducers |
| 3 | Ordered immutable RAW + quality | Original observation can be reinterpreted and audited | Logs/derived tables as historical truth |
| 4 | Valid versioned BookState | Later calculations consume coherent bids/asks/freshness | Silent gap repair or midpoint substitute |
| 5 | Point-in-time metadata/fees/precision | Route/formula/order boundary uses one rule version | Static hardcoded exchange examples |
| 6 | Fixed directed route definitions and indexes | Hot path evaluates bounded affected structures | Per-tick general graph search |
| 7 | One FormulaVersion/NetConvert core | Same state and q give same typed economics | Equation forks or double-counted costs |
| 8 | Same-Core ReplayReport/DecisionTrace | Every downstream behavior can be tested immediately | Separate simplified backtest engine |

## First useful vertical slice

Before the full Phase-8 exit, integrate a narrow fixture-driven route:

```text
RawEvent → Normalized MarketEvent → BookState
→ one precomputed route → NetConvert → Replay trace
```

It uses final types and reducers. It is small, not throwaway. It creates no capital effect.

## Failure inheritance

A payload error fails at Phase 2; a data gap makes Phase-4 state invalid; an unknown rule fails Phase 5; an invalid topology fails Phase 6; an invalid economic input fails Phase 7; an invalid region/lookahead/nondeterminism fails Phase 8. A later phase may not coerce any upstream invalid state into a usable zero/default.

## Evidence exits

- Phase 1: unit/property/misuse/serialization compatibility report.
- Phase 2: current fixture/conformance and reconnect report.
- Phase 3: checksummed RAW plus quality/backpressure/soak report.
- Phase 4: exact book-reconstruction report.
- Phase 5: metadata/fee/precision boundary golden report.
- Phase 6: deterministic route/invalidation report.
- Phase 7: PASS11 golden/parity report.
- Phase 8: repeatable `ReplayReport` and `DecisionTrace` hash.

No phase in this group authorizes real strategy capital.

CORR-04 mapping: Phase 2 validates the public HTTP/WebSocket feed/API baseline and versioned source profile; Phase 3 records canonical/challenger/speculative and infra evidence without P0/P1 loss; Phase 8 replays epistemic lanes separately and proves speculative reuse equals fresh canonical computation. Node/kernel bypass do not block these phases.
