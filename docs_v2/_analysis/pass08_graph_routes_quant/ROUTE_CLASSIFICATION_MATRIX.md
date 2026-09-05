# Route Classification Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Structure/context | Classification | Required proof | If proof absent | Owner |
|---|---|---|---|---|
| A→B | Direct | valid directed market, current executable state | unavailable/invalid route | Routing |
| A→X→B with valid A→B comparator | OWA candidate | same q, input, terminal unit, conventions and coherent versions | not OWA | Routing/OWA |
| A→X→B without valid A→B comparator | Bridge / Capital Relocation candidate | terminal viability and relocation utility | STAY/no action | Capital/Bridge |
| A→X→B→A | Triangle candidate | exact closure in starting asset and sequential outputs | ordinary/open path, not Triangle | Routing/Triangle |
| A→…→B for future utility | Bridge | relocation purpose plus PASS07 gates | STAY | Capital/Bridge |
| Existing unwanted X→… | Recovery path | existing exposure and safe-loss objective | hold/other bounded recovery | Execution/Recovery |

An OWA label must be carried explicitly by the opportunity. Accounting must not reconstruct it from `legs.len()`. If the direct market becomes unavailable, the indirect route loses OWA status; it may be reconsidered as Bridge only through PASS07. A failed intentional Bridge becomes actual Recovery input; sunk intent does not preserve its old class.
