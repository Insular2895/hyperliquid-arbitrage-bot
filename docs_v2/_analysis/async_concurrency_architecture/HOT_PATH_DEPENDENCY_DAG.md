# Hot-Path Dependency DAG

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

## Edge types

- `HARD_DATA_DEPENDENCY`: downstream meaning requires the exact upstream result/current state.
- `SAFE_PARALLEL_EVIDENCE`: pure work may run concurrently from the same immutable snapshot; completion is only evidence/proposal.
- `PRECOMPUTABLE`: work can be incrementally maintained or prepared before the opportunity without using future knowledge.

```mermaid
flowchart TD
  RX[C3 receive bytes] -->|HARD_DATA_DEPENDENCY| N[C1 decode/normalize]
  N -->|HARD_DATA_DEPENDENCY| O[C0 order]
  O -->|HARD_DATA_DEPENDENCY| B[C0 Book/metadata/account reducers]
  B -->|PRECOMPUTABLE| ROLL[C1 rolling features/health]
  B -->|HARD_DATA_DEPENDENCY| PR[C1 pair_to_routes]
  PR -->|HARD_DATA_DEPENDENCY| BBO[C1 freshness/BBO]
  BBO -->|HARD_DATA_DEPENDENCY| L2[C1 full-L2 NetConvert baseline]
  BBO -->|SAFE_PARALLEL_EVIDENCE| RW[C2 route/q/model workers]
  ROLL -->|SAFE_PARALLEL_EVIDENCE| RW
  L2 -->|HARD_DATA_DEPENDENCY| OP[C1 Opportunity/economics]
  RW -->|HARD_DATA_DEPENDENCY: revalidate| AC[C0 accept/discard proposals]
  OP -->|HARD_DATA_DEPENDENCY| AC
  AC -->|HARD_DATA_DEPENDENCY| SZ[C0 deterministic size/allocation selection]
  SZ -->|HARD_DATA_DEPENDENCY| RK[C0 current final Risk]
  RK -->|HARD_DATA_DEPENDENCY| RS[C0 atomic Reservation]
  RS -->|HARD_DATA_DEPENDENCY| PL[C0 immutable ExecutionPlan/Intent]
  PL -->|HARD_DATA_DEPENDENCY| SG[C1 local signing]
  SG -->|HARD_DATA_DEPENDENCY| SE[C3 submit effect]
  SE -->|HARD_DATA_DEPENDENCY| EV[C3 observed ACK/update/fill/timeout]
  EV -->|HARD_DATA_DEPENDENCY| O
  B -->|PRECOMPUTABLE| REC[C1 bounded Recorder enqueue]
  REC -->|SAFE_PARALLEL_EVIDENCE| DISK[C4 write/compress/checkpoint/archive]
```

## Leg dependency

```text
actual unique fill for Leg 1
  --HARD_DATA_DEPENDENCY--> current Inventory/Account/Reservation update
  --HARD_DATA_DEPENDENCY--> Risk revalidation
  --HARD_DATA_DEPENDENCY--> exact Leg 2 quantity/price/intent
```

Pure Leg 2 preparation—route lookup, rule lookup, template building, predicted scenarios—may run as `SAFE_PARALLEL_EVIDENCE`. It cannot select the executable quantity, authorize, sign or send Leg 2 before the actual prior fill is committed. The same rule applies recursively to TTT.

## Parallel regions

- Independent route or q calculations sharing an immutable version tuple may run concurrently.
- Optional Participant and F2/F3 Simulator computations may run concurrently with cheap baseline work.
- Recorder serialization, compression, checksums, archive and metrics aggregation run after a bounded handoff.
- None of these regions bypasses ordered proposal acceptance, current Risk or Reservation.

## Forbidden edges

- worker completion → direct order send;
- ACK callback → direct Execution mutation;
- predicted fill → later-leg executable quantity;
- background writer failure → silent evidence loss;
- remote model/license/archive response → synchronous hot-path permission;
- wall-clock thread order → canonical decision priority.
