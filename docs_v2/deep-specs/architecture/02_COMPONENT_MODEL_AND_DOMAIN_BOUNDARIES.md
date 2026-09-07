# 02 — Component Model and Domain Boundaries

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

Logical components are contracts, not necessarily processes or crates. The initial runtime is a modular Rust monolith.

| Component family | Owns | Must not own |
|---|---|---|
| Adapters/Normalizer/Clock | Schema translation, source health and timing observations | Book, Risk or economic permission |
| Book/Metadata/Fee/Precision | Canonical current market/rule state | Strategy decisions |
| Graph/Routes/Watcher/HWC | Structural topology, fixed routes, dependency and compute activation | Inventory truth or Risk permission |
| Formula/Features/Opportunity | Deterministic economics, features and candidate episodes | Orders or capital authority |
| Participants/Simulator/Atlas | Forecasts, outcome distributions and rolling evidence | Actual fills or uncontrolled Live learning |
| Inventory/Capital/Terminal/Sizer/Portfolio/Bridge | Actual exposure interpretation and candidate allocation | Hard-Risk relaxation or order transport |
| Risk/Reservation | Safe action permission and atomic resource claims | Exchange fills |
| Execution/Transport/Recovery/Reconciliation | Plan/order lifecycles, external effects and truth restoration | Formula alternatives or invented balances |
| Accounting/Recorder/Replay | Attribution, evidence and deterministic reconstruction | Trading permission |
| Model/Capability/Operations/Deployment/License | Promoted artifacts, evidence scope, health and lifecycle control | Hot-path economic truth |

Cross-domain exchange uses named immutable interfaces. A consumer may cache a snapshot for bounded computation but may not promote that cache into a competing mutable truth. Ownership changes require domain and Validation impact review.

The detailed rows are in the PASS 13 [Component Catalog](../../_analysis/pass13_master_architecture/COMPONENT_CATALOG.md) and [Domain Interface Catalog](../../_analysis/pass13_master_architecture/DOMAIN_INTERFACE_CATALOG.md).
