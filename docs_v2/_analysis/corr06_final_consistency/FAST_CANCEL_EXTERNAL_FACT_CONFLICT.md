# Fast-Cancel External-Fact Conflict

`RETRIEVED: 2026-09-09`

| Statement | Official source | Result |
|---|---|---|
| `cancel` and `cancelByCloid` support optional `f`/fast; trigger-order cancels reject `f:true`; omit `f` when false | [Exchange endpoint](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/exchange-endpoint) | VERIFIED |
| send cancels with fast; latency guide says no disadvantage except trigger-order limitation | [Optimizing latency](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/optimizing-latency) | VERIFIED GUIDANCE |
| current `f:true` has no other effect; a future upgrade is expected to prioritize only fast cancels | [Exchange endpoint](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/exchange-endpoint) | VERIFIED CURRENT ENDPOINT STATEMENT |

```text
FAST_CANCEL_SUPPORT: VERIFIED
FAST_CANCEL_RECOMMENDED_BY_LATENCY_GUIDE: VERIFIED
CURRENT_MEASURABLE_PRIORITIZATION_EFFECT:
DOC-SCOPE CONFLICT / REVALIDATION REQUIRED
```

The project neither invents an advantage nor removes the field. Adapter conformance may preserve the verified schema, while Simulator, capture metrics and economic comparisons assume no fast-specific latency improvement until primary sources converge or controlled current evidence is accepted. Trigger-cancel incompatibility remains safety relevant. This conflict blocks only claims/behavior that depend on a fast advantage; it does not weaken normal cancel priority, no-blind-retry or Reconciliation.
