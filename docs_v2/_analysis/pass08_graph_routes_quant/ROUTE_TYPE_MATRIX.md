# Route Type Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Type | Input → terminal | Closed? | Comparator | Strategy/capital meaning | Formula family | Modes | Risk/accounting |
|---|---|---:|---|---|---|---|---|
| `DirectRoute` | A→B | No | itself/reference | executable direct conversion; OWA benchmark | QF-016/017 | T; maker use only where supported | current conversion cost/output |
| `Route2Leg` | A→X→B | No | context-dependent | structural path only; not automatically OWA | QF-016/018 | TT or MT | route execution exposure; classification required |
| OWA | A→X→B | No | **valid A→B required** | strategy advantage in terminal B | QF-017–020, QF-024/025 | TT/MT | Strategy/Route PnL; Capital still validates B |
| Bridge | A→…→B | No | not required | intentional capital relocation/future utility | QF-016, QF-068/070/072 | supported execution plan | Bridge/Relocation accounting, not OWA alpha |
| `Cycle3Leg` / Triangle | A→X→B→A | **Yes** | start amount/reference | closed-cycle arbitrage | QF-021–023 | TTT or MTT | Triangle/Strategy PnL |
| Recovery path | current unwanted X→… | goal-based | not an OWA comparator | risk-reducing response to existing exposure | QF-079/080 plus NetConvert | Recovery-owned | Recovery loss, constitutional priority |
| Cross-exchange route | venue-aware endpoints | varies | strategy-specific | `FUTURE`; disabled in V1 | future governed family | disabled | separate XEX/transfer risks |

Classification is semantic, never inferred from leg count. A three-leg open path is not a triangle; a multi-leg relocation may be a Bridge; Recovery is owned by the Execution/Recovery state machine.
