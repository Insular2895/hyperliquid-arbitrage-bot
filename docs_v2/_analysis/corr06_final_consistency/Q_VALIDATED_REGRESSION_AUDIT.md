# Q_validated Regression Audit

All required separations pass:

- QF-027 profitable size is not QF-076 validated capacity.
- balance, visible book depth and hard Risk limit are not `Q_validated`.
- more capital, slicing, high `p_full` or positive EV cannot enlarge validated evidence.
- small-q validation does not transfer to large q.
- `Q_validated` remains q/state/market/route/mode/version/evidence/model-support/operations scoped.
- stale InfraProfile or unvalidated priority policy cannot expand it.

Regression count: `0`. Any change requires the existing evidence, Risk and human promotion gates.
