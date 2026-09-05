# 06 — Runbooks: Feed, Account, Order, Crash and Recovery

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Feed/Book desync

Stop affected new risk; pin sequence/timing/clock evidence; reconnect/resubscribe; fetch a valid snapshot; apply ordered deltas; rebuild books/features/routes; reconcile affected decisions/orders; demand sustained health before readiness.

## Account unreconciled / Unknown order

Lock reservations/capital; never blind resend. Query CLOID/OID/open orders/status, fills and balances; deduplicate/apply fills; classify terminal/remainder state; reconcile reservations/inventory. Ambiguity remains `UNRESOLVED` and blocks affected new risk.

## Cancel race / Recovery failure

Apply actual fill truth even during cancel; resolve remainder and accounting. Recovery failure stops new risk, preserves current exposure/path evidence and escalates. Only a proven bounded exit or explicit controlled hold ends the runbook.

## Crash/reboot

Start non-ready; establish one owner; verify artifact/config/clock/feed; combine checkpoint, journal and exchange queries; reconstruct executions/recovery/account/inventory; reconcile and then run readiness. No persisted READY or presumed clean signal is trusted.

Every runbook attaches an IncidentId for P0/P1, records automated/human actions and ends with explicit verification/evidence.
