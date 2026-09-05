# Market Atlas: Structure, Features and Rolling State

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Definition

Market Atlas is a rolling, versioned economic map derived from recorded evidence. It is not structural topology, current BookState, Strategy, Risk or Capital decision. Graph says what can exist; Atlas estimates what has been economically interesting; HWC decides where compute is spent.

## Records

Atlas groups semantic fields by market, route, asset, capital location and regime. Market fields cover spread/depth/liquidity, volatility/jumps, replenishment/resilience, competition/event intensity and execution quality. Route fields distinguish structural/active/reachable counts, opportunity episodes/frequency, edge distributions by q, survival/capture/completion/recovery and capacity. Asset/capital fields expose connectivity, exit liquidity, Bridge usefulness and PASS07-owned terminal/capital context.

Exact schema is PASS06-owned. Structural fields carry Graph/Route/Metadata versions. Learned fields carry horizon, support/confidence, ModelVersion, DatasetVersion/RunManifest and last evidence time.

## Horizons and evidence

FAST, RECENT, MEDIUM and LONG horizon identities are retained, but exact windows are calibrated. Evidence from Replay, Shadow, Micro-live and Live is labelled by source/mode; predictions, rejections and actual fills are not merged. OpportunityEpisode semantics avoid counting one persistent edge as thousands of independent observations.

## Update

Rolling updates are incremental by affected market/route/asset, not full-history rescans. Sparse/new markets start with low support, enter the Graph and remain COLD/WARM until evidence supports more. Historical records survive delisting while current availability is false.

## Governance

Atlas scores/weights are learned or research heuristics, never constitutional truth. Formula definitions do not self-modify. Promotion requires Replay/OOS/Shadow/Micro-live governance. Atlas cannot override current books, structural validity, comparator requirements, Risk or PASS07 terminal decisions.

See [field catalog](../../_analysis/pass08_graph_routes_quant/MARKET_ATLAS_FIELD_CATALOG.md) and [dependency map](../../_analysis/pass08_graph_routes_quant/MARKET_ATLAS_DEPENDENCY_MAP.md).
