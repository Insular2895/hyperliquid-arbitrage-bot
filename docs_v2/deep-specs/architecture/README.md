# Architecture Deep Specifications

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

These documents decompose [00 — Master Architecture](../../00_MASTER_ARCHITECTURE.md) without replacing domain authority.

| Spec | Concern |
|---|---|
| [01](01_SYSTEM_CONTEXT_AND_ARCHITECTURAL_PRINCIPLES.md) | Product boundary, scope and governing principles |
| [02](02_COMPONENT_MODEL_AND_DOMAIN_BOUNDARIES.md) | Logical components and domain ownership |
| [03](03_STATE_OWNERSHIP_EVENTS_COMMANDS_AND_EFFECTS.md) | Single writers, snapshots and event/effect separation |
| [04](04_HOT_PATH_AND_ASYNCHRONOUS_ARCHITECTURE.md) | Compute classes and latency boundaries |
| [05](05_MARKET_TO_DECISION_PIPELINE.md) | Market state through decision and reservation |
| [06](06_EXECUTION_RECOVERY_AND_RECONCILIATION_PIPELINE.md) | Actual-fill execution and truth restoration |
| [07](07_DATA_REPLAY_RESEARCH_AND_MODEL_PIPELINE.md) | L0–L4, determinism, Replay and model artifacts |
| [08](08_INVENTORY_CAPITAL_RISK_AND_ALLOCATION_PIPELINE.md) | Exposure, viability, sizing, allocation and action taxonomy |
| [09](09_RUNMODES_CAPABILITY_ACTIVATION_AND_VALIDATION.md) | Same Core, M0–M5 and permission intersection |
| [10](10_RUNTIME_DEPLOYMENT_SECURITY_AND_CLIENT_TOPOLOGY.md) | Modular monolith, OCI and client boundaries |
| [11](11_FAILURE_CONTAINMENT_AND_DEGRADATION_ARCHITECTURE.md) | Scoped fail-closed behavior and safe actions |
| [12](12_CURRENT_V1_FUTURE_BOUNDARIES_AND_EVOLUTION.md) | Current, progressive and Future capabilities |

Authority order: owning domain master/deep spec → Formula/Risk/Data/Execution closures → this cross-domain synthesis. The completed [PASS 14 audit](../../_analysis/pass14_cross_domain_consistency/PASS14_FINAL_REPORT.md) records cross-domain resolutions and bounded residual dependencies.
