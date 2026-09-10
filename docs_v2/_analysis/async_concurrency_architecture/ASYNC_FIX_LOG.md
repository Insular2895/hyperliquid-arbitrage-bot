# Async Architecture Fix Log

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

| ID | Finding | Disposition | Files |
|---|---|---|---|
| AF-001 | Existing architecture had bounded async/single-writer principles but no unified C0–C5 classification. | Added architectural classes without mandating Rust types/tasks. | system map, matrix, architecture deep spec/master |
| AF-002 | Worker provenance existed but deadline/generation/revalidation/memory lifecycle was distributed. | Consolidated exact stale-result contract. | stale/versioning, Data |
| AF-003 | No repository-wide per-function concurrency inventory. | Classified major functions and authorities in the master matrix. | function matrix |
| AF-004 | Route parallelization lacked a final decision-policy boundary. | Specified two safe calibrated candidates; first-worker-wins forbidden; no winner invented. | route policy, HDC ledger |
| AF-005 | Full L2 and q-grid location could be read as prematurely parallel. | Fixed initial inline baseline and kept C2 variants benchmark-only. | sequential table, experiment matrix |
| AF-006 | External effect semantics existed but coordinator non-blocking behavior needed one explicit contract. | Classified submit/cancel/query/reconciliation effects and ordered returns. | effect contract, Execution |
| AF-007 | Recorder background principle lacked checkpoint capture/serialization split in one place. | Split short ordered snapshot capture from C4 serialize/checksum/write. | Recorder contract, Recorder/Data |
| AF-008 | Small-host oversubscription risk was not explicit enough. | Added two-vCPU scheduler/starvation treatment; no numeric worker choice. | CPU contract, Infrastructure |
| AF-009 | Replay determinism did not enumerate scheduler permutations. | Added CT-001..015 and policy-aware trace rules. | concurrency Replay, Validation |
| AF-010 | Startup/shutdown task ordering and failure scoping were distributed. | Added deterministic readiness/drain contract and failure matrix. | lifecycle/failure contracts, Operations |

No source, build, dependency, Docker, runtime configuration, legacy documentation, formula or implementation file was changed.
