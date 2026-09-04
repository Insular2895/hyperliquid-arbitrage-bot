# Contradiction Register

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Conflict ID | Concept | Source A / statement | Source B / statement | Chronology / authority | Proposed resolution | Confidence | Domain review |
|---|---|---|---|---|---|---|---|
| CONFLICT-001 | Live language | Earlier Python-first/live exploration | Later Rust production core | Later explicit correction; architecture direction | Rust core; Python research; old live-Python direction SUPERSEDED | HIGH | YES |
| CONFLICT-002 | Node at launch | Earlier node-focused architecture/specs | SRC-008 + SRC-006 public feed first | Later refinement + deployment authority | Node-compatible, not node-required | HIGH | YES |
| CONFLICT-003 | Production storage size | SRC-001/003 comfortable 250GB–1TB examples | SRC-008 40–100GB light baseline | Later infrastructure correction | Light baseline; size calibrated from recorder working set | HIGH | YES |
| CONFLICT-004 | Fixed latency thresholds | Earlier 35ms/120–150ms/500µs examples | SRC-004/005 calibrated distributions/no magic numbers | Closure authority | Preserve mechanism; numerical examples not invariants | HIGH | YES |
| CONFLICT-005 | Formula variants | Pre-closure formulas in SRC-002/003/007/008 | SRC-004 QF-001..110 | Formula closure authority | QF form wins; earlier variants SUPERSEDED/context only | HIGH | PASS 11 |
| CONFLICT-006 | Market orders | Early/general market execution language | Protected IOC/FOK/no blind market orders | Later correction + execution closure | Protected limit IOC/FOK as permitted; blind market rejected | HIGH | PASS 04 |
| CONFLICT-007 | OWA identity | Indirect paths sometimes called arbitrage without comparator | Later direct A→B comparator requirement | Later refinement | No comparator = Bridge/relocation, not OWA | HIGH | PASS 08 |
| CONFLICT-008 | Capital-driven infrastructure | Earlier profile language tied performance to capital | SRC-008 says capital alone is not trigger | Later explicit correction | Upgrade from recoverable PnL/ROI, not capital alone | HIGH | PASS 01 |
| CONFLICT-009 | Recorder implementation | Earlier Python Recorder suggestions | Later Rust non-blocking Recorder | Later correction | Rust event capture; Python offline processing | HIGH | PASS 06 |
| CONFLICT-010 | Exact alternate-world replay | Naive historical modification could imply exactness | SRC-008 calibrated plausible distributions | Advanced simulator correction | Never claim exact alternate universe | HIGH | PASS 03 |

## PASS 01 — Infrastructure review

| Conflict ID | PASS 01 result | Residual item | Canonical evidence |
|---|---|---|---|
| CONFLICT-002 | `RESOLVED` — public feed first; node-compatible, not node-required | Node activation remains `OPEN-006` | `13_INFRASTRUCTURE.md`; deep spec 06 |
| CONFLICT-003 | `RESOLVED` — small VPS working disk and large R&D/archive storage are separate roles | Exact capacities remain `OPEN-011` | master; deep specs 01/03/07 |
| CONFLICT-004 | `RESOLVED` — mechanisms locked; historical numerical examples are calibrated hypotheses | Exact health thresholds/windows remain `OPEN-004` | master; deep specs 03/04/07 |
| CONFLICT-008 | `RESOLVED` — limitation/InfraLostPnL/ROI, never capital alone, drives transitions | LCB method/parameters remain `OPEN-005` | master; deep spec 05; QF-084–QF-093 |

The complete source comparison and retained history are in `pass01_infrastructure/INFRA_CONFLICT_RESOLUTION.md`.

## PASS 02 — Market Participants review

| Conflict ID | Concept | Source evolution | Canonical resolution | Confidence | Domain review |
|---|---|---|---|---|---|
| CONFLICT-011 | Synthetic agents as market truth | Agent-world research possibility versus SRC-007/008 explicit aggregate-first correction | Production predicts collective effects; explicit agents are P5 stress/scenario research | HIGH | `RESOLVED` PASS 02 |
| CONFLICT-012 | Address as identity | Pseudonymous trade counterparties could be read as participant identity | Address/cluster is behaviour evidence only, never proven person/firm/strategy; P4 optional | HIGH | `RESOLVED` PASS 02 |
| CONFLICT-013 | Dense cross-market matrix | Conceptual cross-market matrix versus explicit rejection of `N×N×horizons` live modelling | Sparse graph neighbourhood only; neighbours/horizons learned and validated | HIGH | `RESOLVED` PASS 02 |
| CONFLICT-014 | Complex model first | Queue-Reactive/Hawkes/GBDT/deep models available versus simple empirical Champion | Simple empirical survival first; advanced models shadow Challengers until full promotion evidence | HIGH | `RESOLVED` PASS 02 |
| CONFLICT-015 | Heavy simulation in Participant hot path | Stochastic response research could imply per-tick simulation | Small bounded inference in Participant; Monte Carlo/agents remain Simulator/research | HIGH | `RESOLVED` PASS 02 |
| CONFLICT-016 | Random/live-adaptive learning | Random row splits or live self-updating weights versus temporal scientific governance | Temporal/walk-forward OOS; offline train/validate/promote; no uncontrolled live self-learning | HIGH | `RESOLVED` PASS 02 |

Full evaluation and non-conflicts are in `pass02_participants/PARTICIPANT_CONFLICT_RESOLUTION.md`.

## PASS 03 — Counterfactual Simulator review

| Conflict ID | Concept | Source evolution | Canonical resolution | Confidence | Domain review |
|---|---|---|---|---|---|
| CONFLICT-010 | Exact alternate-world replay | Naive modified historical continuation versus SRC-008 epistemic correction | Only calibrated plausible distributions; exact alternate-world claim rejected | HIGH | `RESOLVED` PASS 03 |
| CONFLICT-017 | Historical event continuation | Blind future trades/cancels versus incompatibility after `Δour` | Explicit compatibility policy; Exogenous limitation or Interactive branch/rejoin | HIGH | `RESOLVED` PASS 03 |
| CONFLICT-018 | Triangle book mutation | Route-level intuition versus local mechanical causality | Only traded book mutates mechanically; other books use historical events/response | HIGH | `RESOLVED` PASS 03 |
| CONFLICT-019 | Deterministic future/PnL | Point forecast versus scenarios/tail distributions | Full/partial/recovery/failure distribution plus VaR/CVaR/confidence | HIGH | `RESOLVED` PASS 03 |
| CONFLICT-020 | Complex model first | Hawkes/agents sophistication versus empirical baseline | Conditional Empirical Champion direction; advanced models Challenger/Research | HIGH | `RESOLVED` PASS 03 |
| CONFLICT-021 | Exact maker queue from L2 | Aggregate level changes versus unknown cancellation position | Three explicit Pessimistic/Optimistic/Probabilistic L2 modes | HIGH | `RESOLVED` PASS 03 |
| CONFLICT-022 | Fixed rejoin horizon | Universal time versus impact-dependent decay/support | Calibrated variable horizon, explicit event, valid non-rejoin | HIGH | `RESOLVED` PASS 03 |
| CONFLICT-023 | Replay versus live evidence | Strong backtest versus poor persistent actual fills | Live evidence wins; Risk may reduce/disable via calibration kill switch | HIGH | `RESOLVED` PASS 03 |

Full reasoning is in `pass03_simulator/SIMULATOR_CONFLICT_RESOLUTION.md`. No unresolved Simulator contradiction blocks documentation reconstruction.

## PASS 04 — Execution State Machine review

| Conflict ID | Concept | Source evolution | Canonical resolution | Confidence | Domain review |
|---|---|---|---|---|---|
| CONFLICT-024 | Partial fill branch | Happy-path/atomic shorthand versus closure | Partial is normal; actual exposure is applied immediately | HIGH | `RESOLVED` PASS 04 |
| CONFLICT-025 | Planned downstream quantity | Precomputed plan versus actual fills | Every later leg uses actual fills, fees and rounding after current revalidation | HIGH | `RESOLVED` PASS 04 |
| CONFLICT-026 | Retry after timeout | Generic transport retry versus closure | Stable CLOID, query/reconcile, NO BLIND RETRY | HIGH | `RESOLVED` PASS 04 |
| CONFLICT-027 | Timeout semantics | Timeout as failure/no fill versus economic ambiguity | Possible transmission becomes `UNKNOWN`; reservations stay locked | HIGH | `RESOLVED` PASS 04 |
| CONFLICT-028 | Cancel finality | Cancel-send shorthand versus cancel race | `CANCEL_REQUESTED` is not `CANCELED`; racing fills remain real | HIGH | `RESOLVED` PASS 04 |
| CONFLICT-029 | Local versus exchange truth | Checkpoint/journal inference versus observed account | Orders/fills/balances and reconciliation outrank local assumption | HIGH | `RESOLVED` PASS 04 |
| CONFLICT-030 | Recovery destination | Finish original route versus current portfolio objective | QF-079 chooses best current permitted exit; original route has no privilege | HIGH | `RESOLVED` PASS 04 |
| CONFLICT-031 | Recovery cardinality | Single-exit examples versus split recovery | Multiple exits allowed under atomic reservations and Risk constraints | HIGH | `RESOLVED` PASS 04 |
| CONFLICT-032 | Restart readiness | Automatic restart/trade versus reconciliation-first | `BOOTING→SYNCING→RECONCILING`; only consistency permits `READY` | HIGH | `RESOLVED` PASS 04 |
| CONFLICT-033 | TM/MM activation | Representable execution modes versus implied availability | Supported by types, disabled and capital-unvalidated pending explicit approval | HIGH | `RESOLVED` PASS 04 |
| CONFLICT-034 | Journal hot-path I/O | Durability wording versus latency/single-writer requirement | Append-only asynchronous durability; reconciliation reconstructs exchange truth | HIGH | `RESOLVED` PASS 04 |
| CONFLICT-035 | Maker partial exposure | Planned maker completion versus observed partial | Every actual partial immediately updates inventory and continuation/recovery | HIGH | `RESOLVED` PASS 04 |

CONFLICT-006 (unbounded market language versus protected IOC/marketable limit) was also closed by PASS 04. No genuine earlier requirement mandating one giant enum was found; compressed legacy prose was not manufactured into a conflict. Full analysis: `pass04_execution/EXECUTION_CONFLICT_RESOLUTION.md`.
