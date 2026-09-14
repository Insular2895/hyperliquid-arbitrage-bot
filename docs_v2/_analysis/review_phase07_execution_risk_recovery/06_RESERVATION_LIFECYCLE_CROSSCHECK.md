# Reservation Lifecycle Crosscheck

Canonical order is validate → reserve → plan → intent → send. Actual fill consumes the used claim and creates actual exposure. Potentially live residual stays reserved; only exchange-proven terminal/reconciled unused quantity releases. `UNKNOWN` and `CANCEL_REQUESTED` lock. Replanning transfers/creates only the needed downstream claim against actual available inventory and never double-reserves V1 and V2.
