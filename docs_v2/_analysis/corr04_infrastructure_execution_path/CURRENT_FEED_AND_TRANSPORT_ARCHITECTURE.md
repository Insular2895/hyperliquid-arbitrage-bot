# Current Feed and Transport Architecture

`STATUS: SPECIFIED — IMPLEMENTATION NOT AUTHORIZED`

## Current V1 boundary

```text
public WebSocket/HTTP feed -> public adapter -> canonical normalizer
-> single canonical BookState writer -> Core/Risk/ExecutionTransport

node/other feed -> challenger adapter -> isolated comparison state
-> Recorder/Shadow/research only
```

The documented order-entry transports are HTTP `/exchange` and WebSocket post requests. `ExecutionTransport` stays protocol-abstract, but no FIX adapter is current. Transport response/ACK, order status, fill and `FullRouteCompletion` are separate facts.

## Identities

Each run binds `FeedProfileId`, source, adapter/schema version, node build/flags if any, `InfraProfileId`, container/network/CPU profile, bot build and config through linked evidence. Exactly one declared feed profile writes canonical market state for the run.

## Forbidden shortcuts

No feed fusion, silent mid-run source switch, dual canonical reducer, node-to-order shortcut, speculative `BookState`, ACK-as-fill or latency-only promotion. Any future canonical feed change is material and repeats affected Replay, Shadow, readiness, model and Simulator validation.
