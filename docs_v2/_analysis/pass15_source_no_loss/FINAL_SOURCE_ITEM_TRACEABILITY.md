# Final Source Item Traceability

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

The machine-readable companion [FINAL_SOURCE_ITEM_TRACEABILITY.csv](FINAL_SOURCE_ITEM_TRACEABILITY.csv) is the authoritative row-level join. It contains **2,669 rows**: 2,577 PASS00 atomic source items, 13 explicit PASS00 cross-domain derivations, and 79 PASS15 recovered source items. Requirement IDs are unchanged.

## Reading the ledger

- `CanonicalMaster` is the single owner or the already-defined distributed Accounting boundary; blank means non-active research trace only.
- `CanonicalDeepSpec` resolves logical PASS00 destinations to an existing physical index/spec or the trace-only register.
- `CanonicalSection` names the contract family; `RequirementId` joins to exact row-level domain ledgers and `DOCUMENT_TARGET_MAP.md`.
- `CoverageQuality` uses only `EXACT`, `FULL`, `SUBSTANTIAL`, `PARTIAL`, `TRACE_ONLY`, or `MISSING`.
- `TRACE_ONLY` is reserved for external snapshots/revalidation, superseded or rejected material. It is not used to hide current implementation semantics.
- The CSV preserves PASS00 provenance status. Domain-pass reviewed overlays remain authoritative where keyword heuristics were corrected; PASS15 introduced no new status or authority override.

## Control totals

| Population | Rows | Present in V2 | Destinationless current | MISSING | unexplained PARTIAL |
|---|---:|---:|---:|---:|---:|
| PASS00 atomic source items | 2,577 | 2,577 | 0 | 0 | 0 |
| PASS00 overlay/candidate derivations | 13 | 13 | 0 | 0 | 0 |
| PASS15 recovered source items | 79 | 79 | 0 | 0 | 0 |
| **Total trace rows** | **2,669** | **2,669** | **0** | **0** | **0** |
