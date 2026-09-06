# Formula Cross-Domain Gap Register

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

PASS11 recorded discrepancies without silently rewriting PASS01–10 masters. The `Proposed PASS14 resolution` column below is the historical handoff; PASS14 has now completed its cross-domain review, with final dispositions appended after the original register.

| Gap ID | QF | Domain doc | Current statement | Canonical Formula Book statement | Severity | Implementation risk | Proposed PASS14 resolution | Source |
|---|---|---|---|---|---|---|---|---|
| GAP-F11-01 | 007–008 | 05 Microstructure / 11 Data | delegates units/rules to PASS11/external metadata | floor equation and source price rule now exact | high | divergent legal orders | link exact formula/numeric contract after external validation | SRC-004 3793–3847 |
| GAP-F11-02 | 009–010,016 | 03 Graph / 05 Microstructure | full-fill invalidity stated but source walk itself yields filled amount | walk returns fill/residual; full-fill consumer separately rejects | high | partial result lost or extrapolated | distinguish pure walk result from route gate | SRC-004 3848–4325 |
| GAP-F11-03 | 014–016 | 03/05/10/11/Accounting consumers | fee rate/value broadly correct; actual debit asset delegated | economic value and asset delta must remain separate | critical | double charge/reconciliation error | add FeeEngine schema once external semantics validated | SRC-004 4121–4325 |
| GAP-F11-04 | 029 | 05 Microstructure / Participants | calibrated weights noted, index said plain LOCKED | headline LOCKED plus calibrated weights | medium | hard-coded weights | propagate mixed status | SRC-004 4860–4925 |
| GAP-F11-05 | 036 | 05 Microstructure | correctly requires explicit price series | source says reference explicit; R&D default generally Mid | low | hidden reference drift | ensure schema requires reference ID | SRC-004 5233–5262 |
| GAP-F11-06 | 039 | 05 Microstructure / Risk | threshold delegated; epsilon not fully typed | epsilon positive numerical safeguard; threshold calibrated | medium | divide-zero/different score | version epsilon and threshold separately | SRC-004 5299–5363 |
| GAP-F11-07 | 041 | 05 Microstructure / Execution | declares provenance but no zero-volume result | source provides no zero-denominator rule | high | Inf/zero silently reaches gate | validate typed invalid/reject policy | SRC-004 5410–5446 |
| GAP-F11-08 | 043 | 05 Microstructure / Participants | raw/clamp behavior correct; no D0=Ds rule | denominator-zero source omission | medium | NaN/Inf resilience | validate typed invalid policy | SRC-004 5516–5583 |
| GAP-F11-09 | 046 | legacy/index consumers | legacy uses `j<k` | exact source product is `j=1..k` | high | one-bin survival shift | replace legacy-derived tests/references with source index | SRC-004 5675–5693 |
| GAP-F11-10 | 053 | Execution/Participants | expected fill time named; censor/tail estimator delegated | integral is fixed; conditional/truncated result must be labelled | medium | biased maker timing | select versioned tail convention | SRC-004 5926–5971 |
| GAP-F11-11 | 057 | Execution/Simulator | scenario contract broadly F/P/R/failure | exact exhaustiveness/overlap evidence not schema-closed | high | EV mass double count | formalize scenario enum/mass invariant | SRC-004 6082–6149 |
| GAP-F11-12 | 061–062 | Risk/Validation | VaR/ES required without empirical interpolation/tie algorithm | distribution formula fixed; finite-sample method open | high | Rust/Python risk gate drift | validate one empirical quantile/ES convention | SRC-004 6314–6391 |
| GAP-F11-13 | 064 | Inventory/Risk | normalized deviation assumed | source omits B_a=0 behavior | medium | division by zero | validate band positivity and migration behavior | SRC-004 6492–6517 |
| GAP-F11-14 | 077 | Inventory/Sizing | grid/refinement architecture fixed | exact grid, refinement and ties remain config/open | medium | nondeterministic q* | specify deterministic search config | SRC-004 7314–7342 |
| GAP-F11-15 | 078 | Portfolio | objective/constraints fixed | exact solver/tie/failure policy open | medium | different allocations | select solver evidence contract, not library prematurely | SRC-004 7343–7380 |
| GAP-F11-16 | 084 | Infrastructure/Ops | stage families present | exact nonoverlapping timing boundaries need instrumentation contract | high | latency double counting | publish boundary diagram/fixtures | SRC-004 7660–7765 |
| GAP-F11-17 | 091 | Infrastructure/Validation | LCB/alpha/SF calibrated/open | strict inequality fixed; estimator/value choices open | high | unsafe infra promotion | validate estimator and parameter evidence | SRC-004 8036–8076 |
| GAP-F11-18 | 092 | Infrastructure/Ops | diagnostic ratio stated | zero/negative InfraCost source behavior omitted | low | invalid dashboard number | typed N/A policy | SRC-004 8077–8123 |
| GAP-F11-19 | 093 | Infrastructure/Ops | ratio-of-sums stated | zero/nonpositive expected denominator not closed by source | medium | misleading capture ratio | typed N/A and cohort contract | SRC-004 8124–8227 |
| GAP-F11-20 | 094 | Participants/Validation/Ops | censoring required generally | exact survival estimator/cohort eligibility open | medium | biased KPI/calibration | validate estimator and eligibility schema | SRC-004 8228–8274 |
| GAP-F11-21 | 096 | Participants/Validation | probability clipping required | exact epsilon status/value not fixed | medium | parity/log instability | version numerical epsilon with vectors | SRC-004 8309–8360 |
| GAP-F11-22 | 099 | Maker/Validation/index | former index says LOCKED; legacy says review | no formal source status; fixed equation context-derived | medium | false provenance/status | propagate context-derived classification | SRC-004 8487–8559 |
| GAP-F11-23 | 103 | Participants/Risk/index | broad OOD contract correct; index said LOCKED | exact source status MODEL DEPENDENT | high | universal estimator invented | propagate model-dependent status/artifact binding | SRC-004 8751–8781 |
| GAP-F11-24 | 104 | Simulator/Risk/Validation/index | gated confidence broadly correct; index said LOCKED | source prohibits fixed weighted score | high | unsafe aggregate confidence | preserve categorical gate truth table | SRC-004 8782–8832 |
| GAP-F11-25 | 106–108 | Accounting/Inventory/Ops | components described but source status omitted | fixed identities are context-derived; disjoint reconciliation mandatory | high | global PnL double count | publish attribution mapping/reconciliation vectors | SRC-004 8891–9147 |
| GAP-F11-26 | 109 | Risk/Ops | drawdown tracked without zero-peak contract | relative DD needs Peak>0; source silent otherwise | medium | NaN dashboard/risk gate | validate typed N/A/absolute-only policy | SRC-004 9148–9204 |
| GAP-F11-27 | 110 | Risk/Validation | MDD required without empty interval rule | nonempty interval required; source silent empty | low | invalid baseline metric | validate minimum evidence interval | SRC-004 9205–9224 |

Cross-domain gaps found: `27`. None changes an older master in this pass. Critical/high gaps are fail-closed until future human resolution.

## PASS 14 final disposition

`OPEN` and `EXTERNAL GATED` mean the formula contract is internally consistent but the consuming capability must not guess the missing estimator or current fact.

| PASS11 gap | PASS14 disposition | Canonical gate / evidence |
|---|---|---|
| `GAP-F11-01` | EXTERNAL GATED | QF-007/008 exact contract + `EXT-004` before exchange-bound encoding |
| `GAP-F11-02` | RESOLVED / VERIFIED | pure QF-009/010 walk output remains distinct from full-route acceptance (`P14-008`) |
| `GAP-F11-03` | EXTERNAL GATED | typed fee value/debit boundary + `EXT-003` (`P14-009`) |
| `GAP-F11-04` | RESOLVED / VERIFIED | locked structure and calibrated weights remain separate |
| `GAP-F11-05` | RESOLVED / VERIFIED | price-series reference is explicit and versioned |
| `GAP-F11-06` | RESOLVED / VERIFIED | positive numerical safeguard and calibrated threshold remain separate versioned parameters |
| `GAP-F11-07` | OPEN | `OPEN-017`; typed invalid/fail-closed until approved |
| `GAP-F11-08` | OPEN | `OPEN-018`; typed invalid/fail-closed until approved |
| `GAP-F11-09` | RESOLVED / VERIFIED | QF-046 exact `j=1..k`; no canonical regression |
| `GAP-F11-10` | OPEN | `OPEN-021`; tail/censoring convention must be versioned |
| `GAP-F11-11` | RESOLVED / VERIFIED | exclusive/exhaustive scenario mass and confidence evidence are explicit |
| `GAP-F11-12` | OPEN | `OPEN-019`; empirical VaR/ES estimator and vectors required |
| `GAP-F11-13` | OPEN | `OPEN-020`; invalid band behavior requires approval |
| `GAP-F11-14` | OPEN | `OPEN-022`; deterministic search/refinement/tie policy required |
| `GAP-F11-15` | OPEN | `OPEN-022`; deterministic solver/tie/failure policy required |
| `GAP-F11-16` | RESOLVED / VERIFIED | latency boundaries are nonoverlapping and instrumentation-owned |
| `GAP-F11-17` | OPEN | `OPEN-005`/`OPEN-023`; LCB estimator/alpha/safety factor require evidence |
| `GAP-F11-18` | OPEN | `OPEN-024`; diagnostic is typed N/A for invalid denominator until approved |
| `GAP-F11-19` | OPEN | `OPEN-024`; denominator/cohort contract requires approval |
| `GAP-F11-20` | OPEN | `OPEN-025`; survival estimator/cohort eligibility requires evidence |
| `GAP-F11-21` | OPEN | `OPEN-026`; clipping epsilon must be versioned and tested |
| `GAP-F11-22` | RESOLVED / VERIFIED | QF-099 status provenance remains source-derived from context |
| `GAP-F11-23` | RESOLVED / VERIFIED | QF-103 remains model-dependent and artifact-bound |
| `GAP-F11-24` | RESOLVED / VERIFIED | QF-104 remains a categorical gate, never an invented scalar score |
| `GAP-F11-25` | RESOLVED | Accounting authority/attribution boundary made explicit (`P14-004`) |
| `GAP-F11-26` | OPEN | `OPEN-027`; zero-peak behavior requires approved typed policy |
| `GAP-F11-27` | OPEN | `OPEN-028`; nonempty evidence interval required |

PASS11 gaps reviewed by PASS14: **27/27**. Resolvable cross-domain inconsistencies remaining: **0**. Unresolved QF misuse: **0**. Open estimator/invalid-case choices and current exchange facts remain scoped gates, not silent defaults.
