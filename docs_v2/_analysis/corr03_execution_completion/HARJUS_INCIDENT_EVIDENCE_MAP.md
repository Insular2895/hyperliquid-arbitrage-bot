# CORR-03 — Harjus Incident Evidence Map

DOCUMENTATION STATUS: COMPARATIVE EVIDENCE CLASSIFICATION

| HJ ID | Classification | Primary support | Exact support | Not supported / inference boundary |
|---|---|---|---|---|
| `HJ-001` | `DIRECT_HARJUS_EVIDENCE` | 2025/2026 write-ups; v4 raw log | submitted FOK orders expire with zero quantity; failed executions | does not prove Hyperliquid reject codes or reservation rules |
| `HJ-002` | `PROJECT_FAILURE_SCENARIO` | general project safety design | order-level first-leg partial | Harjus reports route-level partial execution, not a production partial fill of one FOK order |
| `HJ-003` | `DIRECT_HARJUS_EVIDENCE` | both write-ups; v4 raw log | one or more trades filled, later order expires, route fails and inventory remains | exact affected leg varies; no project Recovery state is present |
| `HJ-004` | `PROJECT_FAILURE_SCENARIO` | inspired by incomplete paths | later-leg order partial | not directly established by Harjus production evidence |
| `HJ-005` | `PROJECT_FAILURE_SCENARIO` | generic transport ambiguity | lost submit response / possible transmission | Harjus log `UNKNOWN` is not proven lost-response ambiguity |
| `HJ-006` | `PROJECT_FAILURE_SCENARIO` | generic order lifecycle | fill during cancel race | Harjus FOK experiment does not establish this incident |
| `HJ-007` | `PROJECT_FAILURE_SCENARIO` | maker safety requirements | maker partial then cancel remainder | Harjus evidence is taker/FOK, not maker validation |
| `HJ-008` | `PROJECT_FAILURE_SCENARIO` | restart consistency requirements | crash during active execution | early-version resource crash is not evidence for a crash with active exposure |
| `HJ-009` | `PROJECT_FAILURE_SCENARIO` | idempotent exchange evidence | duplicate/late/out-of-order fill | no primary Harjus incident identified |
| `HJ-010` | `PROJECT_FAILURE_SCENARIO` | stranded inventory lesson | constrained/partial/failed Recovery | manual unwinding supports the problem, not the exact automated scenario |

Counts: directly evidenced `2/10`; project-derived/inspired `8/10`. These are validation scenario IDs, not Harjus issue IDs, formulas or runtime states.
