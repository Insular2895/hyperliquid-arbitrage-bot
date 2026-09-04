# PASS 02 — Participant Conflict Resolution

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 02 REVIEW COMPLETE`

The requested tensions were checked against original sources. They are mostly explicit design evolution or scope boundaries, not competing current rules.

| Conflict | Earlier/candidate reading | Later/authoritative resolution | Result | Residual |
|---|---|---|---|---|
| `CONFLICT-011` Participant truth | Populate a market with named synthetic bot archetypes and infer realism from stylized output. | SRC-007/008 explicitly makes aggregate, observable response and survival the production target; agents are P5 scenarios. | `RESOLVED` | Agent calibration remains Research. |
| `CONFLICT-012` Address identity | Public pseudonymous counterparties could invite identity- or strategy-centric classification. | SRC-007 states address is not identity; only passive `ParticipantAddress`/signature/cluster with lift. | `RESOLVED` | Current fields/privacy require revalidation. |
| `CONFLICT-013` Cross-market topology | A full `N×N×horizon` response matrix. | SRC-007 explicitly rejects dense global inference in favour of sparse graph neighbourhoods. | `RESOLVED` | Neighbours and horizons learned. |
| `CONFLICT-014` Model complexity | Hawkes, Queue-Reactive, deep survival or GBDT could be treated as more correct because more sophisticated. | Simple empirical survival is initial Champion direction; complex models are shadow Challengers and need OOS calibration, EconomicLift and ModelValue. | `RESOLVED` | Exact Champion variant remains `OPEN-008/010`. |
| `CONFLICT-015` Runtime simulation | Participant-response research includes stochastic processes/agents, which could imply live simulation. | Participant hot path is incremental features + small inference; Monte Carlo belongs to Simulator. | `RESOLVED` | Runtime budgets calibrated. |
| `CONFLICT-016` Learning/evaluation | Random splits or live self-updating weights could appear convenient. | Temporal/walk-forward validation and offline train/approve/deploy are mandatory; no uncontrolled online self-learning. | `RESOLVED` | Window lengths and promotion gates calibrated. |

## Non-conflicts clarified

- Total edge-death hazard and cause-specific hazard coexist: overall hazard is the initial observable target; competing-risk decomposition is future/event-fidelity dependent.
- Locked interface and learned model are different statuses. QF-044/046/047/048 are locked definitions while hazard/arrival-edge/fill/response estimates remain learned.
- P0–P5 Participant fidelity and F0–F4 Simulator fidelity are independent axes.
- Event-level OFI and Snapshot OFI proxy are different feature contracts, not interchangeable implementations.
- A monitoring `RouteCompetitionScore` can coexist with direct Risk inputs, but Risk must not gate blindly on the score.

## Authority order applied

SRC-004 controlled formulas; SRC-005 controlled Risk/Data; SRC-006 controlled validation/activation; SRC-008 controlled counterfactual/simulation boundaries; SRC-007 supplied the detailed model design. Earlier sources were retained only where compatible.

## Remaining open decisions

No unresolved contradiction blocks documentation. Model parameters, exact Champion variants, maker strategy activation, cross-market neighbours/horizons, address feature activation and event-level feed availability remain evidence-dependent open or calibrated items.
