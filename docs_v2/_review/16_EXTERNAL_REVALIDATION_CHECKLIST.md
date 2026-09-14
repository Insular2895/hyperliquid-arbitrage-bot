# External Revalidation Checklist

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Purpose and authority

This checklist indexes changing external facts from the canonical [External Revalidation Register](../_analysis/EXTERNAL_REVALIDATION_REGISTER.md). Source snapshots establish only what was verified at a date/version. They do not prove local implementation, validated capability or runtime permission. SDK behavior is implementation evidence, never protocol authority.

## Lifecycle and status

```text
external fact verification
  -> candidate evidence
  -> local conformance
  -> consumer-specific capability validation
  -> explicit promotion/runtime intersection
```

Allowed documentary states include `UNVERIFIED`, `VERIFIED_AS_OF`, `NOT_FOUND_CURRENT_V1`, `CONFLICT`, `STALE`, `SUPERSEDED`, `REVALIDATION_REQUIRED` and `NOT_APPLICABLE`. They are not M0–M5 maturity. Each record preserves source class, locator/version or retrieval date, scope, confidence/conflict and next trigger. No successful revalidation auto-promotes or auto-restores M5.

## EXT-001..023 current checklist

`Snapshot` below references the dated CORR-04 (2026-09-08) and CORR-06 (2026-09-09) primary-source ledgers where applicable; unrefreshed source-corpus claims remain historical. “Consumer entry” replaces the misleading “earliest technical phase”: work may start earlier, but the fact must be current before the named consumer relies on it.

| ID | Fact family | Source class | Documentary status / snapshot | Consumer entry | Local conformance and capability gate | Safe fallback |
|---|---|---|---|---|---|---|
| EXT-001 | order/matching/batching, IOC/ALO semantics | official exchange docs | VERIFIED_AS_OF 2026-09-09; revalidate before encoding/use | phases 12–13; emulator/transport | fixtures, Replay, then mode-specific validation/promotion | reject unsupported order/mode |
| EXT-002 | API/WS endpoints/subscriptions/reconnect | official exchange docs | VERIFIED_AS_OF 2026-09-09 | phase 2 adapter | payload/reconnect conformance; Shadow before capital | adapter NON-READY |
| EXT-003 | fees/tiers/debit asset | official exchange/account facts | REVALIDATION_REQUIRED; historical source snapshot | phase 5/economics | point-in-time goldens and account reconciliation | no economic permission |
| EXT-004 | metadata/precision/lot/tick/minimums | official exchange metadata | REVALIDATION_REQUIRED; historical source snapshot | phase 5/formulas/orders | boundary goldens and invalidation tests | reject affected market/q |
| EXT-005 | public-feed cadence/fields/identity | official exchange docs + observed capture | VERIFIED_AS_OF 2026-09-09; measurement still required | phase 2/data/book | sequence/gap/reconnect capture; Shadow | public-feed scope NON-READY if invalid |
| EXT-006 | node requirements/flags/outputs/region | official node repo/docs | VERIFIED_AS_OF 2026-09-09 at pinned commit | future node challenger | install/capture/benchmark then scoped validation | public-feed V1 baseline |
| EXT-007 | order_book_server L2/L4/spot | official repository | VERIFIED_AS_OF 2026-09-09: current spot support absent | phases 18/22 if consumed | repository/version conformance before any fidelity claim | no V1 spot-L4 dependency |
| EXT-008 | rate limits/CLOID/nonce/`scheduleCancel` | official exchange docs | VERIFIED_AS_OF 2026-09-09 | phase 13 transport | signer/idempotence/rate fixtures then Shadow | no blind retry; no new risk |
| EXT-009 | TradingFX offer | provider snapshot | REVALIDATION_REQUIRED before spend | infra benchmark/phase 19+ | offer admission then comparable benchmark | exclude candidate |
| EXT-010 | Akamai/Linode offer | provider snapshot | REVALIDATION_REQUIRED before spend | infra benchmark/phase 19+ | offer admission then comparable benchmark | exclude candidate |
| EXT-011 | Kamatera offer | provider snapshot | REVALIDATION_REQUIRED before spend | infra benchmark/phase 19+ | offer admission then comparable benchmark | exclude candidate |
| EXT-012 | AWS Lightsail offer | provider/official cloud docs | REVALIDATION_REQUIRED before spend | infra benchmark/phase 19+ | offer admission then comparable benchmark | exclude candidate |
| EXT-013 | Sakura offer | provider snapshot | REVALIDATION_REQUIRED before spend | infra benchmark/phase 19+ | offer admission then comparable benchmark | exclude candidate |
| EXT-014 | Cherry VDS offer | provider snapshot | REVALIDATION_REQUIRED before spend | infra benchmark/phase 19+ | offer admission then comparable benchmark | exclude candidate |
| EXT-015 | SDK/library/runtime support family | official releases/security advisories | SDK snapshot VERIFIED_AS_OF 2026-09-09; aggregate family revalidated per selected dependency | chosen implementation phase | compatibility/security tests; protocol verified independently | pin supported dependency or exclude |
| EXT-016 | academic claims/dataset statistics | primary literature | UNVERIFIED per exact research use; not exchange truth | phase 21/research consumer | provenance plus local temporal OOS; cannot calibrate Hyperliquid alone | research motivation only |
| EXT-017 | `split_client_blocks` semantics | official node repo at pinned commit | VERIFIED_AS_OF 2026-09-09; uncommitted/no-response/random-default constraints | node research/Shadow | isolated speculative Replay/parity; separate authorization | canonical feed only |
| EXT-018 | gossip/read and IOC/ALO write priority | official exchange docs | VERIFIED_AS_OF 2026-09-09 for existence/typed costs; advantage unvalidated | priority experiment consumer | schema/charge conformance, paired Shadow/Micro-live/economics | no priority policy/input |
| EXT-019 | FIX order entry | official transport docs/repos search | NOT_FOUND_CURRENT_V1 as of 2026-09-08 | future transport only | official support then independent conformance/benchmark | HTTP/WS abstraction; no FIX adapter |
| EXT-020 | Docker bridge/host networking | official Docker docs | VERIFIED_AS_OF 2026-09-08 for general semantics; workload advantage UNVERIFIED | deployment profile | security-preserving local benchmark and validation | isolated bridge baseline |
| EXT-021 | Linux CPU/IRQ/network tuning | kernel/man-page sources | VERIFIED_AS_OF 2026-09-08 for mechanisms; profile effect UNVERIFIED | bottleneck-specific infra candidate | reversible host benchmark, starvation/security/ops gates | default supported host profile |
| EXT-022 | AF_XDP/DPDK/F-Stack | primary project/docs | VERIFIED_AS_OF 2026-09-08 for capabilities; app-path applicability UNVERIFIED | future Research only | prove TCP/TLS/WebSocket fit, security, operations and economics before prototype | standard kernel network path |
| EXT-023 | fast cancel | two official exchange pages | CONFLICT / REVALIDATION_REQUIRED as of 2026-09-09: recommendation versus “currently no other effect” | phase 13 cancellation policy | preserve field only; controlled actual evidence after resolution | assume no measurable advantage |

## Scope, conflicts and historical truth

An invalid/stale fact blocks the smallest safely isolated consumer. Node uncertainty does not block a separately verified public-feed TT baseline; provider uncertainty excludes that candidate rather than the system; maker/priority uncertainty disables that feature. Shared signer/account/owner uncertainty may propagate broadly. Cancel, reconciliation, bounded Recovery and evidence preservation remain available whenever safe.

Conflicting authoritative sources stay `CONFLICT`; the favorable interpretation is never selected. Current facts apply only from their effective time. Historical Replay resolves the source snapshot that was available at event time and never rewrites history using current fees/rules.

## Dynamic dependencies and triggers

New changing dependencies receive the next EXT ID, source class/locator/version/retrieval date, exact consumers, verification owner, fallback and triggers. No ID is repurposed. Triggers include exchange/API/schema/fee/rule change; repository/runtime/library/security release; provider offer/region change; host/kernel/driver/container change; evidence expiry/conflict; observed divergence; and capability scope expansion.

OCI registry, signature/SBOM/scanner and vulnerability-tool facts are registered when concrete tooling is selected. EXT-015 remains an aggregate family but each selected component gets a resolvable versioned evidence record.

## Non-authority invariants

Official existence is not enablement. SDK implementation is not protocol truth. A provider claim is not a benchmark. A paper is not Hyperliquid calibration. Node compatibility is not node dependency. Priority feature existence is distinct from measured advantage, economic benefit and production authorization. External change may invalidate Formula inputs or Risk assumptions but cannot silently alter Formula architecture, accounting ownership, units, invalid semantics or hard Risk rules.
