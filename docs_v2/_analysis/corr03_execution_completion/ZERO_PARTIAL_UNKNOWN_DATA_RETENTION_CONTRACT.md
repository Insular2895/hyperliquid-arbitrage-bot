# CORR-03 — Zero / Partial / UNKNOWN Data Retention

DOCUMENTATION STATUS: MANDATORY EVIDENCE CONTRACT

The calibration dataset is a derived view of canonical journal/events, never a second mutable fill ledger. It retains all real attempts, including known zero fills, partial fills, later-leg rejects, exchange rejects, cancel races, `UNKNOWN`, Recovery, Recovery failure, negative PnL, residual exposure and safe no-exposure terminals. Success-only, completed-only, filled-only or profitable-only datasets are invalid.

| Evidence class | Minimum retained facts |
|---|---|
| zero fill | Execution/Opportunity IDs, route/mode, requested q/price protection, decision book+forecast+versions, possible-send/ACK/status timing, authoritative zero proof, reservation reconciliation/release, economic result and reason |
| partial fill | requested/filled q, continuous fill ratio, unique fills, VWAP/fees/deltas, first/last-fill times, current downstream q, new book/edge/Risk decision, continuation/Recovery split and final resolution |
| `UNKNOWN` | last known order state, possible-send time, CLOID/OID, every query/result, fills discovered, lock duration/scope, time/final truth, reconciliation and Recovery linkage |
| Recovery | origin/Recovery IDs, trigger, actual exposure and books at start, candidate/selected plans, Risk decisions, intents/fills/cost/loss/attempts, final inventory/state/reconciliation |

Missing, unresolved, invalid and not-applicable are distinct from numeric zero. Evidence retention obeys existing security/redaction/retention governance; low-level detail belongs in trace/dataset storage, not metric labels.
