# F2 Precision and HDC Traceability

`DOCUMENTATION STATUS: PROPOSED F2 REVIEW EVIDENCE — AWAITING HUMAN REVIEW`

Authority level: L3 post-source requirement disposition. The `PREC-P*` namespace is a design-
requirement namespace and cannot collide with research `HYP-*` identities. Existing Formula,
Data, Execution, Risk, Accounting and Validation documents remain canonical.

## 1. Provenance boundary

`PREC-P01..PREC-P19` come from a user-supplied complementary design document dated 19 October
2026, which historically referenced `main @ 8994edcc5264b1a6bd0652b7a4724488ccaac53b`.
That reference is preserved as provenance; it is not an SRC-001..008 identity, current external-
fact proof or the F2 baseline. Current exchange facts remain subject to dated primary-source
revalidation.

## 1A. Original precision IDs and source-text reconciliation (proposed F2 delta)

The original document is **`Hyperliquid_Fiche_precisions_conception_v1.md`**, version 1.0,
dated **2026-10-19** (206 rendered text lines in the accessible source). Its source labels are
`HYP-P01` through `HYP-P19`; the F2 ledger deliberately uses `PREC-P01` through
`PREC-P19` to distinguish design precisions from research `HYP-*` hypotheses. The mapping
is exactly ordinal: **`HYP-PNN` (source) = `PREC-PNN` (F2) for NN=01..19**. These
are aliases for traceability, not 38 requirements or a new executable ID family.

A content-by-content source-versus-F2 comparison confirms the 19 corresponding requirement
subjects and retains the following qualifiers that must remain visible to all consumers:

- **P03/P04:** scenario outcomes must be exclusive and probabilities sum to one; realized
  charges are never double counted with L2 consumption, modeled adverse selection,
  Recovery, or a second RAEV uncertainty adjustment.
- **P05:** the initial entry gate is different from the later Risk-governed defensive exit;
  the latter can rationally realize a loss to contain exposure.
- **P06/P07:** an indirect conversion with no comparable direct reference is **not**
  an OWA advantage. A maker result must not be compared to an ex-post selected taker
  quote; the decision-time comparator, deadline and budget are frozen.
- **P08/P09:** conversion savings are a comparative metric and may not be added again
  to portfolio profit; residual-asset valuation and executable liquidation value differ;
  starting-asset gain does not imply profit in every reporting currency.
- **P10/P14:** conditional-on-fill and all-attempt maker outcomes are different
  populations; opportunity cost is an estimate, not an actual fee. **Maker and taker
  viability are independently evidenced**, including when the corresponding taker
  variant is not profitable. TT-first in the technical roadmap defines the staged
  *operational activation order*, not a requirement that TT be economically profitable
  before maker research may be evaluated or MT/MTT may later be authorized.
- **P11/P12/P13:** fill quantity must come from unique actual fills; late/partial fills
  after cancel requests preserve exposure/reservations; `expiresAfter` must not be
  interpreted as a guaranteed cancellation of a resting order.
- **P15/P17/P18/P19:** sampled L2 snapshots do not reveal every intervening order
  event or the exact queue position. `OFI_snapshot` remains a proxy. Own actual order
  and fill evidence is required for maker calibration. Distinguish change-triggered
  channel silence from a verified outage; do not retroactively upgrade historical data
  fidelity.

The source's October 2026 descriptions of `l2Book` frequency/depth, ALO/IOC,
`expiresAfter`, account fees and rate limits remain dated external claims requiring
fresh official-source verification before implementation. This documentary comparison is
**not** that external revalidation.

**Result:** 19/19 original requirements matched one-to-one to the F2 dispositions,
with the above cross-cutting qualifiers explicitly carried forward. No historical HDC
or QF/SI/ESM contract is changed; all material new implementation/profitability
claims remain unvalidated and permissions remain `NOT_AUTHORIZED`.

## 2. Complete PREC disposition matrix

| PREC ID | Purpose | Canonical owner | Existing contract | New requirement / disposition | Test evidence | Review status |
|---|---|---|---|---|---|---|
| `PREC-P01` | full executable L2 economics per leg and q | Formula + Book/Graph | QF-001..027; QF-016 `NetConvert`; full-L2 acceptance | strengthen cross-link only; no new equation | L2 walk, partial-depth, multi-leg and full/fast parity goldens | covered / pending F2 review |
| `PREC-P02` | effective versioned fees, modifiers, rebates and debit assets | Fee/Data + Formula | QF-014..018; point-in-time fee/rule versions; actual fee reconciliation | require explicit version/debit-asset provenance; changing facts revalidate | historical-version, tier/modifier/rebate, unknown-fee fail-closed and actual-fee joins | covered / external freshness gated |
| `PREC-P03` | no economic double counting | Formula + Accounting | QF-056..063, QF-105..110; HDC-051..069 exact-once rules | strengthen ownership matrix; no parallel EV | duplicate fee/Recovery/inventory/infra/priority cost fixtures and QF-106 close | covered / pending F2 review |
| `PREC-P04` | quantity curves, uncertainty and non-monotonic q support | Sizing + Validation | QF-027, QF-075..077; SI-022; `ValidatedQSet` | require region/curve uncertainty and exact-q evidence; no interval inference | holes/non-monotonicity, sensitivity, support/OOD and exact-q gate tests | covered / pending F2 review |
| `PREC-P05` | net admission, uncertainty and tail-risk restrictions | Risk + Formula/Simulator | QF-056..063; constitutional Risk gates; one `Π_exec` | scientific output cannot weaken hard gates or hide tails | tail scenario, uncertainty, invalid support, negative EV and Risk precedence fixtures | covered / pending F2 review |
| `PREC-P06` | explicit Conversion, OWA, Triangle, Bridge and Rebalance intents | Graph/Opportunity + Capital/Accounting | four-axis route taxonomy; SI-019..021 | strengthen typed intent and attribution cross-links | classification and forbidden-conflation fixtures | covered / pending F2 review |
| `PREC-P07` | fair decision-time comparator | Opportunity + Formula | QF-019/QF-020; SI-019; matched input/terminal/conventions | no new formula; require point-in-time comparator lineage | direct-vs-route matched-q, side-asset valuation and missing-comparator tests | covered / pending F2 review |
| `PREC-P08` | separate reconcilable route, Recovery, Inventory, Bridge and Rebalance economics | Accounting + Inventory/Capital | QF-105..110; SI-021; QF-106 global close | strengthen attributable buckets and join lineage | action-bucket reconciliation, Bridge-present QF-106 and no-reclassification tests | covered / pending F2 review |
| `PREC-P09` | intermediate exposure, residual assets and conservative liquidation | Inventory/Capital + Risk/Recovery | actual asset-delta vector; Terminal Viability; SI-011..013 | require explicit residual/exposure duration/value in evidence | partial-leg, dust/residual, adverse exit, terminal inventory and Recovery fixtures | covered / pending F2 review |
| `PREC-P10` | conditional-on-fill and all-attempt maker evidence | Participants/Simulator + Validation | distinct fill labels, censoring and attempt populations | require both views; conditional evidence cannot impersonate all-attempt value | zero/partial/full/right-censored cohorts, selection-bias and denominator tests | covered / pending F2 review |
| `PREC-P11` | maker waiting reassessment and Risk/ESM ownership | Execution + Risk | ordered ESM, current-state Risk, cancel/expiry semantics | strengthen timed reassessment evidence without new state owner | book/risk change while resting, expiry, cancel and continuation/Recovery tests | covered / pending F2 review |
| `PREC-P12` | actual fill quantities and exact-once updates | Execution/FillLedger + Inventory | SI-010/SI-011; unique actual fills only | exact reuse; no research or Simulator label authority | duplicate/out-of-order/partial fill, fee and inventory reconciliation tests | covered / pending F2 review |
| `PREC-P13` | cancel races, UNKNOWN reservations and timer distinctions | Execution + Reservations/Reconciliation | SI-007..009; no blind retry; ordered timer/effect events | strengthen explicit timer/cancel evidence | cancel-requested-late-fill, UNKNOWN restart, timeout/query and reservation-lock fixtures | covered / pending F2 review |
| `PREC-P14` | economically independent maker/taker validation; TT/TTT before MT/MTT only in staged operational activation | Validation + Roadmaps | Phases 20/23; Evidence Stages 12–15; HPD-01 MT/MTT only | maker may be viable where taker is not; mode-specific evidence/authorization; no automatic scope transfer | independent mode-specific Replay/Shadow/Micro-live, Recovery and promotion records | covered / pending F2 review |
| `PREC-P15` | feed capability and historical subscription metadata | Data/Adapters/Recorder | point-in-time source profile, immutable RAW, RunManifest and EXT gates | require historical subscription/capability identity in datasets | schema/subscription/version, reconnect/gap and source-profile replay tests | covered / external freshness gated |
| `PREC-P16` | no invented depth beyond observed support | Book + Formula/Simulator | valid BookState, QF L2 walk, F0–F4 fidelity boundaries | strengthen explicit unsupported-depth outcome | truncated book, insufficient depth, extrapolation rejection and Simulator support tests | covered / pending F2 review |
| `PREC-P17` | snapshot-derived OFI identified honestly | Microstructure/Data | QF-030..033 proxy boundary and feature provenance | require method/version label such as snapshot-derived OFI; no event-level claim | snapshot cadence, gap, offline parity, leakage and alternate-method comparison | covered / pending F2 review |
| `PREC-P18` | maker queue uncertainty and calibration | Simulator + Participants/Validation | F2 queue fidelity; maker labels; support/OOD | strengthen uncertainty/censoring requirements; no exact queue truth claim | calibration/coverage, temporal OOS, queue-proxy support and pessimistic fallback | covered / pending F2 review |
| `PREC-P19` | immutable RAW, point-in-time Replay, gaps and no lookahead | Recorder/Replay + Data | SI-016/SI-017; deterministic Replay; immutable RAW | exact reuse plus explicit precision cross-link | checksum, gap invalidation, point-in-time artifact and repeated-hash Replay tests | covered / pending F2 review |

Aggregate result: `19/19 COVERED`; `0` new QF equations; `0` new runtime modules mandated; `0`
Formula/Risk/ESM semantic overrides; `0` current-external-fact assertions. Coverage means routed for
review, not approved, implemented or validated.

## 3. F2 HDC allocation

Historical `HDC-001..094` remain byte-for-byte historical records. F2 adds six aggregate material
requirements rather than one HDC per precision:

| HDC | Human provenance | Requirement family | Relationship | Canonical owner | F2 destinations | Status |
|---|---|---|---|---|---|---|
| `HDC-095` | F2 Prompt 1, 2026-11-01; commits `46ecd4f…` / `3cce15a…` | Economic Falsifier T0/T1/T2 and finite pre-registered Bounded Sweep | new validation method over existing authorities | Validation; Formula/Data/Replay/Simulator remain truth owners | Validation specs 13/14, Masters 00/16, Roadmaps, F2 crosswalk | pending human review; no permission |
| `HDC-096` | F2 Prompt 1, 2026-11-01 | robustness region, temporal order, T2-before-holdout and one-time untouched holdout | validation strengthening | Validation + Data evidence lineage | Validation 14, atlas temporal map, non-regression audit | pending human review; no permission |
| `HDC-097` | F2 Prompt 2 correction, 2026-11-01; commit `9940899…` | first fixed OWA/TT DRAFT candidate may precede the full Factory gate | semantic dependency correction | Validation/Roadmaps; Strategy Research owns lineage only | Strategy 03, Master, scope, roadmaps, review package | pending human review; no automatic transition |
| `HDC-098` | F2 Prompt 2, 2026-11-01; commit `197a3a9…` | deterministic Registry/Manager/local-worker boundaries and optional deferred distributed/Dragonfly orchestration | new research orchestration contract | Data/RunManifest for facts; Research for orchestration | Strategy 09/11, scope register, atlas, crosswalk | pending human review; no trading authority |
| `HDC-099` | F2 Prompt 2, 2026-11-01 | Structure Discovery is a Future proposal requiring human Architecture Review | architecture-change boundary | Master Architecture + human architecture governance | Strategy 12, scope register, atlas | pending human review; no Core mutation |
| `HDC-100` | complementary user design document dated 2026-10-19; historical reference `main @ 8994edc…` | `PREC-P01..P19` precise economics, intent, maker/execution and data-fidelity requirements | mostly strengthening/cross-linking; no 19 equations/modules | existing Formula/Accounting/Execution/Data/Validation owners | this matrix plus canonical/review cross-links | pending human review; external facts revalidate |

These HDCs are user requirements, not six new human-policy families. They introduce no competing
policy choice requiring a new HPD at this point. Any later product/architecture selection remains
classified by the existing Phase-14 decision tree.

## 4. Exact inventory impact

- historical HDC ledger: `HDC-001..094`, preserved;
- F2 overlay: `HDC-095..100`, proposed and pending review;
- aggregate proposed HDC inventory: 100 sequential IDs with no gap;
- sorted LF-terminated HDC ID-list SHA-256:
  `8ec95ddaf6be694de77f9ef6fe84f142e96db58f8f1fa11d77a4f8b6a5254014`;
- active human-policy families: unchanged at two (`HPD-01`, `HPD-02`), because the new entries are
  requirements, evidence rules or deferred boundaries rather than open competing policy choices.

No HDC record authorizes implementation, research runtime, Shadow, Micro-live, Live, switchover,
capital or a change to Formula/Risk/ESM truth.
