# Replay Determinism Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Functional identity

```text
DecisionTrace = F(
  OrderedEvents,
  ResolvedConfig,
  ModelArtifacts,
  FormulaVersion,
  Seed
)
```

`RunManifest` pins run/mode, git commit, build hash, config hash, optional DatasetId, model versions, formula schema, event schema, start time and optional random seed. Deployment/image and critical dependency identities are linked where needed to reproduce the executable/environment.

## Determinism mechanisms

| Mechanism | Contract |
|---|---|
| Same Core | Replay replaces source/transport/effect boundary only; no replay-specific business logic |
| Canonical order | Receive timeline, source priority at equality, Recorder sequence final tie-break |
| Clock | Core uses ReplayClock; accelerated wall execution preserves domain intervals |
| RNG | All randomness through seeded/versioned RngProvider |
| Reducers | No network, disk, hidden time or hidden randomness |
| Workers | Immutable inputs + input state version; ordered coordinator commits or rejects stale result |
| Serialization/hash | Canonical field/collection/float representation, independent of HashMap/thread order |
| No Lookahead | No later receive event or derived future information visible at T |
| Point-in-time | Historical truth uses only artifacts available at T; later model labeled `COUNTERFACTUAL_MODEL` |
| Checkpoint | Full replay to N equals compatible checkpoint K + exact suffix K+1..N |

## Required equality tests

Two runs with identical ordered events, resolved configuration, model artifacts, formula/schema versions and seed must produce identical normalized input, state-transition order, decisions, rejects, OrderIntents, final state, DecisionTrace and canonical hash. Golden tests may use an explicitly defined economic tolerance for PnL only after exact ticks/lots and deterministic quantization.

On mismatch, StateHashes and Recorder/journal sequences identify the first divergent input or transition. A nondeterministic trace is a release blocker, not a tolerated flaky test.

## Mode boundaries

EXACT RECEIVE-TIME and ACCELERATED must be semantically equal for the same manifest. COUNTERFACTUAL LATENCY and INTERACTIVE intentionally change versioned inputs/branch identity; repeated execution of the same changed manifest still must be deterministic. Simulator stochastic paths remain reproducible per seed/path ID.
