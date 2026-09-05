# Sizing vs Slicing Boundary

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Boundary | Position Sizing | Order Slicing |
|---|---|---|
| Question | Total exposure? | Child timing/order shape? |
| Input quantity | candidate grid | already approved `q*` |
| Output | `q* <= Q_validated` | children with total `<= q*` |
| Optimizes | RAEV inside hard feasible set | execution quality under edge decay/response |
| May raise exposure? | only through fresh validation | never |
| Capacity ownership | consumes available/shared capacity | uses same reservation, cannot create more |
| Failure | q*=0/reject | cancel/replan/revalidate/Recovery |

TT, MT, TTT and MTT use separate size distributions and then separate slicing mechanics. Same-time fragmentation cannot claim new depth; temporal slicing needs Replay/Shadow/Micro-live evidence after replenishment, survival and competition. The 40–50 EUR probe is validation, not either module's universal production rule.
