# Quant Requirement Ledger

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

This ledger closes all **597/597** rows of `../domain_indexes/QUANT.md`. Every original locator was reopened and returned content. Formula rows are indexed and consumed here, not rewritten.

## Coverage

| Source | Reviewed |
|---|---:|
| SRC-001 | 28 |
| SRC-002 | 59 |
| SRC-003 | 27 |
| SRC-004 | 156 |
| SRC-005 | 62 |
| SRC-006 | 45 |
| SRC-007 | 146 |
| SRC-008 | 74 |
| **Total** | **597** |

| Classification | Count |
|---|---:|
| Quant-owned | 34 |
| Microstructure-owned | 29 |
| Routing interface | 23 |
| Formula reference | 151 |
| Other cross-domain | 360 |
| **Total** | **597** |

| Disposition | Count |
|---|---:|
| `MASTER` | 8 |
| `DEEP_SPEC` | 27 |
| `FORMULA_REFERENCE` | 151 |
| `CROSS_DOMAIN_EXISTING_PASS` | 151 |
| `CROSS_DOMAIN_FUTURE_PASS` | 15 |
| `RESEARCH/FUTURE` | 201 |
| `EXTERNAL_REGISTER` | 41 |
| `REJECTED` | 3 |
| **Total** | **597** |
| **Destinationless** | **0** |

## Deterministic row disposition

1. `QUANT` and `MICRO` rows are PASS08-owned. Locked rows target `05_MARKET_MICROSTRUCTURE.md`; calibrated/learned detail targets a Quant deep spec; research/future, external and rejected rows retain conservative status.
2. All `FORMULA` rows are `FORMULA_REFERENCE`: SRC-004 and `../FORMULA_INDEX.md` remain authoritative, with exact expression/unit audit deferred to PASS11.
3. `GRAPH`, `ROUTE`, `OWA`, `TRI`, `HWC`, and `ATLAS` rows target this pass's Graph master/deep specs.
4. Completed domains retain their authoritative masters; Deployment/Security/Client/Product/Operations remain future-pass interfaces.
5. Status is never promoted from an early research statement unless an explicit later closure is documented in `CONFLICT_RESOLUTION.md`.

## Canonical Quant closure

QF-001–QF-043 are consumed as locked Formula Book definitions. PASS08 specifies semantics, units at interfaces, provenance, incremental computation and ownership. It does not create alternative equations. True event-level OFI stays distinct from snapshot proxy; Microprice is a feature rather than guaranteed fair value; Mechanical Impact stays distinct from learned Liquidity Resilience. Production hot-path ownership is Rust; Python is used for research, calibration, golden vectors and parity. No blocking I/O or unbounded history scan belongs in opportunity evaluation.

## Destinations

- Master: `../../05_MARKET_MICROSTRUCTURE.md`.
- Detailed contracts: `../../deep-specs/market-microstructure/`.
- Route economics: `../../03_MARKET_GRAPH_AND_ROUTES.md` and `../../deep-specs/market-graph/`.
- Formula audit: `../FORMULA_INDEX.md`, `FORMULA_CROSSCHECK.md`, PASS11.
- Exchange rules: `../EXTERNAL_REVALIDATION_REGISTER.md`.

Destinationless requirements: **0**.
