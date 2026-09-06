# Formula Status Audit

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

SRC-004 status labels were read at each QF heading. The former discovery index normalized labels to broad classes; this audit preserves source specificity.

| QF | Exact source status evidence | Final audit status | Former index comparison |
|---|---|---|---|
| QF-001–007 | LOCKED (QF-001 rendered `Status : LOCKED`) | LOCKED | compatible normalization |
| QF-008 | LOCKED EXCHANGE RULE | LOCKED EXCHANGE RULE | specificity recovered |
| QF-009–013 | LOCKED | LOCKED | exact |
| QF-014 | LOCKED SOURCE, DYNAMIC VALUE | same | specificity recovered |
| QF-015 | LOCKED | LOCKED | exact |
| QF-016 | LOCKED ARCHITECTURE | same | specificity recovered |
| QF-017–025 | LOCKED | LOCKED | exact |
| QF-026 | LOCKED OBJECT | same | specificity recovered |
| QF-027 | LOCKED DEFINITION | same | specificity recovered |
| QF-028 | LOCKED | LOCKED | exact |
| QF-029 | LOCKED; prose says weights configured/calibrated | LOCKED STRUCTURE / CALIBRATED WEIGHTS | mixed semantic recovered |
| QF-030 | LOCKED DEFINITION | same | specificity recovered |
| QF-031–032 | LOCKED | LOCKED | exact |
| QF-033 | LOCKED STRUCTURE / CALIBRATED WEIGHTS | same | specificity recovered |
| QF-034–038 | LOCKED | LOCKED | exact |
| QF-039 | LOCKED STRUCTURE / CALIBRATED THRESHOLD | same | specificity recovered |
| QF-040–043 | LOCKED | LOCKED | exact |
| QF-044 | LOCKED OBJECT | same | specificity recovered |
| QF-045 | LEARNED | LEARNED | exact |
| QF-046–048 | LOCKED | LOCKED | exact |
| QF-049 | LEARNED DISTRIBUTION | same | specificity recovered |
| QF-050–051 | LEARNED | LEARNED | exact |
| QF-052 | LOCKED FROM SURVIVAL | same | specificity recovered |
| QF-053 | LOCKED DEFINITION | same | specificity recovered |
| QF-054–056 | LOCKED | LOCKED | exact |
| QF-057 | LOCKED STRUCTURE | same | specificity recovered |
| QF-058 | LOCKED STRUCTURE / LEARNED COMPONENTS | same | specificity recovered |
| QF-059–062 | LOCKED | LOCKED | exact |
| QF-063 | CALIBRATED | CALIBRATED | exact |
| QF-064 | LOCKED | LOCKED | exact |
| QF-065 | CALIBRATED | CALIBRATED | exact |
| QF-066–067 | LOCKED | LOCKED | exact |
| QF-068 | LOCKED STRUCTURE | same | specificity recovered |
| QF-069 | CALIBRATED STRUCTURE | same | specificity recovered |
| QF-070 | LOCKED STRUCTURE | same | specificity recovered |
| QF-071 | LOCKED | LOCKED | exact |
| QF-072 | LOCKED STRUCTURE | same | specificity recovered |
| QF-073–074 | LOCKED | LOCKED | exact |
| QF-075 | LOCKED OPTIMIZATION PROBLEM | same | specificity recovered |
| QF-076 | LOCKED DEFINITION | same | specificity recovered |
| QF-077 | LOCKED ALGORITHM | same | specificity recovered |
| QF-078 | LOCKED OPTIMIZATION PROBLEM | same | specificity recovered |
| QF-079–080 | LOCKED | LOCKED | exact |
| QF-081 | LEARNED | LEARNED | exact |
| QF-082 | LOCKED | LOCKED | exact |
| QF-083 | LEARNED | LEARNED | exact |
| QF-084 | LOCKED DECOMPOSITION | same | specificity recovered |
| QF-085–090 | LOCKED | LOCKED | exact |
| QF-091 | CALIBRATED SAFETY FACTOR | same | specificity recovered |
| QF-092–098 | LOCKED | LOCKED | exact |
| QF-099 | no formal bold status line in its section | SOURCE_DERIVED_FROM_CONTEXT; fixed calibration definition | former LOCKED was unjustifiably source-explicit |
| QF-100 | LOCKED | LOCKED | exact |
| QF-101 | LOCKED DEFINITION | same | specificity recovered |
| QF-102 | LOCKED FEATURE | same | specificity recovered |
| QF-103 | MODEL DEPENDENT | MODEL DEPENDENT | material mismatch: former index said LOCKED |
| QF-104 | PAS DE FAUX SCORE PONDÉRÉ FIGÉ | source-explicit gated categorical contract | material mismatch: former index said LOCKED |
| QF-105 | CALIBRATED | CALIBRATED | exact |
| QF-106–110 | no formal bold status line in these sections | SOURCE_DERIVED_FROM_CONTEXT; fixed definitions | former LOCKED was unjustifiably source-explicit |

## QF-099 resolution

`SOURCE_DERIVED_FROM_CONTEXT`. Exact evidence: SRC-004 lines 8487–8559 state the bucket equation and calibration interpretation but contain no formal status label. SRC-004's post-book closure treats calibration metrics as mathematically fixed/codable and requires versioned registry/golden tests for fixed formulas. Therefore the equation is retained as a locked definition while the provenance classification remains explicitly context-derived. No claim of `SOURCE_EXPLICIT` is made.

## Counts

- 110 statuses audited.
- 34 former-index rows lost source specificity, had absent-label provenance, or materially disagreed (excluding QF-001's rendering-only prefix).
- 2 material class/contract mismatches: QF-103 and QF-104.
- 6 absent formal source status lines: QF-099 and QF-106–110.
- 0 unresolved status ownership; all absences are recorded as context-derived rather than silently source-explicit.
