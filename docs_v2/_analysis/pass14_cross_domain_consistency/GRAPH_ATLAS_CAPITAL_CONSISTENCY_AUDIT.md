# Graph–Atlas–Capital Consistency Audit

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Concept | Owner | Meaning | Must not mutate/claim | Result |
|---|---|---|---|---|
| structural Graph | Graph | venue-aware nodes and possible directed conversions | profitability, current book, inventory | PASS |
| route definitions | Route Engine | fixed ordered Direct/Route2/Cycle3 and dependencies | opportunity, execution outcome | PASS |
| `pair_to_routes` | Route Engine | affected-route reverse index including OWA comparator | global tick-time search | PASS |
| Opportunity | Opportunity Engine | current q-specific executable economics | capital permission | PASS |
| Market Atlas | Atlas | rolling point-in-time economic evidence | current exchange truth or topology | PASS |
| HWC | Watcher/Activation | reversible compute/relevance allocation | safety/permission | PASS |
| Capital Reachability | Capital | usable paths from actual available inventory | structural existence | PASS |
| Terminal Viability | Inventory/Capital | acceptable future inventory/exit/stranded state | route legality | PASS |
| Bridge | Inventory/Capital | relocation versus STAY | OWA or Recovery | PASS |
| `Q_validated` | Validation/Risk/Sizing boundary | all-gates supported size | visible depth/balance/QF-027 | PASS |

Capital and HOT state may change route activation, never topology. Atlas consumes historical capital/outcome evidence and emits a later `AtlasVersion`; a current decision pins one version, eliminating call recursion and lookahead. `OPEN-016` retains exact HWC/Atlas/support thresholds. Conflations found after fix: **0**.
