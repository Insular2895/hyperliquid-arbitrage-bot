# Canonical Decisions Summary

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

These are already canonical documentary decisions. Changing one is an explicit design override with impact analysis, not completion of an open checkbox.

| Decision ID | Canonical decision | Status / why | Owning authority | Implementation consequence | Human action now? |
|---|---|---|---|---|---:|
| CD-001 | Rust production Core; offline Python lab; no baseline C++ | LOCKED; deterministic low-latency Core plus separate research | [Master Architecture](../00_MASTER_ARCHITECTURE.md) | no Python/C++ strategy hot path | No |
| CD-002 | Event/command/effect model with one logical ordered coordinator and single writers | LOCKED; prevents dual truth and completion-order nondeterminism | Architecture + Data | reducers commit ordered events; adapters cannot mutate Core | No |
| CD-003 | Replay, Paper, Shadow, MicroLive and Live use the same Core | LOCKED; parity and evidence | Data/Replay | mode changes effect adapters and permissions, not logic | No |
| CD-004 | `NetConvert(q)` is the single conversion primitive | LOCKED; prevents divergent economics | Formula Book | BBO may reject but never replace exact L2 acceptance | No |
| CD-005 | Direct/Route2/Cycle3 routes are precomputed; no generic hot-path graph traversal | LOCKED; bounded deterministic work | Graph/Routes | affected routes found through reverse indexes | No |
| CD-006 | Structural Graph, empirical Atlas and capital HWC/reachability are distinct | LOCKED; separates possibility, evidence and usable capital | Graph + Inventory/Capital | no state family may impersonate another | No |
| CD-007 | Know the universe broadly; expensive compute follows relevance and capital | LOCKED; bounded compute | Architecture | cheap broad awareness, selective exact computation | No |
| CD-008 | Only unique actual fills change economic state | LOCKED safety truth | Execution + Inventory | plans, sends and ACKs never fabricate Inventory | No |
| CD-009 | Reserve shared balance/book/Risk capacity before an order effect | LOCKED safety truth | Reservations + Risk | atomic claim; UNKNOWN keeps ownership locked | No |
| CD-010 | Never blindly retry an ambiguous submit | LOCKED safety truth | Execution | query/reconcile by identity before another effect | No |
| CD-011 | Recovery and Reconciliation are first-class state machines | LOCKED; unresolved exposure is critical | Execution + Risk | startup/unknown/reconnect/crash/update paths cannot bypass them | No |
| CD-012 | Risk hierarchy is Global → Inventory/Allocation → Route → Leg → Order | LOCKED; upper layers only narrow | Risk Constitution | no lower-level or commercial bypass of hard gates | No |
| CD-013 | Capability activation is manifest- and evidence-scoped | LOCKED; progressive activation | Validation | `CapabilityManifest` binds market/mode/q/version/evidence | No |
| CD-014 | Client account, signer, capital and persistent data remain client-isolated | LOCKED product/security model | Deployment | no vendor custody or shared multi-tenant execution baseline | No |
| CD-015 | No SaaS/license/storage call synchronously blocks the trading hot path | LOCKED containment rule | Architecture + Deployment | external service failure can only reduce activity safely | No |
| CD-016 | Evidence precedes capital | LOCKED governing sequence | Validation + Roadmaps | implementation or uptime alone grants no capital | No |
| CD-017 | BBO cannot replace full-L2 QF-016; FastL1 is exact or falls back | LOCKED correction boundary | Graph + Formula | q above L1 is not a reject | No |
| CD-018 | One `Π_exec(q,state)` owns execution outcomes; no blind probability stacking | LOCKED correction boundary | Simulator + Formula | completion/survival/priority evidence calibrates one distribution | No |
| CD-019 | Priority read/write scopes and costs remain typed and exact-once | current external fact plus pending policy | Infra + Simulator + Accounting | no generic priority multiplier/optimizer | Review HDC/external evidence |
| CD-020 | InfraProfile is expiring evidence, not truth or a Live dependency | pending `HDC-077..079` | Data + Recorder + Infra + Validation | no permanent challenger rental or actual-label leakage | Review HDC |
| CD-021 | Advanced strategy research is deferred, uses the same Core/Simulator and has no automatic/AI promotion | pending `HDC-080..090` | Architecture + Data + Simulator + Validation | baseline first; OOS/Shadow/Micro-live evidence; 26 phases only | Review HDC |

Human review confirms or rejects this baseline as a whole in the [decision form](21_FINAL_HUMAN_DECISION_FORM.md). Individual overrides must name the affected authorities, invariants, tests and traceability.
