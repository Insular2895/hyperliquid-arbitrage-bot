# Authorization Layer Audit

| Layer transition | Separate record required | Current result |
|---|---:|---|
| exact F package complete → documentation approved | yes | PENDING — currently decision-eligible |
| documentation approved → switchover authorized from exact F | yes | NOT_AVAILABLE — documentation not approved |
| switchover authorized → Commit B generated/validated/accepted | yes | NOT_AVAILABLE — authorization absent; B absent |
| Commit B accepted → Phase 1 authorized | yes | NOT_AVAILABLE — B absent/unaccepted |
| Phase 1 exit → Phase 2 authorized | yes | NOT_STARTED for Phase 1 / NOT_AVAILABLE for Gate G |
| implementation → capital permission | yes plus runtime intersection | NOT_AUTHORIZED |

`PENDING` is used only when the decision is eligible now; unmet prerequisites yield `NOT_AVAILABLE`, and unbegun execution/evidence yields `NOT_STARTED`. No blanket HDC approval, fixed human-family count, fixed invariant count or transitive authorization remains.

Exact F commit/tree identity is supplied externally by the human DecisionRecord. Moving HEAD is not authority, and F never self-embeds its own SHA.
