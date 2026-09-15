# Capability Size Scope and Q_validated

`size_range` is a coarse manifest envelope. Documentary `ValidatedQSet` is the exact evidenced support and may be non-monotonic; QF-076's scalar `Q_validated` is its supremum/boundary, while runtime evaluates current `Gates(q)` for every selected q.

| q | In envelope 0..200 | Evidence support | Current gates | New risk |
|---:|---:|---:|---:|---:|
| 100 | yes | yes | pass | allowed only if every other permission intersects |
| 150 | yes | no | fail | rejected |
| 200 | yes | yes | pass | allowed only if every other permission intersects |
| 250 | no | yes | pass | rejected |

No schema field is redefined. Exact support, evidence and restrictions remain linked artifacts.
