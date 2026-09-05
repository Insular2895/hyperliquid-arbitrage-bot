# Graph / Routing Requirement Ledger

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

This ledger closes all **574/574** rows of `../domain_indexes/ROUTING.md`. Every indexed source range was reopened; none was empty or outside its original file. The union with QUANT contains **1,013** unique requirements: the two indexes overlap on 158 IDs and are not treated as 1,171 independent requirements.

## Coverage

| Source | Reviewed |
|---|---:|
| SRC-001 | 65 |
| SRC-002 | 108 |
| SRC-003 | 77 |
| SRC-004 | 62 |
| SRC-005 | 89 |
| SRC-006 | 51 |
| SRC-007 | 83 |
| SRC-008 | 39 |
| **Total** | **574** |

| Classification | Count |
|---|---:|
| Graph-owned | 14 |
| Route-owned | 39 |
| OWA-owned | 8 |
| Triangle-owned | 5 |
| HOT/WARM/COLD-owned | 12 |
| Atlas-owned | 3 |
| Quant interface | 7 |
| Formula reference | 26 |
| Other cross-domain | 460 |
| **Total** | **574** |

| Disposition | Count |
|---|---:|
| `MASTER` | 9 |
| `DEEP_SPEC` | 7 |
| `FORMULA_REFERENCE` | 26 |
| `CROSS_DOMAIN_EXISTING_PASS` | 231 |
| `CROSS_DOMAIN_FUTURE_PASS` | 17 |
| `RESEARCH/FUTURE` | 233 |
| `EXTERNAL_REGISTER` | 37 |
| `OPEN_ITEM` | 1 |
| `SUPERSEDED` | 1 |
| `REJECTED` | 12 |
| **Total** | **574** |
| **Destinationless** | **0** |

## Deterministic row disposition

This rule set assigns a destination to every stable ID without renumbering or duplicating the PASS00 ledger:

1. `GRAPH`, `ROUTE`, `OWA`, `TRI`, `HWC`, and `ATLAS` are PASS08-owned. Their PASS00 `LOCKED` rows target `03_MARKET_GRAPH_AND_ROUTES.md`; calibrated detail targets a graph deep spec; research/future, external, open, superseded and rejected rows retain the corresponding allowed disposition.
2. `FORMULA` rows target `FORMULA_CROSSCHECK.md` and the immutable Formula Index; equations remain PASS11-owned.
3. `QUANT` and `MICRO` rows target the PASS08 Quant master/deep specs as interface requirements.
4. Completed Participant, Simulator, Inventory/Capital, Risk, Execution and Data/Replay requirements retain their existing master. Deployment, Security, Client, Product and Operations work routes to a future pass.
5. A cross-domain row whose source status is research/future, external, open, superseded or rejected retains that conservative disposition; it is not promoted merely because it appears in the Routing index.

## Closure overlays

Later source closure and the PASS08 authority order lock the following architecture even where early PASS00 rows were exploratory: directed economic conversions; venue-aware identity; fixed `DirectRoute`, `Route2Leg` and `Cycle3Leg`; valid direct comparator for OWA; Bridge classification without that comparator; precomputation plus `pair_to_routes`; global topology with selective route activation; `NetConvert(q)`; separation of ConversionAlpha and ExecutionAlpha. These corrections are enumerated in `CONFLICT_RESOLUTION.md` and do not overwrite the original source status.

## Destinations

- Master: `../../03_MARKET_GRAPH_AND_ROUTES.md`.
- Graph details: `../../deep-specs/market-graph/`.
- Quant interfaces: `../../05_MARKET_MICROSTRUCTURE.md` and `../../deep-specs/market-microstructure/`.
- Formulas: `../FORMULA_INDEX.md`, this pass's `FORMULA_CROSSCHECK.md`, then PASS11.
- Exchange facts: `../EXTERNAL_REVALIDATION_REGISTER.md`.
- Cross-domain ownership: masters 06–13 and future PASS09/PASS10/PASS12/PASS13.

Destinationless requirements: **0**.
