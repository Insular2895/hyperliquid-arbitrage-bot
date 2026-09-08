# Post-Reconstruction Human Decisions

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

These records preserve requirements explicitly supplied after PASS 16. They are not retroactively attributed to SRC-001..SRC-008 and do not modify the PASS 00 source inventory.

| ID | Origin | Date | Baseline | Decision | Relationship | Affected canonical documents | Validation / roadmap impact | Approval |
|---|---|---|---|---|---|---|---|---|
| `HDC-001` | `HUMAN_POST_RECONSTRUCTION` | 2026-09-08 | `fdb4a25588670fb245edebc0650d262c7f536b4c` | Add a canonical capture funnel that distinguishes observed, evaluated, detected, eligible, attempted, filled, completed, reconciled and economically positive populations. It is an evidence projection, not a runtime state machine. | `STRENGTHENING` | Masters 00/03/10/11/12/16/18/19; Operations deep spec 11 | exact population and reconstruction validation; map into existing phases/stages | `PENDING FINAL REVIEW` |
| `HDC-002` | `HUMAN_POST_RECONSTRUCTION` | 2026-09-08 | `fdb4a25588670fb245edebc0650d262c7f536b4c` | Define event-level Opportunity identity and a versioned offline/near-line `OpportunityEpisodeId`; do not put episode segmentation on the hot path or claim exchange truth. | `NEW REQUIREMENT` | Masters 03/11/12/16/18; Operations deep spec 11 | segmentation stability, overlap and censored-boundary tests | `PENDING FINAL REVIEW` |
| `HDC-003` | `HUMAN_POST_RECONSTRUCTION` | 2026-09-08 | `fdb4a25588670fb245edebc0650d262c7f536b4c` | Freeze attempt-time execution forecasts and join them immutably to actual fill, completion, recovery, reconciliation and economic labels. | `STRENGTHENING` | Masters 07/10/11/12/16/18; Operations deep spec 11 | join-completeness, calibration and bias tests | `PENDING FINAL REVIEW` |
| `HDC-004` | `HUMAN_POST_RECONSTRUCTION` | 2026-09-08 | `fdb4a25588670fb245edebc0650d262c7f536b4c` | Define named timing points and non-overlapping latency stages with clock, mode, scope, missing-data and external-timestamp semantics. | `NEW REQUIREMENT` | Masters 00/11/12/13/16/18; Operations deep spec 11 | endpoint, monotonicity, additive-boundary and instrumentation-overhead validation | `PENDING FINAL REVIEW` |
| `HDC-005` | `HUMAN_POST_RECONSTRUCTION` | 2026-09-08 | `fdb4a25588670fb245edebc0650d262c7f536b4c` | Every capture/latency metric must state numerator, denominator, population, exclusions, scope, time basis, window, dimensions, records, missing-data policy, minimum sample, consumer, status and bias risk. | `NEW REQUIREMENT` | Masters 11/12/16/18; Operations deep spec 11 | contract linting, empty/small cohort and missingness validation | `PENDING FINAL REVIEW` |
| `HDC-006` | `HUMAN_POST_RECONSTRUCTION` | 2026-09-08 | `fdb4a25588670fb245edebc0650d262c7f536b4c` | A technical optimization requires endpoint-valid measurement, controlled attribution, comparable remeasurement, funnel movement and robust economic evidence; speed alone cannot authorize promotion. | `SOURCE-COMPATIBLE STRENGTHENING` | Masters 13/16/17/18/19; Operations deep spec 11 | controlled experiment and economic gate in existing phases/stages | `PENDING FINAL REVIEW` |

## Approval boundary

The requirement origin is human and explicit; acceptance of the resulting canonical wording remains pending review. No row authorizes Phase 1, Micro-live, Live, capital, legacy switchover or implementation.
