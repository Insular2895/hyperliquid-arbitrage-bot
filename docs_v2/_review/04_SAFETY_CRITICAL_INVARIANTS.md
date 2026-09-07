# Safety-Critical Invariants

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

Every review box is intentionally unchecked. Evidence references are documentary; no invariant is claimed proven in code.

| Review | Invariant ID | Exact rule | Why | Owner | Consumers | Failure consequence | Validation evidence | Source authority |
|---:|---|---|---|---|---|---|---|---|
| [ ] | SI-001 | `Safety > StateConsistency > ExistingExposure > RiskLimits > ExpectedPnL > Opportunity` | resolves competing objectives | Risk | all decision makers | unsafe priority choice | Risk property/fault suite | [Risk](../09_RISK_CONSTITUTION.md) |
| [ ] | SI-002 | No stale book may create new risk | stale economics are not executable truth | Book + Risk | Opportunity, Execution | false edge or unmanaged exposure | freshness/gap tests | Risk; Data |
| [ ] | SI-003 | No unknown fees or precision rules | unknown boundaries can create illegal orders/false edge | Fee + Precision | Formula, Execution | invalid order or economics | version/boundary vectors | Formula; Data |
| [ ] | SI-004 | Reserve before any order effect | prevents shared overcommit | Reservation | Risk, Execution | unowned/overcommitted effect | concurrency/property tests | Risk; Execution |
| [ ] | SI-005 | No double spending | one resource cannot fund two routes | Reservation | Capital, Portfolio | aggregate exposure exceeds capacity | reservation replay | Inventory/Capital |
| [ ] | SI-006 | No blind retry | ambiguous submit may already exist | Execution | Transport | duplicate order/exposure | ambiguous-submit trace | Execution |
| [ ] | SI-007 | `SENT` may have executed | lack of ACK is not absence of order | Execution | Risk, Recovery | hidden live exposure | disconnect/crash tests | Execution |
| [ ] | SI-008 | `UNKNOWN` locks reservations | unresolved exposure still owns capacity | Execution + Reservation | Capital, Risk | reused capital plus hidden order | restart/unknown replay | Execution; Risk |
| [ ] | SI-009 | Cancel requested is not canceled | cancel intent is not exchange fact | Execution | Inventory, Recovery | fills ignored after cancel request | cancel-race trace | Execution |
| [ ] | SI-010 | Actual fill only changes economic state | plans/ACKs are not economics | FillLedger | Inventory, Accounting | corrupted inventory/PnL | unique-fill vectors | Execution; Inventory |
| [ ] | SI-011 | Partial fill updates Inventory immediately | next action depends on actual output | FillLedger + Inventory | Risk, ESM | wrong next-leg quantity/exposure | partial-fill suite | Execution |
| [ ] | SI-012 | Recovery uses current state | the planned path can be obsolete | Recovery | Risk, Execution | exit optimizes a nonexistent state | recovery scenario suite | Execution; Risk |
| [ ] | SI-013 | Sunk costs do not control Recovery | past loss cannot justify added unsafe risk | Recovery | Risk, Accounting | loss chasing/unbounded exposure | negative-EV exit tests | Execution; Formula |
| [ ] | SI-014 | Reconcile before new risk after uncertainty | exchange truth must be restored | Reconciliation | Readiness, Inventory, Risk | activity resumes on false state | startup/reconnect/crash suite | Execution; Operations |
| [ ] | SI-015 | No hard Risk bypass | opportunity, operator, license or model cannot relax safety | Risk | all effect producers | unauthorized unsafe effect | authorization/property tests | Risk |
| [ ] | SI-016 | No lookahead | evidence must reflect knowledge available then | Data/Replay | Models, Validation | invalid validation/economic claim | temporal leakage checks | Recorder/Replay |
| [ ] | SI-017 | No silent formula/model version change | reproducibility needs exact artifacts | Data/Validation | Core | non-reproducible decision drift | manifest/hash replay | Data; Formula |
| [ ] | SI-018 | Position Sizing is not Order Slicing | decomposition cannot increase exposure | Sizer | Execution | slice sum exceeds validated q | quantity conservation tests | Inventory/Capital |
| [ ] | SI-019 | OWA requires a fair direct comparator | otherwise alpha is misclassified | Opportunity | Formula, Validation | false OWA claim | comparator vectors | Graph/Routes |
| [ ] | SI-020 | Bridge is not OWA | moving capital is a distinct economic action | Capital | Risk, Accounting | bypassed relocation gates/double count | classification tests | Inventory/Capital |
| [ ] | SI-021 | Strategy, Bridge, Rebalance and Recovery are distinct | disjoint attribution prevents double counting | Accounting | Operations, Validation | misleading PnL and decisions | ledger reconciliation | Inventory/Capital |
| [ ] | SI-022 | More capital does not imply more `Q_validated` | size support is empirical and nonlinear | Validation | Sizer, Risk | unsupported larger exposure | next-band evidence | Validation |
| [ ] | SI-023 | Implemented does not mean validated | code existence is not evidence | Validation | Deployment, Capability | unproven feature activates | manifest gate tests | Validation |
| [ ] | SI-024 | Licensed does not mean validated | commercial permission is not safety | Deployment | Capability, Risk | commercial state grants unsafe action | license-failure tests | Deployment |
| [ ] | SI-025 | Running does not mean ready | process health is not coherent exchange state | Operations | Execution | effects before reconciliation/readiness | startup gate suite | Operations |
| [ ] | SI-026 | Software rollback is not exchange rollback | software cannot undo prior fills/orders | Deployment | Recovery, Reconciliation | external exposure is forgotten | rollback drill | Deployment; Execution |
| [ ] | SI-027 | No dual active economic owner | duplicate truth races and diverges | Architecture | all modules | duplicate effects/state corruption | ownership audit | Master Architecture |
| [ ] | SI-028 | Failure makes the system less active | faults cannot expand authority | Risk + Operations | all capabilities | failure increases exposure/permission | fault injection | Risk; Validation |

Reviewer red-team prompts: What happens during ambiguous submit plus restart? Can any telemetry/license outage strand exposure? Can a second instance share an account? Can stale worker output commit? Can a model or larger balance expand permission without a new manifest? Any “yes” is a blocking rejection.
