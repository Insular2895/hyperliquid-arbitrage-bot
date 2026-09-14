# ExecutionPlan Actual-Fill Versioning

V1 plans 1000 USDC → expected 20 HYPE and a second leg taking 20 HYPE. An actual unique fill yields 13.7 HYPE. The FillLedger, Account, Inventory and used Reservation update immediately; V1 stays immutable. Current state/economics/forecast and T3/T4 Risk are recomputed. If 13.7 changes an executable field, V2 is mandatory, linked by existing execution/evidence lineage and `plan_version`, with current Risk and reservation ownership. Only after T2/current pre-send checks may a new intent use the quantized actual available amount. No frozen field is added.
