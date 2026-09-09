# Risk Permission versus Economic Score

Economic scores rank or size candidates only inside existing authority. Risk hard gates remain Boolean permission predicates with current state, scope, TTL and reason codes. They are not converted into finite monetary penalties because a sufficiently high modeled EV could then buy through a constitutional prohibition.

| Condition | Economic score | Risk decision | Action |
|---|---:|---|---|
| positive RAEV, gate denied | any | deny | no new risk |
| negative RAEV, gates allowed | negative | allow-capable only | economic layer rejects/skips |
| OOD/no support | unavailable | fail closed or narrower fallback | no unsupported q |
| all gates and economics valid | positive | allow within scope | Execution may attempt under plan |

CORR-05 adds zero hard gates and zero `p_full` thresholds.
