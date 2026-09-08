# CORR-02 — Baseline and Scope

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

| Field | Value |
|---|---|
| `CORR02_BASELINE_COMMIT` | `eb6f48a688459430b7230c1903c264aa59915a7e` |
| Branch | `codex-docs` |
| Baseline captured | 2026-09-08 |
| CORR-01 prerequisite | `VERIFIED` |
| Work class | documentation, contracts, benchmarks and evidence gates only |
| Human approval | `PENDING FINAL REVIEW` |
| Implementation | `NOT AUTHORIZED` |

## Scope

CORR-02 specifies how to reduce hot-path work without changing executable economics, state ownership, Risk authority, execution behavior or deterministic Replay. Its order of attack is:

`less work → locality/layout → fewer allocations/copies → exact specialization → measured Rust/compiler tuning → proven contention removal → possible C++ review`.

The safety order remains `Safety > StateConsistency > ExistingExposure > RiskLimits > ExpectedPnL > Opportunity`. A faster wrong answer is failure.

## Explicit exclusions

No source code, Cargo profile, build script, FFI, executable benchmark, allocator replacement, Docker, CI, provider, CPU pinning, kernel tuning, node, AF_XDP, DPDK or F-Stack change is made. CORR-02 does not choose a queue, allocator, container, compiler flag, dense representation, numeric threshold or foreign-language library.

## Semantic boundary

- QF-001–QF-110 and `FormulaVersion` semantics are unchanged.
- QF-016 `NetConvert` remains the sole canonical executable conversion.
- BBO may validate state, prove a conservative rejection, prove exact L1 specialization eligibility, or prioritize work; these four roles are not interchangeable.
- `pair_to_routes` remains the logical reverse dependency contract.
- Stable canonical IDs remain authoritative; runtime indices are generation-local accelerators only.
- Critical state retains one logical writer.
- Every transparent optimization must preserve canonical outputs, reasons, versions and `DecisionTrace`.

## Audit effect

PASS 14, PASS 15 and the PASS 16 review package predate this correction. Their historical reports are not rewritten. The review baseline remains stale during the CORR series and will be refreshed by CORR-06.
