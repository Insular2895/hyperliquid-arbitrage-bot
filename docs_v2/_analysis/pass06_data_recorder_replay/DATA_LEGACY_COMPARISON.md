# Data / Recorder / Replay Legacy Comparison

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Legacy review occurred only after the V2 masters/deep specs were written. Reviewed read-only: `docs/11_DATA_CONTRACTS.md`, `docs/12_RECORDER_AND_REPLAY.md`, `docs/13_INFRASTRUCTURE.md`, `docs/16_VALIDATION_MATRIX.md`, `docs/18_OPERATIONS_AND_MONITORING.md`, and relevant specs for Recorder, ReplayEngine, Normalizer, ClockAndRng and FeedAdapter.

| Legacy omission/ambiguity | V2 recovery |
|---|---|
| No exact L0–L4 table | Exact five-layer matrix and authority boundaries |
| RawEvent used `recorder_sequence` and added non-closure concepts | Exact closure field name/list: `recorder_seq` etc. |
| Source enum absent | Five exact Source variants |
| SourceQuality absent | Exact four fields and unknown semantics |
| Market/Account event enums incomplete | Closure variants indexed |
| Ticks/lots rule terse | Exact exchange-boundary numeric rule/tests |
| Canonical state list/ownership incomplete | One logical state owner, immutable publication, versions |
| Reducer/effect boundary absent | Pure reducer, separate executor, command/event distinction |
| Worker staleness absent | `input_state_version`, TTL, discard/revalidate |
| RunManifest fields expanded without closure distinction | Exact frozen fields plus linked deployment/research evidence |
| DecisionTrace exact schema absent | Four exact arrays and deterministic function identity |
| Ordering rule only “recorder order” | Receive/monotonic/source priority/recorder tie-break contract |
| EventTime vs ReceiveTime underexplained | Separate chronology vs bot-knowledge semantics |
| Only three Replay modes implied | Four exact modes including INTERACTIVE |
| Replay fidelity/mode axes conflated | Replay mode, RunMode, ReplayFidelity, SimulationMode separated |
| No complete No-Lookahead attack surface | Future buffers/features/models/timers/checkpoints covered |
| Recorder priority was P2 derived/P3 RAW | Corrected to SRC-005 P2 market/P3 derived |
| No INVALID/LOW_FIDELITY contract | Scoped dataset quality regions |
| ExecutionJournal event list absent | Exact closure envelope/minimum events |
| Retention class semantics incomplete | Four exact classes and permanent evidence set |
| Cleanup proof terse | close/upload/remote checksum/holds prerequisites |
| Checkpoint fields/equivalence incomplete | Cursor/hash/schema and full-vs-seek replay equality |
| Point-in-time model distinction absent | Historical truth vs `COUNTERFACTUAL_MODEL` |
| Training contamination controls incomplete | temporal split/training-range artifact rules |
| Lineage chain incomplete | 68-contract inventory and edge keys |
| Schema failure actions incomplete | model disable/config boot failure/state rebuild matrix |
| Recorder/Replay DoD not mapped to closure lines | 33-test validation map and SRC-006 closure |

Material legacy omissions/ambiguities recovered: **27**. Legacy files modified: **NO**. The useful legacy statements remain compatible where not contradicted; legacy is not promoted to authority.

## Classification summary

| Classification | Count | Treatment |
|---|---:|---|
| `RECOVERED` | 27 | Missing/ambiguous material listed above is explicit in V2 |
| `OVER_COMPRESSED` | 5 master areas | Layers, ordering, determinism, lineage and recovery were expanded from terse legacy prose |
| `MISSING` | 0 after V2 recovery | Every material omission identified has a destination |
| `SUPERSEDED` | 1 | Legacy P2-derived/P3-general priority order |
| `CONTRADICTED` | 1 | Any reading that normalizes storage priority into Core economic order is rejected |
| `LEGACY_UNTRACED` | 0 accepted as authority | Extra legacy fields/claims without closure provenance were not imported silently |
| `ROUTED_TO_OTHER_PASS` | 6 families | Full Inventory/Accounting, RiskConfig/kill encoding, deployment restore, operations telemetry, formula definitions and validation capability registry |

Examples in legacy such as `recorder_sequence`, extra RawEvent venue/checksum fields and expanded RunManifest fields are not silently declared frozen. They are either mapped to the closure name, carried by an enclosing manifest, or left to the owning future domain.
