# 11 — Failure Containment and Degradation Architecture

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

Failure makes the system less active. New risk fails closed; safe cancel, evidence preservation, bounded Recovery, Reconciliation and shutdown remain when their inputs are valid.

Containment uses the narrowest proven-safe scope: Global, Venue, Market, Route, Strategy, Execution Mode, Model, Infrastructure or Client Deployment. Stale Book/unknown rules disable affected routes; model OOD falls back or shrinks model-dependent scope; UNKNOWN order locks its resources; account/reconciliation uncertainty can widen to the account; split brain or signer compromise halts the client context.

Detection and permission are separate: Book/Model/Infrastructure/License components emit typed health facts; Risk maps them to allowed action classes; Execution enforces; Operations alerts and preserves evidence. A component cannot clear its own safety consequence by reporting one healthy sample.

Recovery to a wider scope requires sustained valid evidence, any necessary reconciliation, fix/rollback verification and explicit capability revalidation. Cleared alerts do not restore maturity. The canonical per-failure matrix is [FAILURE_CONTAINMENT_MATRIX.md](../../_analysis/pass13_master_architecture/FAILURE_CONTAINMENT_MATRIX.md).

Challenger/speculative feed failure is isolated from canonical authority; shared CPU/disk/network pressure that harms canonical state or P0/P1 evidence escalates through existing Infra/Risk scopes. Canonical source lag/gap/mismatch forbids affected new risk. Feed-profile fallback is a controlled rebuild/readiness/reconciliation transition, never last-arrival-wins fusion.
