# Formula Precondition and Failure Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

The per-QF ledger and deep-spec rows are normative. This matrix groups identical failure controls without erasing formula identities.

| QF | Mandatory precondition | Boundary / invalid case | Required behavior |
|---|---|---|---|
| 001–003 | coherent positive BBO; Mid>0 for ratio | missing/crossed/nonpositive/zero denominator | typed invalid; no midpoint/zero substitute |
| 004–006 | ordered valid levels; K/band/side declared | missing/corrupt level, invalid δ | invalid or explicitly incomplete depth evidence |
| 007–008 | current precision metadata/rule | negative/nonfinite, stale/unknown metadata, illegal price | reject; never round up or generic-round |
| 009–010 | correct side, ordered book, positive prices, protection/minimum policy | zero input, partial/exhausted book, invalid level | explicit filled/spent/residual; full-fill consumer rejects residual |
| 011–013 | nonzero valid fill and positive side reference | zero fill/reference, wrong side | QF-011 undefined; slippage invalid |
| 014–016 | point-in-time fees/debit asset, precision, minimums, immutable state | stale tier, unknown debit, partial/minimum/quantization failure | typed invalid plus actual asset deltas; no approximate fallback |
| 017–025 | route continuity, same input/terminal/state/mode scope, positive ratio denominator | missing comparator, open triangle, invalid leg/zero denom | invalidate composite; preserve residual exposure |
| 026–027 | evaluated valid discrete sizes and aligned threshold | discontinuity, empty feasible set | retain invalid points; no interpolation/monotonicity; no size if empty |
| 028–035 | aligned BBO/events/levels/weights; positive denominators | both sizes zero, gaps/reorder, weight mismatch | invalid; snapshot OFI explicitly proxy |
| 036–039 | named positive price series, time order/window, ε>0 | nonpositive price, empty/gapped window, nonfinite scale | invalid; no hidden annualization/imputation |
| 040 | positive matching depth | depth=0 | reject; conceptual infinity not serialized |
| 041 | positive executed volume, declared window | volume=0 | typed invalid; exact policy remains open |
| 042 | valid side/walk/Mid0>0 | missing fill/zero reference | invalid |
| 043 | aligned depths/times and D0≠Ds | zero denominator | typed invalid; exact source behavior open; raw >1 valid |
| 044–046 | defined event/horizon/features/model; probabilities in [0,1] | OOD/missing artifact/invalid hazard | unavailable/invalid; do not clamp model error silently |
| 047 | valid survival curve/horizon | no 0.5 crossing | censored `t50>model_horizon` |
| 048–050 | aligned time/edge units and valid normalized distribution/model/threshold | missing mass, OOD, unit mismatch | invalid/low-confidence; no exponential substitute |
| 051–053 | defined fill event/order/model/tail convention | cancellation/censoring/truncated support | explicit censor/conditional label; unknown tail invalid |
| 054–055 | actual fill, positive price, explicit horizon/future mid | no fill/no matured future reference | unavailable until outcome matures |
| 056–058 | exclusive/exhaustive normalized scenarios; common numeraire; disjoint costs | overlap/missing mass/unit mismatch/double cost | invalidate EV |
| 059 | N>0 and common PnL definition | empty sample; PnL=0 | empty invalid; zero outcome not positive |
| 060 | finite labelled PnL | nonfinite/unlabelled | invalid |
| 061–062 | nonempty loss distribution, 0<α<1, versioned estimator | bad α/empty/ties/interpolation ambiguity | invalid until empirical convention is closed |
| 063 | aligned EV/penalties with ownership ledger | fee/slippage/recovery or penalty duplicated | invalidate RAEV; never silently correct |
| 064 | aligned asset quantities and B_a>0 | zero/negative band | typed invalid; normalization convention open |
| 065–066 | valid candidate post-inventory; κ≥0; ordered hard limits | invalid κ/unknown state/hard breach | invalid soft value; hard/unknown rejects new risk |
| 067 | ordered deduplicated reconciled trades/window | gap/duplicate/unreconciled event | invalid flow |
| 068–072 | point-in-time executable valuation, sequential NC, common horizon/numeraire, disjoint costs | unavailable exit, nonpositive cycle EV, incomparable alternatives | lock/no bridge; QF-071 conceptual infinity; STAY |
| 073–074 | reconciled matching actual/observed and reservations | negative available value/stale version | invariant violation and reject new allocation |
| 075–078 | valid discrete candidates, all gates, exact scope/shared constraints, deterministic tie | empty/infeasible/solver uncertainty | no action/no allocation; never extrapolate capacity |
| 079–080 | actual current exposure, legal actions, consistent before/after valuation | no safe action/missing value | contain/reconcile; never reset state or charge sunk loss |
| 081–083 | ordered market roles/shock/horizon/event/model/time unit | OOD/missing artifact/negative hazard/E0≤0 | unavailable/invalid; no unidentifiable cause claim |
| 084–085 | nonoverlapping stage boundaries, one clock/unit, valid survival/latency distribution | missing/double stage/time mismatch | attribution/capture invalid |
| 086–091 | same opportunity universe/strategy/capital/horizon/cost scope; ΔCost>0 for ROI; valid LCB | cohort mismatch, denominator≤0, missing uncertainty | invalidate comparison/ROI/gate; use net value where defined |
| 092–094 | positive denominator, aligned eligible cohort and censoring | zero/negative cost or expected PnL; empty cohort | typed invalid diagnostic/rate |
| 095–096 | aligned p/y, p∈[0,1], binary y, N>0, valid ε | empty/mismatched sample/log endpoint | invalid; clip only by versioned ε |
| 097–100 | matured aligned actual/predicted outcomes; comparable model/baseline | unit/event/horizon/cohort mismatch or empty bucket | unavailable/invalid |
| 101–104 | like-for-like OOS evidence, aligned ensemble/support, all six gates | duplicated cost, M=0, NaN/negative OOD, missing gate | invalidate value/score; confidence cannot be HIGH |
| 105 | C,T≥0 and calibrated empirical rate | negative/unvalidated/mismatched rate | invalid cost |
| 106–108 | same period/numeraire and disjoint reconciled components/flows | overlap, missing attribution, stale valuation | accounting invalid; reconciliation incident |
| 109 | nonempty ordered equity series; Peak>0 for relative | empty/reordered; Peak=0 relative | absolute may exist; relative typed invalid/open |
| 110 | nonempty valid drawdown interval | empty interval | typed invalid/open |

Operational rule: formula failure carries QF ID, FormulaVersion, input/state versions, reason code and consumer disposition. A failure cannot be converted to zero, NaN, infinity, stale value or permissive default.
