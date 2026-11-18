# RAW, Normalized and Domain-event Schemas

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

## RAW envelope

`RawEvent` contains exactly `event_id`, `recorder_seq`, `source`, `source_connection_id`, optional `exchange_ts`, `recv_wallclock_ts`, `recv_monotonic_ns`, optional `market`, `event_type`, optional `source_seq`, optional `block_id`, `payload_bytes`, and `schema_version`.

`event_id` is unique enough for deduplication/trace/replay. `recorder_seq` is strictly monotonic per Recorder. The payload is the original byte representation available at capture, not a later JSON rendering.

Adapter reception first preserves `payload_bytes` plus provisional source, connection and receive
provenance. The complete canonical envelope is finalized when the authorized ingress serialization
boundary binds its stable `event_id` and assigns `recorder_seq` exactly once. This distinction
allows bounded Live normalization to run before or overlap ingress without losing an invalid/unknown
payload. Its valid or rejected typed outcome is later joined to `source_raw_event_id`; no outcome
may change the assigned sequence. The exact pre-assignment arbitration remains OPEN under `ARCH-016`.

## Normalized envelopes

`NormalizedEvent` adds `normalized_schema_version` and `source_raw_event_id`. The domain payload belongs to one closed family:

- `MarketEvent`: `BookSnapshot`, `BookDiff`, `Trade`, `MetadataUpdate`, `MarketStatus`, `Heartbeat`.
- `AccountEvent`: `OrderUpdate`, `Fill`, `BalanceUpdate`, `FeeUpdate`, `AccountSnapshot`.
- `EngineInputEvent`: `Market`, `Account`, `Infra`, `Timer`, `Control`.

Book levels and fills use ticks/lots; optional fields stay optional. Side is `Buy|Sell`, not a bool. Market and asset IDs are strong types. Metadata carries its version and invalidates dependent routes when changed.

## Ingestion outcomes

| Input | RAW | Normalize | State mutation |
|---|---|---|---|
| Valid known payload | retain | emit typed event | reducer may apply |
| Unknown optional field | retain | ignore only when compatibility says safe | allowed after validation |
| Unknown event type | retain | no guessed event; alert | forbidden |
| Missing required field | retain | reject with reason | forbidden |
| Negative size/impossible price/unknown market | retain | reject/quarantine | forbidden |
| Duplicate fill | retain | deduplicate by stable identity | apply once |

Fixtures cover real normal, edge, malformed and historical payload variants. Hyperliquid-specific timestamp, sequence and optional-field behavior must be checked against the current official interface.

Recorder persistence is a bounded background handoff after identity/outcome association. Storage
priority and writer completion do not change canonical order. A crash after sequence assignment but
before durability creates an explicit evidence gap; it cannot be relabeled complete and invokes the
`ARCH-019` restart/reconciliation boundary. Cross-recorder order requires a separately approved
versioned merge policy.
