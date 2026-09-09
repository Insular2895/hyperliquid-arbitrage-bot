# Probability Event Tree

```text
E0 opportunity
├─ E1 survives arrival
│  ├─ not attempted (policy/Risk/capital/expiry)
│  └─ E2 attempt
│     ├─ F: E4 full route, actual fills, no Recovery
│     ├─ P: noncomplete, E3 any strategy fill, no Recovery
│     ├─ R: noncomplete, E5 Recovery entered
│     │  ├─ E6 recovered operationally
│     │  └─ Recovery failed/residual exposure
│     └─ X: resolved zero-fill, no Recovery
└─ does not survive arrival
   ├─ not attempted
   └─ only if a separately specified policy still attempts

Each resolved branch -> E7 reconciliation -> E8 economic result -> E9 positive or non-positive PnL
```

QF-048/QF-085 model E1 from E0. `ROUTE_OUTCOME_RESOLVED_V1` models F/P/R/X conditional on E2 and its frozen supported candidate. QF-059 is the E9 probability derived from the same PnL distribution. A factored `P(E1|E0) × P(F|E2,...)` is not automatically a joint probability because the second factor's selection and conditioning may already encode survival.
