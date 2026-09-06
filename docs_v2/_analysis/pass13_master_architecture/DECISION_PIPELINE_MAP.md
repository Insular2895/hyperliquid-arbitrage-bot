# Decision Pipeline Map

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

```mermaid
flowchart TD
  S[Coherent Book + Metadata + Fee + Precision versions] --> AR[affected RouteDefinitions via pair_to_routes]
  AR --> CE{cheap reject-only eligibility/BBO/freshness}
  CE -->|reject| RJ[typed RejectEpisode]
  CE -->|continue| NC[NetConvert(q) exact L2 over bounded q grid]
  NC --> CL[OWA direct comparator / Triangle / conversion classification]
  CL --> F[required FeatureSnapshot]
  F --> MF[optional promoted Participant forecasts]
  MF --> SF[configured F0/F1/F2/F3 ExecutionForecast]
  SF --> TV[projected actual-state Terminal Viability]
  TV --> EV[RAEV + P+ + ES/CVaR + confidence/support]
  EV --> SZ[feasible size curve: all gates incl. Q_validated]
  SZ --> PA[optional joint Portfolio allocation]
  PA --> R1[Risk T1 pre-reservation]
  R1 -->|deny| RJ
  R1 --> RV[atomic balance/book/risk reservations]
  RV --> R2[Risk T2 current-version pre-send]
  R2 -->|deny| REL[release/contain by observed reservation rules]
  R2 --> EP[immutable ExecutionPlan]
```

Data interfaces: `BookSnapshot`/rule snapshots → `RouteEconomics` → Opportunity/RejectEpisode → Feature/Model forecasts → `ExecutionForecast` → viability/size/allocation proposal → `RiskDecision` → `ReservationState` → `ExecutionPlan`.

Ordering resolution: Risk is staged, not a single terminal function. Constitutional/cheap eligibility happens before expensive inference; exact candidate/tail/size checks happen before reservation; T2 is immediate pre-send; T3–T5 revalidate after fills, before later legs and while a maker order rests. No later stage can restore an action removed from `A_safe`.

Basic Opportunity + conservative models/F0/F1 + zero/limited q are final-interface-compatible bootstrap baselines.
