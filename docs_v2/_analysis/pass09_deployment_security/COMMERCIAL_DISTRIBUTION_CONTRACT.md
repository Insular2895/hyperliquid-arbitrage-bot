# Commercial Distribution Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Canonical model

```text
client -> own VPS/server -> own OCI container/process
       -> own Hyperliquid account -> own signer/API wallet -> own capital
```

The product is a distributed software package, not a centralized multi-tenant execution SaaS. The vendor supplies a private immutable image, `botctl`, Compose/config templates, documentation, a release channel, a license entitlement and support. The client owns the runtime boundary, account, signer, funds, configuration, persistent data, logs and authorization to trade.

## Responsibility matrix

| Concern | Client | Vendor | Invariant |
|---|---|---|---|
| VPS, host account and OS | Owns/administers | Publishes supported profile | Vendor cannot silently alter host security |
| Exchange account/capital | Owns | No custody | No vendor trading backdoor |
| Signer/API wallet | Creates, scopes, stores, rotates, revokes | Specifies safe handling | No withdrawal permission; no upload to vendor |
| Image | Pulls by version/digest | Builds, signs, scans, releases | Artifact immutable and attributable |
| Config/risk overrides | Supplies local values | Supplies schema/defaults | Client may tighten, never weaken constitutional floors |
| State, journal, recorder, logs | Owns | Defines formats/retention boundary | Container replacement must preserve declared state |
| License | Holds entitlement | Issues/revokes signed entitlement | Validation outside hot path; failure cannot block recovery |
| Support | Chooses what to send | Provides redaction-safe tooling | Bundle remains local until explicit client action |
| Updates | Approves and schedules | Publishes verified release | No silent automatic activation |

Each client installation has a unique `installation_id`, isolated credentials, volumes, config and runtime identity. Thirty clients mean thirty isolated deployments—not one shared trading engine.

## Distribution package

The supported package comprises the OCI reference, expected digest/signature, SBOM/provenance metadata, read-only registry access, Compose template, config schema/templates, `botctl`, onboarding/runbooks, release notes, compatibility declaration and license entitlement. Source delivery is not required by the model; Docker packaging alone does not guarantee IP secrecy, so commercial/legal controls remain necessary.

## Non-goals

- no pooled custody or capital;
- no vendor-side order routing dependency;
- no central Redis/Postgres/license/dashboard call in the trading hot path;
- no hidden remote-control channel;
- no Kubernetes or fleet orchestrator in the initial baseline;
- no guarantee that a container prevents reverse engineering.

Pricing, customer limits, registry provider, support SLA and exact license grace duration are `COMMERCIAL_POLICY` or `OPEN_ITEM`, not technical facts.
