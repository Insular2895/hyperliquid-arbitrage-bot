# 02 — NetFlow, Capital Reachability and Terminal Viability

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## NetFlow

QF-067 aggregates actual inventory deltas over window `W`. Multiple calibrated horizons expose directional accumulation while stock remains inside a band. The offline reference and live rolling result must agree. NetFlow may decrease size or economic rank before a hard limit; Risk retains final permission.

## Inventory Graph and reachability

The economic Inventory Graph answers:

- where actual/available capital is located;
- what structural routes are point-in-time available;
- what routes are reachable using current capital;
- which reachable routes are Risk-eligible and size-supported;
- what terminal/exit states would become reachable after an action.

Do not equate structural route count, capital-reachable routes and validated active routes. Capital Reachability includes conversion cost, time, reservations, terminal state and exitability. PASS08 owns Market Graph structure, route identity, Atlas and HOT/WARM/COLD; this spec only declares their consumer interface.

## Terminal Viability gate

| Dimension | Required evidence | Failure effect |
|---|---|---|
| Hard inventory | Post-action state passes QF-066 | Hard reject except strict Risk reduction |
| Soft inventory | Deviation/penalty at candidate quantity | Rank/size adjustment |
| Classification | Terminal is allowed for intentional holding | Reject invalid terminal |
| Exit path | At least one currently permitted credible exit | Reject or unsupported |
| Exit cost | QF-068 at candidate quantity | Include in economics |
| Liquidity | Supported executable exit capacity | Reject/downsize/OOD |
| Stranded risk | Exit, idle and risk components | Penalty/reject under Risk limit |
| Future utility | Point-in-time validated opportunity evidence | Relocation comparison input |
| Confidence/OOD | Model/data support at size and horizon | Reduce/reject |

An OWA with positive Conversion Alpha can fail Terminal Viability. `A -> X -> B` is evaluated at B after candidate execution, not at current inventory alone. Transit X remains actual exposure if the second leg fails.

## Point-in-time contract

Historical relocation/terminal decisions use only the Atlas, routes, classifications, books, inventory, models and forecasts available then. Today's complete history cannot replace the state known at decision time. Each evaluation stores relevant versions and source timestamps.

Sources: SRC-002 inventory graph/capital-location sections; SRC-003 §§15–30; SRC-004 QF-066–069; SRC-005 §§67–74/Data §§155–159. PASS08 owns topology and Atlas semantics.
