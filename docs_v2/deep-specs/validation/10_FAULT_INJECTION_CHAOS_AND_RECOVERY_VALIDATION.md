# 10 — Fault Injection, Chaos and Recovery Validation

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

For every meaningful dependency, test stopped/unavailable, late, stale, corrupt/lying, duplicate, reordered, overloaded and OOD behavior. Cover feed/book/account/order/fill, lost submit response, cancel race, crash at every persistence/effect boundary, Recovery crash/failure, balance/reservation mismatch, models/Simulator, clock/CPU/memory/disk/Recorder/network, signer/license/config/schema, update/migration, ownership and exchange-rule change.

Each scenario specifies injection, pre-exposure state, expected engine/Risk/capability states, allowed/prohibited effects, accounting/reservation result, alerts/runbook/escalation, evidence, recovery criteria and post-recovery reconciliation. Success requires the expected safe economic result, not merely continued process operation.

Chaos combines failures only after single-fault behavior is proven and with bounded blast radius. Live fault work uses the minimum authorized scope and stop controls. It must never become an excuse for uncontrolled production experiments.

Recovery is valid only when current exchange orders/fills/balances, local journal/checkpoint, inventory/reservations and ownership reconcile. Unresolved state remains locked and prevents affected new risk.
