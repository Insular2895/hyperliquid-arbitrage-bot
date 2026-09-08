# Event Coalescing Safety Analysis

DOCUMENTATION STATUS: DEFAULT PROHIBITED — HUMAN REVIEW REQUIRED FOR EXCEPTION

Default rule: do not coalesce distinct market events or ordered book states before canonical processing/evaluation. Two states with the same final BBO may contain a transient route opportunity, validity transition, sequence gap or evidence needed by Replay and CORR-01 denominators.

Any future coalescing proposal is a semantic performance policy and must define:

- exact event class, scope, horizon and priority;
- states/evidence guaranteed not to be lost;
- interaction with book reconstruction, gaps and resync;
- effect on `OpportunityId`, episodes, funnel denominators and latency;
- scheduling/config version and `DecisionTrace` representation;
- deterministic Replay baseline versus coalesced mode;
- Shadow capture/economic comparison, starvation/fairness and fail-safe disablement;
- explicit human approval.

Account events, fills, order status, reservations, Risk, execution, Recovery, reconciliation and accounting evidence are never coalescing candidates. A latest-value view may support display or C4 scheduling, never replace ordered economic truth.
