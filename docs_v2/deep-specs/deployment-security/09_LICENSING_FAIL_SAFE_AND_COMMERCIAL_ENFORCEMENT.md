# 09 — Licensing Fail-Safe and Commercial Enforcement

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Entitlement

The runtime verifies a locally cached signed entitlement with an embedded vendor public key. Candidate fields are license ID, installation ID, enabled commercial features, validity/expiration and signature. The exchange private key is never sent to or needed by the license service.

License validation runs outside the order/decision hot path. Temporary service unavailability may use a bounded cached grace policy; exact duration, renewal cadence, revocation transport and hardware binding are commercial/security decisions. Binding must tolerate planned recovery/migration through a controlled process.

## Permission rule

Commercial entitlement is a necessary but insufficient input for new-risk capability. It cannot add a strategy, size or mode absent from compiled/configured/validated/current-Risk support.

Expired, revoked, invalid or missing entitlement blocks new risk. It does not block:

- canceling open orders;
- reconciling orders, fills, balances and inventory;
- reducing or recovering existing exposure;
- safe shutdown;
- reading/exporting client-owned data through redaction rules;
- diagnosing or updating to repair the installation.

This prevents commercial enforcement from stranding client capital or obscuring truth.

## Security and privacy

Entitlement requests expose only the minimum installation/license/release metadata. License credentials are separate from registry and exchange credentials. Cached files have strict permissions and signature checks. Revocation/expiry decisions emit stable reasons and audits without secret material.

## Failure tests

Validate service outage at startup/runtime, stale cache, invalid signature, wrong installation binding, expiry during exposure, revocation during execution, clock uncertainty, host migration and renewal. Every case must demonstrate safe-action continuity and no synchronous dependency in the hot path.
