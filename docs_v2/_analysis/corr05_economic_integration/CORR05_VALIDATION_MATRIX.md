# CORR-05 Validation Matrix

| ID | Required evidence | Pass condition |
|---|---|---|
| `EC-01` | E0–E9 label goldens | every axis distinct; UNKNOWN outside failure |
| `EC-02` | F/P/R/X partition fixtures | exclusive/exhaustive only for declared resolved profile |
| `EC-03` | conditioning lint | every probability declares event, population and scope |
| `EC-04` | product scan | no blind QF-048/QF-085 × `p_full` |
| `EC-05` | scenario EV goldens | probability and path cashflow each represented once |
| `EC-06` | Recovery fixtures | entry, success and QF-080 loss remain separate |
| `EC-07` | inventory/stranded goldens | QF-068/QF-105 not repeated beside QF-069 |
| `EC-08` | Bridge fixtures | QF-070–072 and action bucket stay separate from Strategy |
| `EC-09` | q/state support grid | no small-q extrapolation; no monotonicity assumption |
| `EC-10` | QF-027/QF-076 cases | profitable size and validated capacity diverge correctly |
| `EC-11` | infra profile comparison | coherent outcome delta and incremental cost once |
| `EC-12` | accounting reconciliation | each fill/cost maps to one action bucket and one total |
| `EC-13` | prediction/actual mode tests | Shadow/Replay never create realized PnL |
| `EC-14` | Risk boundary | positive RAEV never overrides a hard gate |
| `EC-15` | demotion/OOD | fallback contracts capacity or disables authority |
| `EC-16` | formula namespace scan | QF identifiers remain QF-001–110; HDF=0; QF equation changes=0 |

Thresholds and statistical support remain calibrated and require human review where material. This matrix specifies future validation; it does not assert runtime implementation.
