# Deployment / Security Requirement Ledger

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

This ledger closes all **426/426** rows of `../domain_indexes/DEPLOYMENT_SECURITY.md`. Every indexed locator was reopened against its original source; failures: **0**. Stable requirement IDs and PASS00 source statuses are preserved.

## Coverage

| Source | Reviewed |
|---|---:|
| SRC-001 | 10 |
| SRC-002 | 17 |
| SRC-003 | 6 |
| SRC-004 | 18 |
| SRC-005 | 36 |
| SRC-006 | 299 |
| SRC-007 | 12 |
| SRC-008 | 28 |
| **Total** | **426** |

| Classification | Count |
|---|---:|
| Deployment-owned | 220 |
| Security-owned | 21 |
| Distribution-owned | 28 |
| Licensing-owned | 7 |
| Operations interface | 6 |
| Infrastructure interface | 22 |
| Risk interface | 19 |
| Data interface | 22 |
| Validation interface | 33 |
| Other cross-domain | 48 |
| **Total** | **426** |

| Disposition | Count |
|---|---:|
| `MASTER` | 263 |
| `DEEP_SPEC` | 1 |
| `CROSS_DOMAIN_EXISTING_PASS` | 70 |
| `CROSS_DOMAIN_FUTURE_PASS` | 31 |
| `RESEARCH/FUTURE` | 41 |
| `EXTERNAL_REGISTER` | 14 |
| `OPEN_ITEM` | 3 |
| `SUPERSEDED` | 1 |
| `REJECTED` | 2 |
| **Total** | **426** |
| **Destinationless** | **0** |

## Deterministic disposition

1. `DEPLOY`, `SEC`, `CLIENT` and `LIC` are PASS09-owned. Their `LOCKED` rows target `../../14_DEPLOYMENT_AND_DOCKER.md`; the one `CALIBRATED` row targets a deployment-security deep spec.
2. Owned `RESEARCH`/`FUTURE`, `EXTERNAL_REVALIDATION`, `OPEN`, `SUPERSEDED` and `REJECTED` rows retain those conservative dispositions.
3. Locked/calibrated Infrastructure, Risk, Execution, Data, Determinism, Inventory, Routing, Quant, Simulator and Formula interfaces retain their completed owner through `CROSS_DOMAIN_EXISTING_PASS`.
4. Validation and Operations requirements whose owning reconstruction has not occurred route to `CROSS_DOMAIN_FUTURE_PASS`; their deployment-facing interface is specified here without pre-empting those passes.
5. External facts also enter `../EXTERNAL_REVALIDATION_REGISTER.md`. Commercial choices such as price, customer count, provider and exact license grace duration are policy/open facts, not silently converted into technical invariants.

## Authority corrections

SRC-006 Dossier 5 closure supersedes exploratory alternatives where it is explicit: isolated client-owned deployment rather than centralized execution SaaS; one initial VPS and OCI container rather than a distributed baseline; immutable version/digest rather than production `latest`; cached signed license outside the hot path; recovery remains possible under license failure; client-owned diagnostics with mandatory secret exclusion. `CONFLICT_RESOLUTION.md` records the corrections.

## Destinations

- Master: `../../14_DEPLOYMENT_AND_DOCKER.md`.
- Detail: `../../deep-specs/deployment-security/`.
- Existing owners: masters `03`, `05`–`13` and their deep specs.
- Future owners: Validation and Operations passes.
- External facts: `../EXTERNAL_REVALIDATION_REGISTER.md`.

Destinationless requirements: **0**.
