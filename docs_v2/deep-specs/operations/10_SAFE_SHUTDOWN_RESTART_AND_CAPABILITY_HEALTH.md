# 10 — Safe Shutdown, Restart and Capability Health

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Safe shutdown

Disable new risk; handle resting orders; resolve/bound active executions and Recovery; persist coherent journal/checkpoint/evidence; record unresolved exposure; release active ownership. Timeout or failed persistence escalates rather than reporting a clean stop.

## Restart

Every normal/forced/update restart begins non-ready. Validate artifact/config/owner/license, clock/feed/books/account/open orders/fills, reconstruct checkpoint+journal, reconcile exchange truth and recompute Risk/capability. A stored readiness flag has no authority.

## Capability health

Current permission is the intersection of implementation/config/license/channel/validated scope/readiness/Risk. Health can be scoped by market, mode, model, size and infrastructure. Demotion preserves safe cancel/reconcile/Recovery and evidence paths.

## Resume

Health recovery clears only the failed current-state gate. If an incident, drift or material change invalidated evidence, affected maturity remains demoted until required Unit/Replay/Shadow/Micro-live proof and explicit re-promotion. Operations cannot grant capital through a dashboard or manual force flag.
