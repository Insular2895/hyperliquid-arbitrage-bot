# 09 — Reporting, Experiment Registry and Knowledge Base

`DOCUMENTATION STATUS: F2 PART 2 / INTERMEDIATE DOCUMENTARY WORK / AWAITING HUMAN REVIEW`

`CAPABILITY STATUS: DOCUMENT FORMAT SPECIFIED / GENERATOR AND DASHBOARD NOT IMPLEMENTED`

The knowledge base is durable evidence, not a results scrapbook. It strengthens the existing
[Research Knowledge Base](../../research/README.md); it does not replace it or create competing
runtime identities.

## 1. Identity and immutability

Canonical runtime identities remain `DatasetId`, `RunId`, `IncidentId` and `EvidenceId`. Display
forms `DATASET-*`, `RUN-*` and `INC-*` are reversible serializations or registry links, not duplicate
IDs. Documentary families remain `HYP-*`, `EXP-*`, `BENCH-*`, `STRAT-*`, `ADR-*`, `POST-*`,
`REL-*`; external facts use the existing `EXT-*` register. `HDC-*` records post-reconstruction
human requirements and is not replaced by ADR.

IDs are never reused. Machine facts and immutable artifact hashes are append-only. A correction
creates a superseding version or amendment with reason and lineage; it never overwrites the prior
record. `StrategyFamily`, Configuration and job/attempt keys are fields/links, not new canonical ID
namespaces.

Every planned or attempted run remains visible, including failed jobs, invalid points, aborted
evaluations, censored/unresolved cases, negative economics, exact duplicates, manual reruns,
predeclared early-stop leftovers and results invalidated by later data-quality findings. A later
invalidation appends validity evidence; it does not delete the original observation.

## 2. Registry contract

An experiment registry entry links:

| Family | Required contract |
|---|---|
| scientific identity | `HYP-*`; Structure; StrategyFamily; optional `STRAT-*` version; `EXP-*` version; owner/reviewer |
| frozen protocol | protocol/config-space hash; parameter domains; locked values; budget; splits; selection/region rules; multiplicity; T2; final-holdout policy |
| data and build | `DatasetId`/hash/split; Git commit; build/image; schema; point-in-time support |
| canonical dependencies | Formula, Fee, Metadata, Book, Graph, Replay, Simulator, feature and model versions |
| exact evaluation | Configuration/value serialization/hash; RunMode; ReplayMode; fidelity; `FALSIFIER_T*`; scenarios; RNG seed/stream |
| compute lineage | deterministic ordinal; job/attempt state; host/environment; retry/manual-rerun/duplicate reason; timestamps |
| scientific validity | valid/invalid/unsupported/aborted/failed/censored/negative status; reason; missingness; clock/data quality |
| economic/path evidence | canonical net results and cost owners; zero/partial/full/Recovery; exposure/time/tails; actual vs replay/simulated provenance |
| validation | OOS/window/fold; walk-forward; region membership/maturity; T2; final holdout access/result |
| interpretation | claim classes; human/AI producer; uncertainty; limitations; no mutation of machine facts |
| governance | supersession; incidents; ADR/decision/release links; status and explicit non-authorization |
| artifacts | immutable URI/reference, media/schema, content hash, producer/version and `EvidenceId` packaging |

The exact serialized schema and storage technology are `HUMAN_DECISION_REQUIRED`. These fields are
the semantic M0 contract; they do not add ad hoc fields to the frozen canonical `RunManifest`.

### D6 — Experiment Registry and evidence lineage

```text
HYP-* ----> EXP-* frozen protocol ----> deterministic Configurations
  |                 |                              |
  |                 +--> DatasetId/splits          +--> job attempts
  |                 +--> versions/builds                    |
  |                 +--> budget/selection/T2                v
  |                                                  canonical RunId
  |                                                         |
  |                          +------------------------------+------------------+
  |                          |              |               |                  |
  |                       valid          invalid         failed/censored     duplicate
  |                          +--------------+---------------+------------------+
  |                                                         |
  +---------------------> immutable complete run population-+
                                                            |
                                                            v
          RobustnessRegion / OOS / T2 / holdout ----> EvidenceId package
                                                            |
                              +-----------------------------+------------------+
                              |                                                |
                              v                                                v
                   STRAT-* version lineage                         ADR/decision/release
                              |
                              v
                    read-only Analytics/Dashboard
```

Read left-to-right: the frozen experiment binds inputs and configurations; every compute/scientific
outcome enters one immutable population; evidence packages can inform Strategy and decisions
without changing the source facts.

Contract — **Inputs:** canonical IDs, frozen protocol, versions/configurations and run/attempt
outputs. **Operations:** validate, hash, append, supersede/link and deterministically aggregate.
**Outputs:** complete queryable lineage, `EvidenceId` packages and report projections. **Canonical
authority:** Data/RunManifest and domain owners for facts; Registry for durable indexing only.
**Failure/uncertainty:** missing joins, invalid hashes, failed/negative/censored/duplicate runs and
later invalidations remain explicit; no deletion or favorable imputation. **Activation timing:**
document/index structures now; generator/storage/runtime only after authorization and applicable
research gates.

## 3. Reports and machine/interpretation boundary

Every report has separate machine facts and interpretation. A future deterministic generator owns
manifest fields, hashes, counts, metrics and links. Human or AI content can annotate, classify or
propose but cannot overwrite them. Amendments append or supersede with lineage.

An experiment report contains identity/version/status; hypothesis/falsifier; owner/reviewer; dates;
scope; Dataset/Run manifests; code/config/formula/model/strategy versions; split and leakage policy;
method/search/seed/budget; primary/guardrail metrics; results/uncertainty; failures/censoring/
missingness; sensitivity/OOS/stress; comparison; selection trace; claim classification;
limitations; conclusion; non-authorizing disposition; linked incidents/ADRs/releases; and immutable
artifacts/hashes.

The intended navigation is bidirectional: `StrategySpec -> Experiment -> Run/Evidence ->
Incident/Postmortem -> ADR/promotion decision -> Release`, with hypotheses and datasets reachable
from every relevant node. Reports remain readable Markdown and future-tool parseable through
stable front matter/tables. Empty indexes continue to say `ZERO RECORDED ARTIFACTS`; no fake
experiment, run, winner or maturity is created.

## 4. Future human-facing Analytics and Dashboard

Analytics and Dashboard are read-only projections over registry snapshots. They never write
machine facts, define scientific truth, issue a `RiskDecision`, grant permission, change q/capital,
promote a Strategy or send an order. Every aggregate drills down to exact `RunId`, Dataset,
Configuration, versions, scenario assumptions, errors and evidence.

Required conceptual views:

- **Overview:** Structures, Strategy Families, active hypotheses, experiments, runs,
  valid/invalid/censored counts, Discovery regions, independent-Validation survivors, adversarial
  survivors and final-holdout survivors.
- **Robustness:** q × threshold heatmaps, supported regions vs isolated optima, neighborhood
  stability, boundaries, exact q holes, temporal/regime stability, worst supported periods,
  uncertainty, missingness and coverage.
- **Economics/execution:** canonical net economics, exact-once fees/costs, slippage, zero/partial/
  full completion, Recovery, tails, capital/time exposure, maker all-attempt vs conditional-on-fill
  populations when maker is eligible, and actual vs predicted evidence where actual truth exists.
- **Lifecycle:** hypothesis/experiment history, DRAFT/candidate/validated-evidence distinctions,
  StrategyVersions, supersession, drift, demotion, human decisions and retirement/rejection reason.
- **Drill-down:** exact facts/assumptions/provenance and immutable artifacts behind every cell.

No invented composite such as “97% reliable” is allowed. A health/confidence label must expose the
contributing dimensions, support, uncertainty, missing evidence and rule/version.

### D7 — Robustness Map to Analytics to Dashboard

```text
immutable Run population
          |
          v
Discovery Map -> independent Validation -> T2 -> final holdout
          |                 |              |          |
          +-----------------+--------------+----------+
                            |
                            v
              versioned Analytics projection
        counts / surfaces / economics / lifecycle
                            |
             +--------------+--------------+
             |                             |
             v                             v
      human Dashboard                 machine report
      read-only filters              deterministic facts
             |                             |
             +--------------+--------------+
                            |
                            v
       drill-down to RunId / Dataset / config / versions

No arrow returns to Registry facts, Strategy status, Risk or Live.
```

Read top-to-bottom: immutable evidence creates versioned projections; dashboard and report are two
views of the same snapshot; drill-down preserves provenance and there is no write-back path.

Contract — **Inputs:** accepted and explicitly invalid/failed registry populations plus region/
validation lineage. **Operations:** deterministic aggregation, coverage/uncertainty computation and
read-only filtering. **Outputs:** human views and machine reports with full drill-down. **Canonical
authority:** Registry/domain facts remain authoritative; Analytics only presents. **Failure/
uncertainty:** stale snapshot, missing join, insufficient support or invalid population is shown,
never hidden or scored optimistically. **Activation timing:** conceptual only; implementation is
deferred and `HUMAN_DECISION_REQUIRED`.

## 5. PREC-P01 through PREC-P19 — research lifecycle implications

This table consumes, and does not duplicate or change, the Prompt-1 owners/mapping in
[Validation 14](../validation/14_ROBUST_REGION_AND_CANDIDATE_LIFECYCLE.md).

| ID | Research/registry implication |
|---|---|
| `PREC-P01` | bind full executable L2 support and exact leg/q evidence; midpoint/BBO-only whole-route claims remain invalid |
| `PREC-P02` | version fee rules by account/market/role/time, modifiers/rebates/debit asset; preserve historical comparability and dated external-fact links |
| `PREC-P03` | store one explicit cost-owner map and exclusive scenario population so no fee/slippage/penalty is double counted |
| `PREC-P04` | retain exact evaluated q membership, uncertainty and holes; no region/search result raises `Q_validated` |
| `PREC-P05` | separate new-route admission evidence from defensive loss-taking; research never replaces Risk |
| `PREC-P06` | freeze structure/class/mode/intent; conversion benefit is not absolute profit and Bridge/Rebalance remain distinct |
| `PREC-P07` | bind matched OWA comparator information, deadline and Risk scope; separate route-selection benefit from execution effects |
| `PREC-P08` | retain attributable exact-once accounting buckets and reconciliation links; no research accounting authority |
| `PREC-P09` | report exposure duration/limits/residuals and executable liquidation separately from accounting valuation |
| `PREC-P10` | when maker is eligible, retain all-attempt and conditional-on-fill populations, wait/cancel/Recovery/opportunity cost |
| `PREC-P11` | maker evidence links every remaining-leg economics/Risk reassessment; no research-created cancel/continue policy |
| `PREC-P12` | distinguish actual reconciled fills from simulated fills and propagate only actual simulated available quantized output inside scenarios |
| `PREC-P13` | retain cancel race, resting/action expiry and UNKNOWN/censored outcomes; current external behavior remains revalidated |
| `PREC-P14` | preserve TT -> TTT -> separately gated MT/MTT; maker or optimistic queue evidence cannot bypass capability gates |
| `PREC-P15` | bind feed capability/subscription/depth/aggregation/clocks/order/gaps/reconnect and documented-vs-measured provenance |
| `PREC-P16` | unsupported/invisible depth is invalid or a smaller predeclared candidate, never favorable extrapolation |
| `PREC-P17` | version/label OFI snapshot or equivalent fidelity honestly; no exact event-level claim from snapshot proxies |
| `PREC-P18` | maker T2 records queue uncertainty and rejects touched-price/reduced-size-as-fill inference; actual calibration remains separately gated |
| `PREC-P19` | preserve immutable RAW, `recorder_seq`, clocks/gaps and point-in-time lineage; later quality knowledge never repairs old evidence retroactively |

External fee/feed/API changes create new `EXT-*`/version boundaries and drift/revalidation triggers.
The registry keeps both historical assumptions and later facts; it does not silently restate old
runs under new rules. All 19 mappings remain subordinate to their original Formula/Data/Execution/
Risk owners.

## 6. Human decisions

Final registry serialization, storage, artifact retention/backup, deterministic generator,
dashboard technology, access control, snapshot freshness and any health-label vocabulary are
`HUMAN_DECISION_REQUIRED`. Safe default: immutable Markdown/manifests and hashes, zero fabricated
rows, no dashboard write path and `UNAVAILABLE` when evidence/support is missing.
