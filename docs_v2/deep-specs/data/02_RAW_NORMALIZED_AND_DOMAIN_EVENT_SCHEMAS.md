# RAW, Normalized and Domain-event Schemas

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## RAW envelope

`RawEvent` contains exactly `event_id`, `recorder_seq`, `source`, `source_connection_id`, optional `exchange_ts`, `recv_wallclock_ts`, `recv_monotonic_ns`, optional `market`, `event_type`, optional `source_seq`, optional `block_id`, `payload_bytes`, and `schema_version`.

`event_id` is unique enough for deduplication/trace/replay. `recorder_seq` is strictly monotonic per Recorder. The payload is the original byte representation available at capture, not a later JSON rendering.

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
