# Determinism, RNG and Hash Validation

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

The system enforces:

```text
DecisionTrace = F(OrderedEvents, ResolvedConfig,
                  ModelArtifacts, FormulaVersion, Seed)
```

Core time comes from Clock. Randomness comes from RngProvider; Replay stores the seed in RunManifest. No reducer uses host wall time, network, disk, implicit RNG or iteration order. Deterministic model inference is required where possible; exact ticks/lots remain integers and threshold comparisons declare any necessary numeric epsilon.

Parallel workers may calculate features, models, simulation, compression and analytics. Each result includes input state version and validity; only a single ordered coordinator commits. Completion order cannot change decisions. Canonical serialization sorts maps/sets and fixes float representation.

Validation runs the same input repeatedly and compares ordered events, state-transition sequence, RiskDecisions, OrderIntents, final state and DecisionTrace hash. Periodic StateHashes identify the first divergent `recorder_seq`. A hash mismatch is never waived as harmless without locating and classifying the semantic difference.

Accelerated and checkpoint-assisted replay must equal full exact replay under the same semantic mode. Counterfactual assumptions intentionally change the input manifest and therefore create a distinct run/branch identity.
