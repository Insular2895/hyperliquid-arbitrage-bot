# Model Support and Validated-Capacity Contract

`Q_validated` requires model support for the economic distribution at the evaluated q/state. QF-102 disagreement, QF-103 OOD and QF-104 confidence are evidence/governance signals, not PnL cashflows.

| Model state | Capacity effect | Economic behavior |
|---|---|---|
| supported/promoted | eligible for remaining gates | consume versioned distribution |
| supported fallback | only within fallback's explicit domain | use fallback distribution and confidence |
| OOD/insufficient support | q excluded or capacity contracted | no favorable extrapolation |
| unavailable/invalid | no decision authority | fail closed for new risk |

Model demotion activates only a declared, versioned fallback. It may reduce capacity to zero or a narrower domain; it never silently preserves the prior capacity.
