# Component Ownership Matrix

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

`Y*` means the component mutates only its owned logical family. `Effect` means it requests/sends external action; external observations still return as events.

| Component family | Owns state | Mutates economic truth | Produces decision/proposal | Sends external effect | Model | QF | Hot path | Replay-identical logic | Persistent | Risk critical | Deployment critical |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Adapters/Normalizer/Clock | Y* | N | N | Adapter I/O | N | N | Y | schema/clock policy | RAW/quality | Y | Y |
| Ordered Coordinator | Y* | commits | Y | requests | N | N | Y | Y | journal | Y | Y |
| Book/Metadata/Fee/Precision | Y* | market/rule truth | N | N | N | Y | Y | Y | checkpoint/PIT | Y | Y |
| Graph/Routes/`pair_to_routes` | Y* | N | candidate inputs | N | N | Y | Y | Y | definitions | Y | N |
| Watcher/HWC | Y* | N | activation proposal | N | optional | Y | bounded | Y | snapshots | N | N |
| Features/Formula/Opportunity | Feature only | N | Y | N | optional | Y | Y | Y | L3/L4 | Y | N |
| Participants | artifact refs only | N | forecast | N | Y | Y | bounded | Y | forecasts | Y | N |
| Simulator | branch state only | N | distribution | N | Y | Y | configured | Y | reports | Y | N |
| Atlas | Y* | N | evidence/proposal | N | Y | Y | read only | PIT | derived | N | N |
| Inventory/Capital/Terminal/Sizer/Portfolio/Bridge | Inventory Y* | fills only via reducer | proposal | N | optional | Y | mixed | Y | journal/derived | Y | N |
| Risk | Y* | permission only | Y | N | consumes | Y | Y | Y | decisions | constitutional | Y |
| Reservations | Y* | resource ownership | Y | N | N | Y | Y | Y | journal | Y | Y |
| Execution Coordinator | Y* | lifecycle | Y | requests | consumes | Y | Y | Y | journal | Y | Y |
| Transport | connection only | N | N | Y | N | N | Y | mode adapter differs | observations | Y | Y |
| Recovery/Reconciliation | Y* | reconciled commit | proposal/Y | query/effect via transport | consumes | Y | Y | Y | journal | Y | Y |
| Accounting | Y* records | realized attribution | N | N | N | Y | N | Y | Y | N | N |
| Recorder/Replay | Recorder Y* | N | Replay report | disk/source effect | N | N | enqueue only | Core Y | Y | evidence | Y |
| Model/Capability Managers | Y* | N | promotion scope | artifact/license I/O BG | Y | N | read snapshot | PIT | Y | Y | Y |
| Operations/Infra/Deployment/License | Y* health/lifecycle | N | alert/control | BG/control only | N | diagnostics | snapshot only | mode-aware | Y | Y | Y |

Detailed component inputs, outputs, failure scopes and maturity are in [COMPONENT_CATALOG.md](COMPONENT_CATALOG.md).
