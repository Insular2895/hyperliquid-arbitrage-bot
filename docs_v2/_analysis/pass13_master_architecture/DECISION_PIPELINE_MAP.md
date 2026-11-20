# Decision Pipeline Map

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

```mermaid
flowchart TD
  S["Coherent Book + Metadata + Fee + Precision versions"] --> AR["affected RouteDefinitions via pair_to_routes"]
  AR --> CE{"cheap reject-only eligibility/BBO/freshness"}
  CE -->|reject| RJ["typed RejectEpisode"]
  CE -->|continue| NC["NetConvert(q) exact L2 over bounded q grid"]
  NC --> CL["OWA direct comparator / Triangle / conversion classification"]
  CL --> R0{"current canonical market/account/resource eligibility and cheap preliminary hard Risk screen"}
  R0 -->|deny| RJ
  R0 -->|safe candidate domain| F["required bounded FeatureSnapshot"]
  F --> MD{"exact capability requires promoted Participant or configured Simulator input"}
  MD -->|documented conservative baseline| TV["projected actual-state Terminal Viability"]
  MD -->|required| MF["resolve supported promoted Participant forecasts"]
  MF --> MS{"artifact support OOD freshness and capability scope valid"}
  MS -->|no| RJ
  MS -->|yes| SF["configured supported F0/F1/F2/F3 ExecutionForecast"]
  SF --> TV
  TV --> EV["RAEV + P+ + ES/CVaR + confidence/support"]
  EV --> SZ["feasible size curve: all gates incl. Q_validated"]
  SZ --> PA["optional joint Portfolio allocation"]
  PA --> R1["Risk T1 pre-reservation"]
  R1 -->|deny| RJ
  R1 --> RV["atomic balance/book/risk reservations"]
  RV --> EP["immutable ExecutionPlan"]
  EP --> R2["Risk T2 current-version pre-send"]
  R2 -->|deny| REL["release/contain by observed reservation rules"]
  R2 --> FX["mode-authorized Transport effect"]
```

Data interfaces: `BookSnapshot`/rule snapshots → `RouteEconomics` → Opportunity/RejectEpisode → Feature/Model forecasts → `ExecutionForecast` → viability/size/allocation proposal → `RiskDecision` → `ReservationState` → `ExecutionPlan`.

Ordering resolution: Risk is staged, not a single terminal function. Current canonical eligibility
and the constitutional/cheap screen happen before an expensive optional model invocation becomes a
required predecessor. Required bounded features may be incrementally available and independent
pure calculations may overlap; the diagram fixes dependencies and authorization, not one synchronous
scheduler. A capability that requires an unavailable/unsupported model rejects, while the documented
conservative baseline follows its own support envelope. Exact candidate/tail/size checks happen
before reservation; the immutable plan follows the committed claims; T2 is immediate pre-send;
T3–T5 revalidate after fills, before later legs and while a maker order rests. No later stage can
restore an action removed from `A_safe`.

Basic Opportunity + conservative models/F0/F1 + zero/limited q are final-interface-compatible bootstrap baselines.
