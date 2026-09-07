# Formula Legacy Comparison

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

Compared only after the SRC-004 source-first reconstruction. Legacy file: `docs/04_FORMULA_BOOK.md`; it was not edited.

| QF | Legacy classification | Audit note |
|---|---|---|
| QF-001 | EXACT | equation and units compatible |
| QF-002 | EXACT | — |
| QF-003 | EXACT | — |
| QF-004 | EXACT | notation differs only |
| QF-005 | EXACT | — |
| QF-006 | SUBSTANTIALLY_CORRECT | calibrated bands captured |
| QF-007 | SUBSTANTIALLY_CORRECT | lot form equivalent but source decimal form restored |
| QF-008 | EXTERNAL_RULE_STALE | accurately flagged external; current fact unverified |
| QF-009 | FORMULA_MISMATCH | legacy makes insufficient depth intrinsic invalid; source walk returns filled amount |
| QF-010 | MISSING_FAILURE_RULE | partial/residual behavior omitted |
| QF-011 | MISSING_FAILURE_RULE | zero-fill undefined not stated in row |
| QF-012 | EXACT | — |
| QF-013 | EXACT | — |
| QF-014 | SUBSTANTIALLY_CORRECT | dynamic source semantics present |
| QF-015 | SUBSTANTIALLY_CORRECT | distinction present |
| QF-016 | SUBSTANTIALLY_CORRECT | architecture correct; full failure surface compressed |
| QF-017 | EXACT | — |
| QF-018 | EXACT | — |
| QF-019 | MISSING_PRECONDITION | direct denominator positivity implicit |
| QF-020 | EXACT | — |
| QF-021 | SUBSTANTIALLY_CORRECT | nested NC equivalent |
| QF-022 | MISSING_PRECONDITION | positive input/closure implicit |
| QF-023 | EXACT | — |
| QF-024 | SUBSTANTIALLY_CORRECT | wording compressed |
| QF-025 | EXACT | — |
| QF-026 | EXACT | discontinuity captured |
| QF-027 | MISSING_FAILURE_RULE | empty feasible set absent |
| QF-028 | EXACT | denominator condition present |
| QF-029 | SUBSTANTIALLY_CORRECT | mixed weight status captured |
| QF-030 | EXACT | equality branches preserved |
| QF-031 | EXACT | equality branches preserved |
| QF-032 | EXACT | — |
| QF-033 | EXACT | mixed status present |
| QF-034 | EXACT | — |
| QF-035 | EXACT | — |
| QF-036 | FORMULA_MISMATCH | legacy hard-codes Mid; source requires explicit P reference and only generally defaults R&D to Mid |
| QF-037 | MISSING_PRECONDITION | sampling/window validity omitted |
| QF-038 | MISSING_PRECONDITION | no implicit annualization omitted |
| QF-039 | SUBSTANTIALLY_CORRECT | epsilon/threshold provenance compressed |
| QF-040 | SUBSTANTIALLY_CORRECT | zero-depth safety captured |
| QF-041 | MISSING_FAILURE_RULE | zero-volume behavior absent |
| QF-042 | EXACT | both side signs correct |
| QF-043 | MISSING_FAILURE_RULE | D0=Ds absent; raw/clamp correct |
| QF-044 | SUBSTANTIALLY_CORRECT | target/object status compressed |
| QF-045 | EXACT | — |
| QF-046 | FORMULA_MISMATCH | legacy uses `j<k`; source uses `j=1..k` |
| QF-047 | MISSING_FAILURE_RULE | no-crossing censor result omitted |
| QF-048 | SUBSTANTIALLY_CORRECT | discrete expression compressed |
| QF-049 | EXACT | no exponential assumption stated |
| QF-050 | MISSING_PRECONDITION | threshold unit/provenance omitted |
| QF-051 | EXACT | — |
| QF-052 | EXACT | — |
| QF-053 | MISSING_PRECONDITION | tail/truncation/censor label omitted |
| QF-054 | EXACT | sign correct |
| QF-055 | EXACT | sign correct |
| QF-056 | MISSING_PRECONDITION | exclusivity/exhaustiveness not in row |
| QF-057 | SUBSTANTIALLY_CORRECT | exact structure present |
| QF-058 | SUBSTANTIALLY_CORRECT | learned components/cost ownership compressed |
| QF-059 | MISSING_PRECONDITION | N>0 absent; strict > present |
| QF-060 | EXACT | sign semantics present |
| QF-061 | MISSING_PRECONDITION | alpha/sample estimator absent |
| QF-062 | OVER_COMPRESSED | robust integral and empirical ties not explicit |
| QF-063 | EXACT | double-counting warning present |
| QF-064 | MISSING_FAILURE_RULE | B_a=0 absent |
| QF-065 | SUBSTANTIALLY_CORRECT | soft-band role present |
| QF-066 | SUBSTANTIALLY_CORRECT | gate semantics correct |
| QF-067 | MISSING_PRECONDITION | ordered actual event requirement absent |
| QF-068 | SUBSTANTIALLY_CORRECT | executable NC exit captured |
| QF-069 | EXACT | components separated |
| QF-070 | EXACT | — |
| QF-071 | EXACT | nonpositive denominator handled |
| QF-072 | SUBSTANTIALLY_CORRECT | threshold/hysteresis captured |
| QF-073 | EXACT | nonnegative invariant present |
| QF-074 | MISSING_FAILURE_RULE | negative/stale capacity behavior absent |
| QF-075 | SUBSTANTIALLY_CORRECT | gate list present |
| QF-076 | MISSING_FAILURE_RULE | empty set/evidence tuple absent |
| QF-077 | MISSING_PRECONDITION | deterministic tie/config absent |
| QF-078 | SUBSTANTIALLY_CORRECT | typed resource/unit detail absent |
| QF-079 | EXACT | actual-current-state objective and equivalent loss retained |
| QF-080 | EXACT | sunk cost exclusion retained |
| QF-081 | SUBSTANTIALLY_CORRECT | learned distribution present |
| QF-082 | EXACT | interpretation preserved |
| QF-083 | SUBSTANTIALLY_CORRECT | global-before-cause note present |
| QF-084 | SUBSTANTIALLY_CORRECT | stage equations present; instrumentation boundaries omitted |
| QF-085 | EXACT | — |
| QF-086 | MISSING_PRECONDITION | like-for-like note present but full scope compressed |
| QF-087 | MISSING_PRECONDITION | horizon/scope alignment implicit |
| QF-088 | EXACT | — |
| QF-089 | EXACT | denominator handling present |
| QF-090 | SUBSTANTIALLY_CORRECT | double-count warning present |
| QF-091 | SUBSTANTIALLY_CORRECT | calibration/open estimator compressed |
| QF-092 | MISSING_FAILURE_RULE | zero/negative InfraCost absent |
| QF-093 | MISSING_FAILURE_RULE | zero denominator absent; ratio-of-sums correct |
| QF-094 | MISSING_PRECONDITION | censoring noted; exact estimator/empty cohort absent |
| QF-095 | MISSING_PRECONDITION | aligned p/y, bounds and N>0 absent |
| QF-096 | MISSING_PRECONDITION | epsilon range/status and N>0 absent |
| QF-097 | EXACT | sign convention present |
| QF-098 | EXACT | sign convention present |
| QF-099 | STATUS_MISMATCH | legacy review is cautious; canonical resolution now context-derived |
| QF-100 | SUBSTANTIALLY_CORRECT | comparable scope present |
| QF-101 | SUBSTANTIALLY_CORRECT | OOS promotion present; attribution detail compressed |
| QF-102 | MISSING_PRECONDITION | M>0/aligned outputs absent |
| QF-103 | STATUS_MISMATCH | legacy `M` approximates but does not preserve exact MODEL DEPENDENT label |
| QF-104 | STATUS_MISMATCH | gated semantics correct; exact source prohibition/status not preserved |
| QF-105 | SUBSTANTIALLY_CORRECT | empirical rate meaning present |
| QF-106 | STATUS_MISMATCH | equation correct; source has no formal status line |
| QF-107 | STATUS_MISMATCH | equation correct; source has no formal status line |
| QF-108 | STATUS_MISMATCH | equation correct; source has no formal status line |
| QF-109 | STATUS_MISMATCH | equation correct; source has no formal status line and zero-peak failure absent |
| QF-110 | STATUS_MISMATCH | equation correct; source has no formal status line and empty interval absent |

Legacy mismatches recovered: `3 FORMULA_MISMATCH`, `8 STATUS_MISMATCH`, `28 MISSING_PRECONDITION/MISSING_FAILURE_RULE`, plus compressed or externally stale rows. The legacy book remains comparison material only.
