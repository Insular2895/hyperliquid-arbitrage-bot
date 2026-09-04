# 07 — Participant Signatures and Address Behaviour

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Status

Address/behaviour features are optional `P4`, Research/Future and external-dependent. Initial production does not depend on them. Aggregate survival and response remain primary even if public trade records expose pseudonymous counterparties.

## Address is not identity

One entity may use multiple wallets, subaccounts, vaults or API wallets; one address may run multiple strategies. Therefore:

```text
ParticipantAddress != proven person, firm, owner or strategy
BehaviourCluster != proven common owner
```

Permitted output describes observations and statistical similarity. Names such as a specific firm or “the market maker behind this wallet” are forbidden without independent proof and explicit legal/privacy review.

## Passive AddressBehaviourSignature

If current feed fields and legal/data policy permit, passive trade observations may derive:

- markets traded and market-transition graph;
- frequency, inter-trade time and burstiness;
- median/quantile size and buy/sell symmetry;
- time-of-day/regime activity;
- reaction to defined anomalies, large trades, spread changes and cross-market moves;
- `ReactionDelay(address,event)` distributions.

The model does not poll positions, balances, open orders or full history for every observed address. Mass per-address API enrichment is out of scope and can be costly, rate-limit intensive and privacy-expansive.

## FastCorrectionSignature

For a precisely labelled opportunity born at `t0`, a pseudonymous address or behavioural cluster can be associated with repeated corrective trades after a measured delay. A signature may include reaction-delay distribution, affected markets, size distribution, edge threshold and activity regime.

The usable feature is a conditional probability such as `P(fast competitor activity | X)`, not the claim that the address uses our algorithm. `first_corrective_trade`, `first_corrective_book_change`, 50% decay and death labels require causality-safe language.

## Clustering

Research may cluster signatures by markets, delays, sizes, sequences, time patterns and transitions. Similarity method, stability, sample support and cluster version must be recorded. Cluster IDs are ephemeral model constructs; changes across retraining are expected and must not silently join historical identities.

## Activation gate

Address features enter a production challenger only if they provide material, stable, incremental temporal OOS predictive lift over the aggregate model, improve or preserve calibration and EconomicLift/ModelValue, and pass OOD/privacy/runtime/fallback tests. Minor in-sample metric gains are insufficient.

The challenger first runs shadow-only. Model failure or absent address fields falls back to aggregate features without blocking capabilities that do not require P4.

## Data minimization and provenance

- revalidate current availability, semantics and completeness of counterparty fields before dependency;
- record source, event/trade ID, timestamp semantics and feed version;
- hash or pseudonymize addresses in analytical datasets when exact values are unnecessary;
- restrict retention/access and do not present public pseudonyms as personal data conclusions;
- do not perform unsupported deanonymization or combine external datasets without explicit authorization and governance;
- keep identity assertions out of model labels, UI and logs.

## Validation

- temporal split preventing an address's future behaviour leaking into past features;
- new-address and sparse-address OOD tests;
- cluster stability and ablation versus aggregate model;
- calibration/lift by market, regime and activity support;
- privacy leakage and log/export tests;
- runtime/storage and fallback-to-aggregate tests;
- micro-live observation only after passive/shadow evidence, with no identity claim.

## External revalidation

SRC-007 states that the public trades feed exposed buyer/seller addresses at the time of research. PASS 02 preserves this as a source snapshot and does not assert it is current. Field availability/semantics and applicable privacy/legal obligations must be revalidated before collection or product use.

## Sources

SRC-007 address behaviour, clustering and activation sections; SRC-005 Data/Risk; SRC-006 validation governance; EXT-005 in the external revalidation register.
