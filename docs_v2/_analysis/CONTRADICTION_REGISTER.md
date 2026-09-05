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

## PASS 05 — Risk Constitution review

| Conflict ID | Concept | Canonical resolution | Confidence | Domain review |
|---|---|---|---|---|
| CONFLICT-036 | Hard risk as EV penalty | A hard violation removes the action from `A_safe`; RAEV ranks only eligible actions | HIGH | `RESOLVED` PASS 05 |
| CONFLICT-037 | Semantic versus frozen RiskDecision fields | Dossier 4 frozen fields win; config/model/mode semantics link through RiskSnapshot/ExecutionPlan | HIGH | `RESOLVED` PASS 05 |
| CONFLICT-038 | Seven kill scopes versus narrow ControlEvent enum | Preserve constitutional scopes; exact asset/mode/model/infra event encoding is deferred to Data closure | HIGH | `RESOLVED` PASS 05, schema gap |
| CONFLICT-039 | Fail-open wording | Only strict reduction of a known exposure under RecoveryRiskPolicy; no generic fail-open | HIGH | `RESOLVED` PASS 05 |
| CONFLICT-040 | Capital/server price as risk permission | Scaling remains bounded by validated capacity and all gates; infrastructure economics cannot relax safety | HIGH | `RESOLVED` PASS 05 |
| CONFLICT-041 | PASS 00 keyword statuses inside SRC-005 | Fourteen false statuses corrected by full closure reading; source-prescriptive rules remain locked | HIGH | `RESOLVED` PASS 05 |

`CONFLICT-004`, `CONFLICT-005` and `CONFLICT-023` were crosschecked. Fixed numeric examples remain calibrated; Formula Book remains PASS 11 authority; persistent supported live evidence outranks backtest. Full reasoning: `pass05_risk/RISK_CONFLICT_RESOLUTION.md`. No unresolved constitutional conflict blocks the documentary reconstruction.

## PASS 06 — Data / Recorder / Replay review

| Conflict ID | Concept | Canonical resolution | Confidence | Domain review |
|---|---|---|---|---|
| CONFLICT-042 | Recorder P2/P3 | SRC-005 closure wins: P2 general market events; P3 derived diagnostics | HIGH | `RESOLVED` PASS 06 |
| CONFLICT-043 | Simplified Replay engine | Replay is the production Core with historical source/simulated transport | HIGH | `RESOLVED` PASS 06 |
| CONFLICT-044 | Exchange time as knowledge order | Receive chronology and recorder sequence own bot knowledge; exchange time remains research chronology | HIGH | `RESOLVED` PASS 06 |
| CONFLICT-045 | Checkpoint as truth | Compatible checkpoint + journal + exchange reconciliation; no silent READY | HIGH | `RESOLVED` PASS 06 |
| CONFLICT-046 | Storage priority as economic order | Recorder retention/backpressure priority never reorders Core dependencies | HIGH | `RESOLVED` PASS 06 |
| CONFLICT-047 | Parallel commit nondeterminism | One ordered coordinator commits version-checked worker results | HIGH | `RESOLVED` PASS 06 |
| CONFLICT-048 | Derived-only historical evidence | Immutable original RAW remains source evidence; normalized/derived are versioned derivatives | HIGH | `RESOLVED` PASS 06 |
| CONFLICT-049 | Later model in historical truth | Later artifacts require explicit `COUNTERFACTUAL_MODEL`; historical truth is point-in-time | HIGH | `RESOLVED` PASS 06 |

CONFLICT-009 (Recorder implementation) is closed: capture/Core implementation is Rust-compatible and non-blocking; Python remains offline normalization/research tooling, not the source capture hot path. Full analysis: `pass06_data_recorder_replay/DATA_CONFLICT_RESOLUTION.md`. No unresolved Data/Recorder/Replay documentary conflict remains.

## PASS 07 — Inventory / Capital / Bridge / Sizing review

| Conflict ID | Concept | Canonical resolution | Confidence | Domain review |
|---|---|---|---|---|
| CONFLICT-050 | Fixed inventory percentages | Ordered targets/bands are locked; values are calibrated evidence, not examples | HIGH | RESOLVED PASS07 |
| CONFLICT-051 | Universal holdability | `CORE_INVENTORY`, `TRANSIT`, `EXCLUDED` with versioned learned class | HIGH | RESOLVED PASS07 |
| CONFLICT-052 | Positive route equals valid terminal | Terminal Viability/exit/stranded/hard gates can reject | HIGH | RESOLVED PASS07 |
| CONFLICT-053 | OWA equals Bridge | OWA needs valid direct comparator; otherwise Bridge/relocation | HIGH | RESOLVED PASS07 |
| CONFLICT-054 | Fewest-hop relocation | Use economic path/NetConvert and QF-072 | HIGH | RESOLVED PASS07 |
| CONFLICT-055 | Bridge fees-only accounting | QF-070 plus expected exit and relocation risk; no duplicated costs | HIGH | RESOLVED PASS07 |
| CONFLICT-056 | Chase current best edge | Point-in-time future utility plus persistence/hysteresis | HIGH | RESOLVED PASS07 |
| CONFLICT-057 | Reallocate on each rank change | Calibrated hysteresis/cooldown prevents flip-flop | HIGH | RESOLVED PASS07 |
| CONFLICT-058 | Sizing equals Slicing | Exposure amount and child execution are separate owners/stages | HIGH | RESOLVED PASS07 |
| CONFLICT-059 | Profitable capacity equals validated capacity | QF-027 and QF-076 remain distinct | HIGH | RESOLVED PASS07 |
| CONFLICT-060 | Capital increase creates capacity | Q_validated changes only with validated evidence/state | HIGH | RESOLVED PASS07 |
| CONFLICT-061 | Route capacities independent | QF-073/074 reservations and QF-078 joint constraints | HIGH | RESOLVED PASS07 |
| CONFLICT-062 | Highest bps wins | Optimize joint absolute RAEV inside Risk/resource constraints | HIGH | RESOLVED PASS07 |
| CONFLICT-063 | Route-only PnL | Hierarchical attributable QF-105–108 accounting | HIGH | RESOLVED PASS07 |
| CONFLICT-064 | Losing Rebalance hidden as alpha | Separate Rebalance purpose and PnL | HIGH | RESOLVED PASS07 |
| CONFLICT-065 | Recovery equals ordinary capital move | Existing unwanted exposure uses QF-079/080 and constitutional priority | HIGH | RESOLVED PASS07 |

Full reasoning and PASS00 heuristic corrections: `pass07_inventory_capital/CONFLICT_RESOLUTION.md`. No unresolved documentary conflict remains; calibration and PASS08/PASS11 dependencies are not disguised as conflicts.

## PASS 08 — Market Graph / Routes / Atlas / Quant review

| Conflict ID | Concept | Canonical resolution | Confidence | Domain review |
|---|---|---|---|---|
| CONFLICT-066 | Undirected market edge | Two directed conversions with different sides/units | HIGH | RESOLVED PASS08 |
| CONFLICT-067 | Generic search per tick | Precomputed fixed 2/3-leg routes; general search offline/future | HIGH | RESOLVED PASS08 |
| CONFLICT-068 | Global route scan | `pair_to_routes` affected-route lookup | HIGH | RESOLVED PASS08 |
| CONFLICT-069 | Midpoint/fixed-fee edge | Exact L2 `NetConvert(q)` with versioned fee/metadata | HIGH | RESOLVED PASS08 |
| CONFLICT-070 | Every two-leg route is OWA | Valid direct A→B comparator required | HIGH | RESOLVED PASS08 |
| CONFLICT-071 | No-comparator OWA | Bridge/Capital Relocation candidate, PASS07-owned | HIGH | RESOLVED PASS08 |
| CONFLICT-072 | Graph equals Atlas/opportunity | Topology, rolling economics and transient condition remain distinct | HIGH | RESOLVED PASS08 |
| CONFLICT-073 | COLD means ignored | Global Watcher/Recorder preserve cheap awareness | HIGH | RESOLVED PASS08 |
| CONFLICT-074 | Capital/HOT changes topology | Capital changes reachability/activation only | HIGH | RESOLVED PASS08 |
| CONFLICT-075 | Conversion/execution alpha merged | QF-024 and QF-025 remain separate | HIGH | RESOLVED PASS08 |
| CONFLICT-076 | Current universe in historical Replay | point-in-time Graph/Route/Atlas/metadata versions | HIGH | RESOLVED PASS08 |
| CONFLICT-077 | Single-venue hardcoding | venue-aware identities; cross-exchange disabled V1 | HIGH | RESOLVED PASS08 |

Detailed source-evolution review: `pass08_graph_routes_quant/CONFLICT_RESOLUTION.md`. No unresolved PASS08 documentary conflict remains; calibration, external facts, PASS11 audit and future venue work remain explicitly open dependencies.

## PASS 09 — Deployment / Security / Distribution review

| Conflict ID | Concept | Canonical resolution | Confidence | Domain review |
|---|---|---|---|---|
| CONFLICT-078 | Centralized client execution | Isolated client VPS/container/account/signer/capital | HIGH | RESOLVED PASS09 |
| CONFLICT-079 | Distributed service baseline | One initial image/process/container; logical modules remain separated | HIGH | RESOLVED PASS09 |
| CONFLICT-080 | External database/broker in hot path | No Redis/Postgres/Kafka/Kubernetes baseline dependency | HIGH | RESOLVED PASS09 |
| CONFLICT-081 | Vendor control/license in hot path | License/telemetry/control are cold or optional; vendor not required for execution | HIGH | RESOLVED PASS09 |
| CONFLICT-082 | Tag as artifact truth | Immutable OCI digest plus provenance is authoritative | HIGH | RESOLVED PASS09 |
| CONFLICT-083 | Production `latest` | Explicit version/digest pinning | HIGH | RESOLVED PASS09 |
| CONFLICT-084 | Mutable client state in image | Config/secrets/state/data/logs have declared external boundaries | HIGH | RESOLVED PASS09 |
| CONFLICT-085 | Restart resumes trading | Every restart syncs and reconciles before READY | HIGH | RESOLVED PASS09 |
| CONFLICT-086 | Liveness equals readiness | Liveness, readiness and trading health are distinct | HIGH | RESOLVED PASS09 |
| CONFLICT-087 | License failure disables safety | New risk stops; cancel/reconcile/Recovery/read access remain | HIGH | RESOLVED PASS09 |
| CONFLICT-088 | Vendor-controlled diagnostics | Bundle remains local/redacted until explicit client export | HIGH | RESOLVED PASS09 |
| CONFLICT-089 | Docker guarantees IP secrecy | Packaging is not a confidentiality guarantee; commercial/legal controls remain | HIGH | RESOLVED PASS09 |
| CONFLICT-090 | Hot standby as baseline | Reproducible cold recovery first; standby needs future fencing validation | HIGH | RESOLVED PASS09 |
| CONFLICT-091 | Replace-and-restart update | Transactional risk-off/resolve/backup/handoff/reconcile/health | HIGH | RESOLVED PASS09 |
| CONFLICT-092 | Rollback restores old economic truth | Previous code reconciles against current exchange truth | HIGH | RESOLVED PASS09 |
| CONFLICT-093 | Client config can weaken all limits | Client may tighten, never relax constitutional Risk floors | HIGH | RESOLVED PASS09 |
| CONFLICT-094 | Broad default telemetry | Minimal opt-in telemetry excludes credentials/raw trading/account history | HIGH | RESOLVED PASS09 |
| CONFLICT-095 | Exact Docker/security provider already selected | Behavior locked; base/network/signing/registry choices remain OPEN/calibrated | HIGH | RESOLVED PASS09 |

Full reasoning: `pass09_deployment_security/CONFLICT_RESOLUTION.md`. Conflicts found/resolved: **18/18**. No unresolved PASS09 documentary conflict remains; open products, thresholds, commercial parameters and future standby are retained explicitly.
