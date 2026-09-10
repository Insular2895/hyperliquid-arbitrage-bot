# Async Effect Executor Contract

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

The Effect Executor performs environment-specific external work. It never mutates canonical state or interprets a response as a state transition. Every result—including timeout, disconnect and parse failure—re-enters the ordered boundary as a normalized event with the originating intent/effect identity.

| Effect | Request authority | Async executor responsibility | Return evidence | Ambiguity/failure |
|---|---|---|---|---|
| `SubmitOrder` | Execution after current Risk/Reservation/intent/signing | transmit exact immutable request | accepted/rejected/transport observation | possible transmission → `UNKNOWN`; no blind retry |
| `CancelOrder` | Execution/Recovery safety action | transmit cancel | confirmed/rejected/timeout/status | `CancelRequested != Canceled`; racing fill remains valid |
| `QueryOrder` | Execution/Reconciliation | fetch exact identity/status | as-of status observation | unresolved remains UNKNOWN |
| `FetchOpenOrders` | Reconciliation | account query | ordered snapshot observation | NON-READY on unresolved failure |
| `FetchFills` | Reconciliation | paginated/cursor query | fill observations + cursor evidence | dedupe in C0 by FillId |
| `FetchBalances` | Reconciliation | account query | balance snapshot observation | cannot erase prior order/fill evidence |
| feed/metadata subscribe | adapter owner | connect/subscribe/reconnect | payload/connection/gap event | Book/rule scope invalidates/resyncs |
| archive upload | Recorder background | upload verified closed artifact | archive/verification result | local pending/retry; no Core dependency |
| license refresh | Licensing background | obtain signed entitlement | license observation | blocks new commercial risk only by policy |
| release/update check | Deployment background | fetch signed metadata | candidate/failure observation | retain current release; no auto update |
| local admin effect | authenticated control owner | execute bounded external/control action | ControlEvent/result | cannot write state directly |

## Executor invariants

- Effect queues are bounded; cancels, account/fill truth and reconciliation safety work outrank new optional submissions.
- The ordered coordinator never awaits network completion. It records the intention, advances only to the correct pending state and continues consuming safety/account events.
- ACK is not fill. Send return is not acceptance unless the transport contract provides that exact evidence. Cancel response is interpreted only by the ESM.
- Retries are effect/state-machine specific, idempotency-aware and evidence-preserving; generic retry middleware cannot duplicate capital effects.
- Executor shutdown stops new risk-increasing work first and preserves bounded safety/query work according to the shutdown contract.
