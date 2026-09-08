# CORR-01 — Market Opportunity Episode Identity Contract

DOCUMENTATION STATUS: POST-RECONSTRUCTION CORRECTION — AWAITING HUMAN REVIEW

## Selected identity

The canonical grouping key is `OpportunityEpisodeId`, not `MarketEpisodeId`. It groups repeated exact-valid Opportunities for one directed `RouteId`; it does not claim to identify a general market regime or an exchange-native object.

## Three distinct identities

| Identity | Cardinality | Created by | Purpose |
|---|---:|---|---|
| `RouteEvaluationId` | one per route evaluation at an explicit input/version set | Market Graph | count cheap/exact work, including rejects |
| `OpportunityId` | one per immutable exact-valid opportunity observation | Market Graph | decision and forecast lineage |
| `OpportunityEpisodeId` | one per derived contiguous opportunity run under one segmentation version | offline/near-line episode projector | survival, duration, attempts-per-episode and selection-bias analysis |

Repeated observations in one episode have different `OpportunityId`s. Multiple attempts may attach to one episode. One attempt attaches to exactly one originating `OpportunityId` and at most one derived episode version.

## Episode key and segmentation

Required grouping dimensions:

```text
(VenueId, directed RouteId, StrategyId, RunMode,
 OpportunityPredicateVersion, EpisodeSegmentationVersion)
```

An episode begins at the first `CF-05 EXACT_CANDIDATE_VALID` observation after the predicate was false/invalid/not observed beyond the segmentation gap policy. It ends when the predicate is observed false, becomes invalid, the route/topology identity changes, or the calibrated maximum observation gap is exceeded. End reason is explicit: `PREDICATE_FALSE`, `INVALIDATED`, `ROUTE_VERSION_CHANGED`, `GAP_CENSORED`, `RUN_ENDED`.

Exact gap duration, grace observations, threshold hysteresis and whether a short invalid interval bridges are `CALIBRATED` under `EpisodeSegmentationVersion`; no number is frozen by CORR-01. Both left- and right-censoring are recorded. Episode counts from different segmentation versions are not pooled.

## Derived identifier

`OpportunityEpisodeId` is a deterministic content-derived identifier over the grouping dimensions, first qualifying `OpportunityId`, first qualifying ordered-event position and segmentation version. The hash algorithm and canonical byte encoding remain an implementation choice, but replay of identical evidence/version must reproduce the same ID.

## Required episode record

- `opportunity_episode_id`, grouping dimensions and segmentation version;
- first/last observation IDs and ordered positions;
- `start_recv_ts`, `end_recv_ts` or censoring marker;
- member Opportunity count and optional exact member references;
- maximum/area-under-duration summaries only with declared units and aggregation method;
- linked attempt IDs, first-attempt delay and attempt count;
- start/end reasons, missing intervals, source/mode and validity;
- derivation run manifest and projection version.

## Runtime and storage boundary

Episode construction is not required in the synchronous hot path. A near-line projector may emit provisional episodes; finalization and later correction are append-only. High-cardinality membership belongs in durable analytical evidence, not metric labels. Operators may display episode summaries only when segmentation/version/censoring are visible.
