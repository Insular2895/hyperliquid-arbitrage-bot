# 02 — Feature Registry

STATUS: FUTURE SPECIFIED / NOT ACTIVE

`FeatureSpec` is a versioned, point-in-time contract for a research input. It does not grant production use.

Required fields: stable feature ID and version; name/meaning; economic rationale; definition and units; owner; source fields and schema versions; event time, receive time and provable availability at decision time; lookback; transformation/normalization; missingness; warm-up; validity/quality; support; known leakage risks; mode/fidelity; code/build hash; validation evidence; consumers; maturity; deprecation/supersession lineage.

Maturity is one of:

- `PROPOSED`: hypothesis only;
- `IMPLEMENTED_OFFLINE`: reproducible extraction, not validated;
- `POINT_IN_TIME_VALIDATED`: no-lookahead and availability proof;
- `OOS_VALIDATED`: temporal OOS evidence for declared scope;
- `SHADOW_ELIGIBLE`: explicit review permits Shadow consumption;
- `PRODUCTION_ELIGIBLE`: separately promoted artifact, still subordinate to Risk and scope;
- `DEPRECATED` or `INVALID`.

For each row, the value at decision time must be reconstructible using only information available before the applicable decision freeze point. Revised, future, reconciled or label-derived values cannot leak backward. Dataset construction preserves event time, receive time, source sequence, clock quality and missingness.

Feature families and interactions must have an explicit hypothesis. A large feature inventory is not evidence. Features with unstable support, high missingness, regime-confounded behavior or unresolved provenance remain unavailable or fall back according to a declared policy; zero is not a generic missing value.

Feature computation may reuse canonical Book, `NetConvert`, Participant, InfraProfile and outcome evidence, but cannot redefine their authority. Any material source/schema/exchange change invalidates or revalidates affected feature versions through the external-fact and drift workflow.

## Research universe and progression

Candidate families may cover timing/lead-lag and Opportunity age/lifetime; direct-versus-route incoherence; q/depth/spread/slippage; imbalance/OFI/microprice; volatility/jumps; liquidity withdrawal/refill and maker cancellation/replacement; zero/partial/full/Recovery behavior; route/market/asset/time regimes; participant/survival response; infrastructure latency/jitter/priority; inventory/capital competition; support/OOD and drift. This is a research universe, never a mandatory Live feature list.

Analyze simple supported relationships first—such as completion by q/age/route/regime or slippage by q/depth—then add economically motivated interactions. The forbidden primary method is “hundreds of features -> opaque optimizer/AI -> best backtest -> Live.” Representative calm, volatile, thin, opportunity-rich, low-opportunity, failure-rich, incident and infrastructure-period datasets may be retained as regression evidence, not tuned as the only proof.
