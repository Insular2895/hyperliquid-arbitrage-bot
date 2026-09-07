# Architecture Conflict Resolution

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

PASS 13 did not reopen domain-resolved conflicts 001–126. It verified that their cross-domain consequences are consistently representable and recorded the following architecture-only clarifications.

| Architecture issue | Competing readings | Resolution | Authority / result |
|---|---|---|---|
| Monolith vs modules | one deployable could imply one undifferentiated module; component map could imply microservices | modular monolith: one process/deployment, strong internal contracts | PASS09 + PASS12; RESOLVED |
| Risk ordering around sizing | Risk only at end vs Risk entirely before economics | staged gates: early eligibility, T1 pre-reservation, T2 pre-send, T3–T5 execution | PASS05/07/12; RESOLVED |
| Account/Inventory/Reservation mutation | Execution coordinator could appear to own every state | ordered coordinator sequences distinct single-writer reducers; each state retains its domain owner | PASS04/06/07; RESOLVED |
| Participant dependency for TTT | all TTT waits for sophisticated model vs no model dependency ever | capability-specific dependency; basic TTT baseline remains possible | PASS02/12; RESOLVED |
| HWC/Atlas/Risk | HOT could imply interesting and safe | Graph=structure, Atlas=evidence, HWC=compute relevance, Risk=permission | PASS07/08; RESOLVED |
| Recovery/Execution circularity | each might directly call/mutate the other | Recovery proposes a new plan; Risk authorizes; Execution applies effects through ordered events | PASS04/05; RESOLVED |
| License failure | commercial disable could stop all execution | new commercial risk stops; safe cancel/Recovery/Reconciliation/data access remain | PASS09; RESOLVED |
| Update/rollback state | software state could overwrite exchange reality | current exchange truth and reconciliation always win | PASS04/09; RESOLVED |

Architecture-only conflicts found/resolved: **8/8**. Remaining domain-changing questions are recorded as four PASS14 gaps, not resolved here. No new permanent project decision, status change or numeric calibration was introduced.
