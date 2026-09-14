# Calibration and Learned Documentation Ledger

This is a documentation index, not a runtime schema. Counts are derived from the current inventories and may change through governed reclassification.

| Source IDs / family | Class | Canonical owner | Earliest evidence | Minimum activation | Candidate provenance/support | Fallback / promotion / invalidation |
|---|---|---|---|---|---|---|
| OPEN-001..005, 023 | CALIBRATED infra profile/economics | Infrastructure Economics | current facts + infra benchmark | consumer-specific; Shadow before production | dated comparable distributions, uncertainty, cost/security | retain validated profile; explicit promotion; topology/provider/build drift invalidates |
| OPEN-004, 007 | CALIBRATED health/Risk values | Risk for risk limits; Infra Health for signals | Replay then Shadow/Micro-live as consumed | exact consumer M2–M4+ | distributions, false-trigger/tail sensitivity | owner-defined no-new-risk/shrink; human promotion where material |
| OPEN-009, 016 | CALIBRATED inventory/Atlas/support | Capital/Atlas/Validation | Replay/Shadow | consumer-specific | q/state support and sensitivity | zero/reject/shrink; drift/support loss contracts |
| OPEN-011 | CALIBRATED Recorder capacity/retention | Data/Recorder | soak/Recorder | before trusted affected evidence | throughput, backlog, restore and loss tests | bounded degradation; critical loss fails safe |
| OPEN-019,021,023,026 | CALIBRATED statistical conventions | named Formula consumer/statistical owner | Replay/offline training | consumer-specific | dataset, estimator, support, uncertainty, goldens | typed invalid/no promotion; data/model drift invalidates |
| OPEN-008,010,025 | LEARNED artifacts/parameters | Participants/Data | offline point-in-time training | model consumer M2 then Shadow/Micro-live as required | ModelReport, temporal OOS, censoring, support/OOD, checksum | empirical/no-model fallback; explicit promotion/demotion |
| QF-045,049,050,051,081,083 | LEARNED QF interfaces | Formula locks interface; Participants learns artifact | offline training | configured consumer-specific | exact target, versions, temporal OOS, calibration, OOD | cannot redefine QF; supported fallback or disable |
| OPEN-015,017,018,020,022,024,027,028 | IMPLEMENTATION_CHOICE | Operations/Formula/Capital as listed in Phase 14 | pre-implementation/Replay | applicable M1/M2 consumer gate | compatibility, deterministic/golden/parity evidence | typed invalid or simple enumeration; semantic change revalidates |
| OPEN-006,013 | DEFERRED | Infrastructure Product / Product Architecture | not yet applicable | separate future authorization | future source/evidence package | public-feed/same-venue baseline |
| OPEN-012,014 | HUMAN_POLICY_DECISION | Execution Product / Commercial Product | after eligibility | separate exact-scope approval | Phase-14 decision record | disabled/local fallback; expiry/scope change reopens |
| exchange/API/fees/provider/node facts | EXTERNAL_REVALIDATION | external-fact owner | dated verification | before affected implementation/promotion | authoritative source snapshot and conformance | last validated safe scope or disable |

Axes remain independent: class does not encode evidence stage, maturity or authority.
