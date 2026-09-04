# 02 — Exchange Emulator and Arrival Timeline

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## Responsibility

`HyperliquidExchangeEmulator` reproduces exchange-visible acceptance, ordering, matching, fill/partial/cancel events, precision, fees, and state transitions closely enough for declared fidelity. `ReplayTransport` submits the same `OrderIntent` shape and produces the same `OrderEvents`/`FillEvents` schemas consumed by the core engine. Execution closure remains authoritative.

Architecture is compatible with IOC, ALO/Post Only, GTC, and price-time priority. Those current Hyperliquid facts, block/action ordering, and API fields are date-sensitive and remain `EXTERNAL_REVALIDATION`. No F1 claim may quietly rely on an unverified current rule.

## Arrival timeline

```text
market event received at t0
→ decode → book → route → simulation → risk → decision
→ sign → send/network → exchange ingress/order → matching
→ t_arrival
```

SRC-008's compact concept is `t_arrival = t0 + L_compute + L_sign + L_network + L_exchange`. QF-084 is authoritative: it includes `L_feed`, uses `L_send`, and decomposes compute into decode, book, route, simulation, risk, and decision. Components come from measured `LatencyTrace` distributions or an explicitly controlled test value.

## Arrival book invariant

The execution state is the book at simulated arrival, not the observation book. A zero-latency `t0` book is allowed only as an explicit test assumption. `recv_ts` establishes what the bot knew; `exchange_ts` is not a look-ahead channel. Exchange ordering finer than available timestamps must be disclosed as uncertainty.

## Deterministic mechanics

At a fixed arrival book and accepted order:

- QF-007/QF-008 provide authoritative precision references;
- QF-009/QF-010 walk bids/asks;
- QF-011 derives VWAP, undefined at zero fill;
- QF-012/QF-013 derive non-negative adverse slippage versus BBO;
- QF-014/QF-015 use the applicable historical fee state;
- QF-016 `NetConvert` keeps book, fee, precision, rules, and execution mode together;
- protected price and time-in-force determine residual handling;
- the same Execution State Machine and Recovery Engine handle events.

No duplicated `live_*` and `backtest_*` formula implementations are allowed.

## Boundary and errors

Invalid price/size, rejected order, exhausted protected depth, partial fill, IOC residual, ALO crossing, cancel/fill race, stale arrival state, and unsupported rule version are explicit outcomes. PASS 04 will close exact transitions. The Simulator must not invent a fill to keep a path profitable.

## Validation

Golden mechanics fixtures, historical fee/precision schedules, property invariants, replay determinism, and Predicted-versus-Actual Micro-live fills are required. Feed/API/rule revalidation precedes implementation reliance.
