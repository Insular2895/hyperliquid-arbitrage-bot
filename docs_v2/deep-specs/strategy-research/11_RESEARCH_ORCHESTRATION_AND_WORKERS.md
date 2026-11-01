# 11 — Research Orchestration and Workers

`DOCUMENTATION STATUS: F2 PART 2 / INTERMEDIATE DOCUMENTARY WORK / AWAITING HUMAN REVIEW`

`CAPABILITY STATUS: FUTURE SPECIFIED / NOT ACTIVE / NO DRAGONFLY DEPENDENCY`

This document specifies the future architectural problem named **Distributed Research / Experiment
Orchestration** before selecting a product. It implements nothing, authorizes no research runtime
and places no distributed component in the production trading hot path.

## 1. Component boundaries

| Component | Owns | Must not own |
|---|---|---|
| Experiment Manager | expand one frozen protocol into deterministic bounded jobs; lifecycle/attempt tracking; deterministic aggregation | hypothesis mutation, economic truth, permission or orders |
| worker | execute one immutable job through the named canonical engines | selection, promotion, shared truth mutation or silent retries |
| Replay | deterministic reconstruction from recorded evidence | alternative history, scenario invention or promotion |
| Simulator | canonical counterfactual economic/execution scenario evaluation | actual-fill truth, search policy or permission |
| Falsifier | tier protocol, diagnostics, region/disposition evidence | Formula/Risk/ESM redefinition or authorization |
| Experiment Registry | durable immutable manifests, results, hashes and lineage | recomputation of truth or deletion of unfavorable evidence |
| Analytics/Dashboard | read-only projections over registry evidence | machine-fact mutation, confidence invention or trading control |
| optional coordinator | transient queue/lease/heartbeat/cache/progress state | durable scientific truth or any production authority |

The Manager consumes `EXP-*`; it does not create or rewrite it during execution. An internal job
key may deterministically address work, but it is not a competing runtime identity and never
replaces canonical `RunId`, `DatasetId` or `EvidenceId`.

## 2. Deterministic Experiment Manager

### D3 — Manager and deterministic workers

```text
FROZEN EXP-* + protocol hash + budget + ordered candidate plan
                              |
                              v
                    EXPERIMENT MANAGER
          validate bounds -> derive deterministic jobs
                              |
            +-----------------+-----------------+
            |                 |                 |
            v                 v                 v
         Worker A          Worker B          Worker C
      canonical Core    canonical Core    canonical Core
            |                 |                 |
     completion #3      completion #1      completion #2
            +-----------------+-----------------+
                              |
                              v
        validate identity/version/hash + preserve attempts
                              |
                              v
     AGGREGATE BY FROZEN SCIENTIFIC ORDER, NOT ARRIVAL ORDER
                              |
                              v
            immutable Run results -> Registry/Reports
```

Read top-to-bottom: the frozen plan determines all eligible jobs; workers may finish in any order;
the Manager validates outputs and commits the scientific view in the declared deterministic order.

Contract — **Inputs:** immutable `EXP-*` version/protocol hash, Dataset/config/scenario/seed
manifests and budget. **Operations:** bound validation, deterministic job expansion, dispatch,
attempt tracking, output verification and ordered aggregation. **Outputs:** complete Run/attempt
lineage and report-ready results. **Canonical authority:** Experiment Manager for orchestration
only; Replay/Simulator/Falsifier/Data own semantics and evidence. **Failure/uncertainty:** timeout,
worker crash, invalid hash, unsupported cell and censored outcome remain distinct and retained;
none becomes economic failure automatically. **Activation timing:** no runtime now; bounded local
form only after exact dependencies and authorization, distributed form only after later evidence
and approval.

### Manager invariants

- Deterministic job expansion is a pure function of the frozen protocol, ordered candidate set,
  Dataset/version references, scenario plan and seed policy.
- Parameter-space bounds, evaluation budget, splits, guardrails, selection rule, T2 plan and final
  holdout policy cannot expand mid-run.
- A job pins exact configuration/config hash, dataset/split, Git/build/image, Formula/Fee/Metadata/
  Book/Graph/Simulator/model versions, RunMode, ReplayMode, fidelity, fully qualified Falsifier
  tier, scenario assumptions and seed/stream where relevant.
- Canonical result order uses the frozen evaluation ordinal and declared tie policy; worker
  completion time, lease acquisition time and host identity never choose a candidate.
- Results are accepted only after identity, version, content-hash, completeness and validity
  checks. Aggregates are reproducible from immutable accepted results.
- The Manager cannot create a hypothesis, adapt guardrails to find a winner, optimize on the final
  holdout, change canonical engines, grant Strategy/Risk/capital permission or send an order.

Job lifecycle and scientific result lifecycle remain separate. Illustrative job states such as
planned, eligible, leased, running, completed, failed, timed out and canceled describe compute.
Scientific dispositions such as invalid/unsupported, negative, censored, T0/T1 failure,
`INCONCLUSIVE` or candidate evidence come only from the canonical evaluation and Validation
contracts. Final serialized states are `HUMAN_DECISION_REQUIRED`.

Every retry is a new linked compute attempt with reason, worker/environment, timestamps and output
hash. A successful retry does not erase the earlier failure. Compute retry is idempotent work
re-execution under the same immutable inputs; it is unrelated to and cannot weaken the canonical
**no blind trading-order retry** rule.

## 3. Early bounded local execution versus later distributed research

### D4 — Capability split

```text
EARLY, NARROW, SEPARATELY AUTHORIZED       LATER, FULL BASELINE GATED

One frozen Bounded Experiment Plan         Generalized Research Program
                 |                                      |
                 v                                      v
     bounded local scheduler                distributed-capable Manager
                 |                                      |
       +---------+---------+                   +---------+---------+
       |         |         |                   |         |         |
   local W1  local W2  local Wn            local     VPS A     VPS B
       +---------+---------+                   +---------+---------+
                 |                                      |
                 v                                      v
 canonical Replay/Simulator/Falsifier       same canonical engines/versions
                 |                                      |
                 v                                      v
 immutable Run results + Region             Registry + Analytics + candidates

No fixed optimal n; measure resource use.       No deployment without measured need.
Neither side enters the production trading hot path.
```

Read left-to-right: a local pool may accelerate one finite declared Falsifier plan; only the later
full program may justify multi-host orchestration, and both use identical canonical semantics.

Contract — **Inputs:** left: one frozen bounded plan; right: later approved generalized research
program. **Operations:** bounded parallel pure computation with deterministic aggregation.
**Outputs:** left: Run results/region; right: durable registry evidence/analytics. **Canonical
authority:** canonical Core/Replay/Simulator/Falsifier, never workers. **Failure/uncertainty:**
resource contention, oversubscription, host loss and partial completion remain measured job
evidence; missing work is not a favorable cell. **Activation timing:** left only after exact T1
dependencies and separate implementation authorization; right only after the complete README
baseline gate and distributed-system authorization.

Local research compute runs outside the production trading process/hot path. Worker count,
concurrency, memory/CPU/disk budgets and isolation are calibrated from profiling; “four workers”
is only an illustration, never an optimum. The local scheduler must remain bounded and must not
starve Recorder, Replay evidence capture or any production safety component.

Generalized Parameter Search, adaptive hypothesis generation, AI discovery, Monte Carlo programs,
strategy Champion/Challenger, regime portfolio optimization, drift-driven selection and
distributed infrastructure remain inactive even if local bounded batches later become available.

## 4. Future distributed solution space

Potential solution classes are:

- local scheduler and worker pool;
- filesystem/job manifests;
- database-backed job queue;
- lightweight distributed scheduler;
- DragonflyDB;
- other benchmarked alternatives.

The architectural need must be demonstrated before a product is selected: workload no longer fits
the bounded local envelope, and a candidate must improve measured throughput/reliability/cost while
preserving reproducibility, semantic parity, operability, security and recovery. Complexity is not
itself scale evidence.

Potential coordination functions are queueing, scheduling, leases, heartbeats, retry orchestration,
temporary cache, progress, bounded priority/concurrency and worker capacity/health. Durable
immutable manifests/artifacts/results must survive coordinator loss independently.

### D5 — Optional DragonflyDB coordination and authority exclusions

```text
                    EXPERIMENT MANAGER
                            |
                            v
               COORDINATION INTERFACE
      filesystem / DB queue / scheduler / Dragonfly candidate
          transient jobs, leases, heartbeats, cache, progress
                            |
          +-----------------+-----------------+
          |                 |                 |
          v                 v                 v
        Mac workers      Research VPS 1    Research VPS 2
          |                 |                 |
          +-----------------+-----------------+
                            |
                            v
          hash/version validation + ordered aggregation
                            |
                            v
             DURABLE IMMUTABLE RESULT STORE
                            |
                            v
             Experiment Registry -> Analytics

DENY AUTHORITY:
ActualFill | Inventory | orders/ESM | Risk | Recovery/Reconciliation
signer/keys/nonce | capital | Q_validated | promotion | Live config
```

Read top-to-bottom: the coordination interface may distribute transient work, while validated
results flow to a coordinator-independent durable store; the deny list prevents coordination from
becoming production or scientific authority.

Contract — **Inputs:** immutable job manifests and declared worker capacity. **Operations:**
optional queue/lease/heartbeat/cache/progress and attempt-aware retries. **Outputs:** transient job
state plus validated results in a durable evidence store. **Canonical authority:** Manager
orchestrates; canonical engines compute; Registry/Data preserve evidence; the coordinator owns
none of their truth. **Failure/uncertainty:** coordinator/worker/network loss expires or requeues a
compute lease with attempt lineage; cache loss triggers recomputation, not evidence loss; duplicate
results are retained/deduplicated by immutable identity and hash. **Activation timing:** DragonflyDB
is only a deferred candidate requiring benchmark, human selection and separate authorization; no
dependency or deployment is authorized.

### Required separations

| Never conflate | Required rule |
|---|---|
| job state vs scientific truth | queue “complete” means bytes returned, not valid or favorable evidence |
| temporary cache vs durable evidence | cache is disposable; manifests/results/artifacts are immutable and content-hashed |
| worker failure vs economic failure | crash/timeout is compute evidence; only a valid canonical evaluation supports economic disposition |
| compute retry vs order retry | compute may re-execute immutable input with attempt lineage; trading no-blind-retry remains untouched |
| completion order vs result order | aggregate by frozen scientific ordinal/tie policy, never first-worker-wins |
| duplicate compute vs duplicate evidence | preserve attempt lineage; never silently count twice or erase |

Workers use the same canonical Core/Replay/Simulator semantics and pin identities, versions, seeds
and content hashes. Distributed research has no default access to production accounts, signer,
keys, nonce, order transport, capital or Live configuration. It is not a production HA mechanism.

## 5. Registry and reporting handoff

The Manager emits job/attempt manifests and result references; canonical `RunId` records and
immutable artifacts go to the [Research Knowledge Base](../../research/README.md). Registry
acceptance records validation state and hash; it does not reinterpret economics. Analytics reads
accepted and rejected/invalid populations. Dashboard projections cannot mutate either.

If only a transient coordinator acknowledges a result and the durable artifact is absent or fails
hash/version checks, the scientific result is missing/invalid. A queue acknowledgement can never
stand in for `EvidenceId`.

## 6. Human decisions and safe defaults

| Decision | Classification | Safe default |
|---|---|---|
| final Manager/job/attempt schema and storage | `HUMAN_DECISION_REQUIRED` | documentary manifests; no runtime |
| local worker count, concurrency and resource/isolation budget | `CALIBRATED / HUMAN_DECISION_REQUIRED` | smallest bounded pool; no production contention |
| deterministic adaptive-search decision barriers | `HUMAN_DECISION_REQUIRED` | non-adaptive finite plan |
| distributed queue, lease, heartbeat, retry and priority policy | `HUMAN_DECISION_REQUIRED` | distributed execution disabled |
| durable artifact/result store and disaster recovery | `HUMAN_DECISION_REQUIRED` | no distributed activation |
| DragonflyDB or alternative benchmark/selection | `HUMAN_DECISION_REQUIRED / DEFERRED` | no dependency, deployment or production use |
| dashboard/analytics implementation | `HUMAN_DECISION_REQUIRED / DEFERRED` | reports/indexes only; read-only semantics |

No decision above may widen the full baseline gate or the absolute authority exclusions. Prompt 3
may reconcile placement/governance without selecting these implementation choices.
