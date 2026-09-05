# Position Sizing Constraint Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Constraint | Hard? | Soft objective? | Formula | Owner | Calibrated? | Learned? | Reduce size? | Reject? | Source |
|---|---:|---:|---|---|---:|---:|---:|---:|---|
| Capital | ceiling | no | QF-073 | Capital/Execution | no | state | yes | yes if unavailable | SRC-004/005 |
| Available balance | yes | no | QF-073 | Execution/Data | no | state | yes | yes | SRC-004 |
| Book capacity | yes | no | QF-074 | Market/Execution | no structure | state | yes | yes | SRC-004 |
| `Q_validated` | yes | no | QF-076 | Sizing/Validation | gate values | yes | yes | yes | SRC-004/006 |
| Risk max | yes | no | Risk policy | Risk | yes | sometimes | yes if independently valid | yes | SRC-005 |
| Hard inventory | yes | no | QF-066 | Risk | bounds | state | yes only inside band | yes | SRC-004/005 |
| Soft inventory | no | yes | QF-064/065 | Inventory | yes | state | yes | not alone | SRC-004 |
| Impact | yes limit | objective input | QF-042 | Risk/Simulator | limit | model/state | yes | yes | SRC-004/005 |
| Volume participation | yes limit | no | QF-041 | Risk | limit/window | state | yes | yes | SRC-004/005 |
| P>0 | yes threshold | objective evidence | QF-059 | Risk/Simulator | threshold | distribution | yes | yes | SRC-004 |
| CVaR / ES | yes limit | risk objective | QF-062 | Risk/Simulator | alpha/limit | distribution | yes | yes | SRC-004 |
| SimulationConfidence | yes minimum where required | uncertainty term | QF-104 interface | Simulator/Risk | gate | learned | yes if supported | yes/OOD | SRC-004/006 |
| Strategy capability | yes | no | capability policy | Risk/Validation | policy | evidence | yes | yes | PASS02–06 |
| Execution mode | yes | affects RAEV | mode contract | Execution/Simulator | activation | learned | yes | yes | PASS02–04 |
| Shared capacity | yes | portfolio interaction | QF-078 constraints | Portfolio/Execution | limits | state | yes | yes | SRC-003/004 |

Final quantity is optimized only inside the intersection of all applicable hard constraints.
