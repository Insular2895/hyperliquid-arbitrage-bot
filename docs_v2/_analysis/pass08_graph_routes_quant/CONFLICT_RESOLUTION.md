# Conflict Resolution

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| ID | Earlier variant | Canonical resolution | Status/authority |
|---|---|---|---|
| P08-C01 | undirected pair graph | two directed economic conversions per market | `LOCKED`; SRC-003/004 |
| P08-C02 | generic path discovery on each tick | precomputed fixed 2/3-leg routes; general graph only offline/future | `LOCKED`; later architecture |
| P08-C03 | scan every route on every update | `pair_to_routes` affected-route lookup | `LOCKED`; SRC-001/005 |
| P08-C04 | midpoint/product opportunity | BBO only prefilters; exact L2 `NetConvert(q)` decides economics | `LOCKED`; SRC-003/004 |
| P08-C05 | hardcoded fee | dynamic Fee Engine/version | `LOCKED`; current values external |
| P08-C06 | one fixed route edge | `Edge(q)` plus QF-027 size boundary | `LOCKED`; QF-026/027 |
| P08-C07 | every two-leg path is OWA | OWA requires valid direct A→B comparator | `LOCKED`; QF-017–020 |
| P08-C08 | no comparator but still OWA | classify as Bridge/Capital Relocation candidate | `LOCKED`; SRC-003/PASS07 |
| P08-C09 | graph equals opportunity/quality map | Graph = topology; Atlas = economic evidence; Opportunity = transient state | `LOCKED` |
| P08-C10 | cold markets ignored | Global Watcher and broad Recorder retain cheap awareness | `LOCKED` architecture |
| P08-C11 | static whitelist/tier | rolling HWC/Atlas state with governed hysteresis; exact thresholds calibrated | `REFINED` |
| P08-C12 | capital dictates HOT/topology | capital and HWC inform activation; topology remains metadata truth | `LOCKED` boundary |
| P08-C13 | conversion and execution improvement merged | QF-024 ConversionAlpha distinct from QF-025 ExecutionAlpha | `LOCKED`; SRC-004 |
| P08-C14 | dense global expensive compute | global structural knowledge, selective compute follows capital/productivity | `LOCKED` architecture |
| P08-C15 | single-venue identity | venue-aware graph; only same-venue Hyperliquid spot activated in V1 | `LOCKED V1` + `FUTURE` XEX |
| P08-C16 | linear depth/slippage | exact book walk per q; no constant coefficient when L2 exists | `LOCKED`; QF-009–016 |
| P08-C17 | three legs imply Triangle | only A→X→B→A exact closure is Triangle | `LOCKED`; QF-021–023 |
| P08-C18 | current topology/Atlas used in all Replay | historical Graph/Route/Atlas/metadata versions at T | `LOCKED`; PASS06 |

Conflicts found: **18** source-evolution classes. Resolved: **18/18** through closure authority and later explicit decisions. Remaining documentary conflicts: **0**. Calibration, external exchange rules and future cross-exchange work are dependencies, not silently resolved facts.
