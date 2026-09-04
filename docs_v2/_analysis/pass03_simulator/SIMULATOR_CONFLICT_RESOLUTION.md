# PASS 03 — Simulator Conflict Resolution

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

| Conflict | Earlier implication | Later/closure evidence | Canonical PASS 03 resolution | Status |
|---|---|---|---|---|
| CONFLICT-010 — exact alternate world | Historical replay + our order could be read as what exactly would have happened | SRC-008 explains future incompatibility/unobservable reactions | Simulator returns calibrated plausible distributions; exact-alternate claim `SUPERSEDED / REJECTED`. | RESOLVED |
| CONFLICT-017 — historical continuation | Apply every later trade/cancel to a modified book | SRC-008 negative-depth example; SRC-005 modes/rejoin | Detect compatibility; Exogenous keeps external future with limitation; Interactive branches/reconciles/rejoins explicitly. | RESOLVED |
| CONFLICT-018 — single/multi-market Shadow | One route-level mutation could imply all triangle books change | SRC-008 triangle correction and multi-market Shadow State | Mechanical mutation is local; other markets change only through their own events or calibrated Cross-Market Response. | RESOLVED |
| CONFLICT-019 — single future | One expected/point PnL as advanced decision output | SRC-008 scenarios/CVaR; SRC-004 QF-056–063; SRC-006 distribution DoD | Mutually exclusive outcome distribution plus tails/confidence required. | RESOLVED |
| CONFLICT-020 — complex-first response | Giant Hawkes/agents could appear more realistic | SRC-008 conditional empirical first; PASS 02 governance | Conditional Empirical Champion direction; Queue-Reactive/Hawkes/agents Challengers/Research. | RESOLVED |
| CONFLICT-021 — exact L2 queue | Aggregate L2 reduction interpreted as exact queue advancement | SRC-008 L2/L4 distinction and three queue modes | L2 queue uncertainty is explicit; Pessimistic/Optimistic/Probabilistic envelope. | RESOLVED |
| CONFLICT-022 — fixed rejoin | A universal time horizon could simplify branch management | SRC-008 variable horizon/non-rejoin; SRC-005 explicit rejoin event | Rejoin is explicit and impact/support dependent; exact rule calibrated; non-rejoin is valid. | RESOLVED |
| CONFLICT-023 — backtest authority | Strong Replay EV could outweigh poor real fills | SRC-005 Risk “Backtest Cannot Override Live Evidence” and calibration kill switch | Persistent supported live contradiction wins; reduce/disable/fallback through Risk. | RESOLVED |

## Non-conflicts retained as separate dimensions

- `ExogenousReplay` and `InteractiveCounterfactual` are complementary modes, not competing truths.
- F0–F4 describes fidelity; M0–M5 describes evidence; P0–P5 describes Participant capability; `RunMode` describes environment.
- A supported F1 can carry higher `SimulationConfidence` than an uncalibrated F3/F4.
- Deterministic mechanics and stochastic response coexist by layering; deterministic replay comes first.
- L2 support at launch and L4-compatible architecture coexist; current L4 availability remains external.

## Residual calibrated decisions, not conflicts

Exact rejoin thresholds/horizons, empirical response estimator, queue probabilities, dependence model, confidence gate thresholds, simulation path count, size grid/refinement, and production fidelity activation require data/evidence. They remain calibrated/learned and are not silently closed here.

No unresolved source contradiction blocks the PASS 03 specification.
