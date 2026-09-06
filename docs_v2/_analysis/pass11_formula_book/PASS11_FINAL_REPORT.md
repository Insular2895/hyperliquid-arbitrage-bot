# PASS 11 — FORMULA BOOK AUDIT COMPLETE

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

QF formulas expected:
110

QF formulas audited:
110

Missing QF IDs:
0

Duplicate canonical QF IDs:
0

SRC-004 Formula Book fully reread:
YES — lines 3350–9520, including every QF section at 3519–9224 and post-book governance/golden material

Canonical expressions verified:
110/110

Statuses verified:
110/110

Status mismatches found:
34 former-index rows lost source specificity, asserted source-explicit status where the heading was absent, or materially disagreed; 2 were material contract classes (QF-103/QF-104)

QF-099 status resolution:
SOURCE_DERIVED_FROM_CONTEXT — fixed bucket calibration equation and interpretation are explicit at SRC-004 8487–8559, but no formal section status label exists

Symbols indexed:
76 semantic symbol families covering every equation symbol and index class

Unit/dimension checks completed:
110/110, grouped into 32 dimensional proof families

Dimensional source issues:
0 contradictions; source-omitted denominator/estimator cases are logged as open rather than guessed

Sign conventions verified:
110/110 through global and formula-local contracts

Precondition/failure rules:
110/110 have explicit fail-closed behavior; 12 source-omitted mathematical choices remain registered for human validation

Numeric/rounding rules:
Exact ticks/lots/fixed-point boundary, floor sizing, PriceQuantizer ownership, deterministic ordering, overflow/NaN/Inf policy and per-formula tolerance contract specified

External exchange rules:
6 formula rule families registered; 0 externally revalidated during PASS11 by mission rule

Formula dependencies:
110/110 mapped; no formula cycle

Consumer mappings:
110/110 mapped with primary owner, consumers, counts and output evidence

Double-counting risks found:
18

Double-counting issues resolved:
18 have first-entry ownership and forbidden-repeat rules; 5 require explicit inclusion/reconciliation evidence at implementation time, with no silent ownership remaining

Golden vector requirements:
17 vector families cover all 110 QFs, including normal, boundary and typed-invalid cases

Rust/Python parity requirements:
Same serialized vector/version tuple; exact discrete equality and formula-specific floating tolerances specified

Cross-domain gaps found:
27, registered without silently rewriting PASS01–10 masters

Conflicts found:
7

Conflicts resolved:
7 by SRC-004 authority and explicit provenance

Conflicts remaining:
0

Legacy formula mismatches:
3 formula mismatches, 8 status mismatches, 28 missing precondition/failure classifications; all 110 legacy rows classified

Open mathematical decisions:
12 (`OPEN-017`–`OPEN-028`): source-omitted denominator, empirical estimator, time-grid/tail, search/solver, clipping and drawdown-empty/zero conventions

Formula master created:
YES — `docs_v2/04_FORMULA_BOOK.md`, 39 required structural sections and one equation/contract row for every QF

Deep specs created:
13 files — README plus 12 required formula deep specs

Analysis files created:
17/17 required, including this report

Formula requirement ledger:
153/153 stable `REQ-FORMULA-*` rows covered by PASS11 overlay; IDs renumbered 0

Destinationless formula requirements:
0

Files modified outside docs_v2:
0 (`.DS_Store` remained pre-existing, untracked and unstaged)

External sources used:
0; local original SRC-004 and repository documentation only

PASS 12 started:
NO

NEXT: HUMAN REVIEW REQUIRED
