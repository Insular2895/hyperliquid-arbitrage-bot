# Data and Replay Pipeline

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

```mermaid
flowchart TD
  X[External payload + source timestamps] --> R[L0 RawEvent immutable]
  R --> N[L1 normalized typed event + raw lineage]
  N --> O[receive-time/recorder_seq ordered stream]
  O --> S[L2 canonical reducers/state]
  S --> F[L3 features/forecasts]
  F --> D[L4 decisions/results]
  D --> J[Execution journal/outcomes]
  R --> DS[Versioned point-in-time dataset]
  DS --> RS[Replay source + ReplayClock]
  RS --> N2[chosen normalization version]
  N2 --> CORE[same ordering/reducers/formulas/Risk/ESM]
  CORE --> DT[DecisionTrace + state hashes/ReplayReport]
```

Ordering in one capture context is `(recv_monotonic_ns, source_priority, recorder_seq)`, with `recorder_seq` the definitive final local observation order. Exchange time does not replace bot-knowledge order. Cross-recorder merge requires an explicit versioned policy.

`RunManifest` pins run/mode, build/config, optional dataset, models, FormulaVersion, event schemas, start and seed. DecisionTrace retains ordered decisions, order intents, state transitions and Risk decisions. Complete identical inputs must produce identical trace/hash regardless of worker scheduling.

No lookahead means no later event, feature, model, timer, checkpoint content or preloaded buffer is visible at replay T. Modern-on-old artifacts are labeled counterfactual, never Historical Truth. Recorder remains non-blocking and its quality/backpressure is explicit.
