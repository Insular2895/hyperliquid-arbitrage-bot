# Incident Evidence Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

An `IncidentId` groups related domain events into one operational object. Source-backed `IncidentRecord` fields are incident ID, severity, affected markets/executions, start, optional end, triggers, actions and optional resolution. It is not merely an error-log entry.

The incident package contains:

- sanitized IncidentRecord, alert/ack/escalation and operator/control timeline;
- RunManifest, build/image digest, dependency locks, ResolvedConfig hash, capability/release/model/formula/schema identities;
- RAW chunk manifests/checksums and normalized data/quality regions for a calibrated pre/post window;
- ordered market, account, order, fill, timer, infra and control events with receive/source times and clock health;
- state versions/snapshots/hashes, opportunities/rejects/decisions/plans/intents/journal/reservations;
- exchange orders/fills/fees, inventory/account reconciliation, Recovery and component/global PnL;
- predicted/actual model/simulator/execution records, latency traces, relevant metrics/logs and runbook steps;
- original reproduction, candidate counterfactual manifest, deviations, root cause, remediation, owners and revalidation decision.

Timeline order uses recorder sequence/canonical event order; source and receive timestamps plus uncertainty are retained. Conflicting clocks are evidence, not silently repaired.

Secrets, seeds, tokens, raw environment dumps, unnecessary wallet/account identifiers, memory/core dumps and unrelated order/balance history are excluded. Local allowlisting, denylist/entropy/canary checks and an inclusion manifest fail closed before explicit client export. Material evidence remains available locally for reconstruction.

An incident may demote M5 immediately. Resume requires containment, current exchange reconciliation, verified fix/rollback, affected test/Replay evidence, Shadow/Micro-live when assumptions changed, and explicit scoped re-promotion.
