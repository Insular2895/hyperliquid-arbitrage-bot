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
