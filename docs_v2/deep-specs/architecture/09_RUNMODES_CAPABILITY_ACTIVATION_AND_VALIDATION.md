# 09 — RunModes, Capability Activation and Validation

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

Replay, Paper, Shadow, MicroLive and Live share domain types, event reducers, formulas, Risk semantics, ESM transitions and evidence contracts. They differ only through explicit market/account event sources, transport/effect policy, clock and capability permission. There is no `easy_fill()` or reduced-risk Replay branch.

Effective permission is:

```text
compiled support
∩ configured mode/feature
∩ release channel
∩ signed license scope
∩ CapabilityManifest exact scope
∩ current readiness/health
∩ current per-action RiskDecision
```

M0 specifies; M1 proves units/goldens/properties; M2 proves deterministic Replay; M3 proves same-Core live no-effect behavior; M4 proves bounded real intervention; M5 proves sustained exact-scope Live behavior. Each level is reversible and capped by the least mature critical dependency.

Optional edges are declared by exact capability: basic TTT does not universally depend on advanced Participants; a TTT manifest that consumes a forecast does. Validation emits immutable evidence/manifests outside runtime; runtime reads them and cannot self-promote.
