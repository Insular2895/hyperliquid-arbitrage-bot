# RiskDecision `allowed` / `action` Contract

| action | `allowed` source value | semantic rule |
|---|---|---|
| `ALLOW` | OPEN exact mapping | new-risk eligibility subject to every gate |
| `ALLOW_REDUCED_SIZE` | OPEN exact mapping | same, capped |
| `ALLOW_RECOVERY_ONLY` | OPEN — source recheck required | never normal new risk; Recovery context still mandatory |
| `REJECT`, `HALT_*` | OPEN exact mapping | cannot authorize scoped economic effect |

SRC-005 fixes both frozen fields and the seven actions but no complete Boolean truth table. `action` is semantic authority; no consumer reads `allowed` alone. Any contradictory or unresolved pair is invalid/fail-closed. Replay preserves the original pair and validation result. No schema expansion or migration occurs.
