# CORR-03 — Validation Matrix

DOCUMENTATION STATUS: REQUIRED EVIDENCE — IMPLEMENTATION NOT AUTHORIZED

| Area | Required tests/evidence | Failure response |
|---|---|---|
| label derivation | tiny ordered-event goldens for complete, zero, partial→Recovery, UNKNOWN→no-fill/fill→complete, negative-PnL complete | invalidate labels |
| censoring/finality | pending/censored/invalid/cutoff/revision fixtures; no `UNKNOWN=0` | exclude from binary fit, report |
| join | exact ID/version join, missing/inferred/duplicate conflicts and join rate | calibration invalid |
| no-lookahead | feature availability/receive-time proof, frozen forecast equality, episode-aware chronological split | model invalid |
| HJ suite | HJ-001..010 state/inventory/reservation/Risk/Recovery/Reconciliation/trace expectations | no capability promotion |
| dedupe | duplicate/late/out-of-order fills; reducer idempotence; no double fee/PnL | reconcile/stop |
| rates | denominator-zero, raw counts, resolved vs operational populations | unavailable, not zero |
| fallback/OOD | sparse/new route/market/q/latency/infra/mode | conservative fallback/no influence |
| calibration | QF-095/096 golden fixture, reliability/support/slices and temporal OOS | recalibrate/demote |
| baseline comparison | constant vs empirical vs Challenger, stability/economic lift | retain simple Champion |
| drift | completion, partial, UNKNOWN, Recovery, latency, support/calibration | scoped demotion/revalidation |
| artifact | immutable manifest/hash/schema/model promotion/rollback | reject artifact |
| runtime | P50–P99.9, CPU/allocation and end-to-end capture/economic impact | no decision-path use |
| Shadow/Micro-live | Shadow observe-only; real small-capital exact labels; q/mode separation | evidence scope capped |

Golden examples assert: UNKNOWN then resolved no-fill gives `Y_full_route=0` and sticky UNKNOWN; UNKNOWN then fills and original route completes gives 1; Recovery reaching `RECOVERED` gives Recovery success but route 0; completed negative PnL gives route 1 and economic positive 0.
