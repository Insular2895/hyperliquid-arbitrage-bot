# F2 Non-Regression Audit

`DOCUMENTATION STATUS: PROPOSED F2 AUDIT EVIDENCE — AWAITING HUMAN REVIEW`

Authority level: L3 audit report. Results describe documentation checks only; they do not prove
runtime behavior, profitability, safety implementation or authorization.

## 1. Frozen inventory checks

| Inventory | Computed result | Identifier-list SHA-256 | Disposition |
|---|---:|---|---|
| Formula contracts in `04_FORMULA_BOOK.md` | 110 unique, contiguous `QF-001..QF-110` | `a2e271b27da3d550647c58bb6e3f9c125b304ac2461dce4f054f79d9de424110` | unchanged; no equation added/edited |
| Applicable review invariants | 29 unique, contiguous `SI-001..SI-029` | `02fd8b6450535dd81cece48fec313c46b7210585ecd4ad9f7859497f2806b60d` | unchanged; count computed, not assumed |
| Historical post-source HDCs | 94 unique, contiguous `HDC-001..HDC-094` | historical ledger preserved | unchanged historical set |
| Proposed F2 HDC overlay / aggregate | 6 new; 100 total contiguous `HDC-001..HDC-100` | `8ec95ddaf6be694de77f9ef6fe84f142e96db58f8f1fa11d77a4f8b6a5254014` | pending review; no new HPD inferred |
| Technical phases | 26, exact `1..26` | ordinal inventory | unchanged; no Phase 27 |
| Evidence stages | 21, exact `1..21` | ordinal inventory | unchanged; no Stage 22 |
| Maturity levels | six, `M0..M5` | semantic inventory | unchanged; no scientific-status alias |

Identifier hashes are SHA-256 over sorted unique IDs with one ID per LF-terminated line. They are
diagnostics for this F2 preparation, not replacements for exact Git/tree identity.

## 2. Safety non-regression review

| Required invariant family | Canonical anchor | F2 result |
|---|---|---|
| exchange truth over local/research assumption | SI-002/003/010/014; Data/Execution masters | preserved; Falsifier/workers cannot create truth |
| `ActualFill > ExpectedFill`; partial fill is exposure | SI-010/011; ESM/Inventory | preserved |
| existing exposure/safety before opportunity | SI-001/012–015 | preserved |
| no blind retry; `CancelRequested != Canceled`; UNKNOWN locks | SI-006–009 | preserved |
| one canonical economic state writer | SI-027; ordered Core | preserved; worker/coordinator completion has no commit authority |
| immutable RAW, no lookahead, deterministic Replay | SI-016/017; Recorder/Replay | preserved |
| no imaginary liquidity or unsupported depth | Book/Formula validity; PREC-P16 disposition | strengthened by cross-link only |
| fair OWA comparator; Bridge distinct from OWA/Rebalance | SI-019–021 | preserved |
| fee/execution/Recovery/Inventory costs exactly once | QF-056..063, QF-105..110; HDC-051..069 | preserved; no QF change |
| no automatic q/capital expansion | SI-022; QF-076 boundary | preserved; simulated q remains non-authorizing |
| no model/AI/Factory promotion or Live self-learning | CD-021; HDC-087..089 | preserved |
| no research-controlled order transmission | Risk/ESM/authorization boundary | preserved |
| no automatic resume from unresolved state | SI-014/025/028 | preserved |
| no production hot-path research-worker/Dragonfly dependency | async C0–C5 + Strategy Research 11 | explicit in F2 scope/crosswalk/maps |

## 3. Scientific-order checks

- PASS: a negative T0 cell rejects only that declared cell/scope; it does not reject OWA globally.
- PASS: data-dependent T0 and the finite Sweep require a frozen protocol.
- PASS: the Sweep is finite, predeclared and distinct from generalized Parameter Search.
- PASS: full T1 waits for Replay/Simulator/ESM/Inventory/Reservation/Risk/Recovery dependencies.
- PASS: T2 acts on a frozen candidate after supported T1 and before the final untouched holdout.
- PASS: the final holdout is evaluated once per locked decision family and is not optimized.
- PASS: `ROBUST_CANDIDATE` remains diagnostic and is not Shadow permission.
- PASS: the first OWA/TT DRAFT/validation path can precede the Factory without bypassing any gate.
- PASS: the full validated-baseline gate still blocks Factory, generalized search, advanced
  discovery, automated Champion/Challenger, later Monte Carlo programs and distributed research.

## 4. Authority and scope checks

- Formula/Risk/ESM/Accounting/Data ownership is unchanged.
- Falsifier validates a fixed claim; Simulator supplies supported scenarios; Factory proposes later
  candidates; Manager/workers orchestrate computation; Registry indexes; Dashboard presents;
  humans decide only their named reviews/authorizations.
- The Bounded Sweep is a Foundation validation method. Generalized Parameter Search is Research.
- Local workers are optional implementation choices. Distributed workers and DragonflyDB are
  deferred Research infrastructure. Structure Discovery is Future.
- MT/MTT and Bridge remain Later V1. Cross-exchange, perp hedge and TM/MM remain Future.
- `PREC-P01..P19` are fully routed without 19 new equations/modules or current-fact claims.

## 5. Candidate and traceability result

Historical L0/L1 source identities and PASS00/PASS15/Phase-18 boundaries are preserved. Prompt-1,
Prompt-2 and Prompt-3 are L3 semantic/documentary overlays. Because F2 changes canonical routing,
scope, HDC inventory and the active review package without executing a new exact-snapshot Phase-18
delta certification, current status is:

`DELTA_RECERTIFICATION_REQUIRED`

This does **not** block mechanical F2 review-package completeness when the final diff, links,
inventories and Git identity checks pass. It **does** block any claim that F2 is already fully
delta-certified, source-certified at its new exact snapshot, approved, switchover-authorized or
implementation-authorized.

## 6. Conflict result

No blocking Formula/Risk/ESM conflict was found. The prior initial-baseline/Factory circularity is
resolved by separating the first fixed OWA/TT validation path from later generalized research.
No new independent human-policy family was identified. Any later selection of distributed
technology, thresholds, estimator details or architecture change remains evidence-,
implementation- or human-review-scoped under existing governance.

## 7. Executed mechanical checks

- `git diff --check`: PASS.
- Markdown relative-link scan: 948 Markdown files, 883 relative links, 0 broken targets.
- Changed tracked-file scope: 39 files, all under `docs_v2/`; six new F2 artifacts, also under
  `docs_v2/`; no `docs/`, source-code, Cargo, Docker or runtime file changed.
- Required F2 artifacts: 6/6 present and inbound-linked.
- PREC matrix: 19/19 unique IDs. Architecture atlas: 5/5 maps and 5/5 required-field tables.
- Exact inventories: 110 QF, 29 SI, 100 HDC, 26 technical phases, 21 evidence stages, six M-levels.
- Historical HDC-001..094 row SHA-256 before/after:
  `782443928fbbbbacf4c0d91e3da20a345ee64f2505fd97efe159df55259e7908` / identical.

Mechanical result: `PASS`. Human confirmation remains pending. Delta source recertification,
documentation approval and every later authorization remain separate and unperformed.
