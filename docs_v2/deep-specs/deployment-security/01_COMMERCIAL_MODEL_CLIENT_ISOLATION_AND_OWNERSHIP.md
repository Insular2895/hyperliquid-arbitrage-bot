# 01 — Commercial Model, Client Isolation and Ownership

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Contract

The project distributes client-operated software rather than offering centralized multi-tenant execution. Each client supplies and controls the VPS/server, Hyperliquid account, API wallet/signer, capital, configuration, persistent data and logs. The vendor supplies attributable artifacts, documentation, release/compatibility metadata, entitlement and support.

```text
Vendor release boundary              Client trust boundary
signed OCI + metadata  ---------->   host + config + secret + volumes
license entitlement    ---------->   one installation/process/account
redaction-safe support <----------   explicit client-created bundle
```

## Ownership

| Object/action | Owner | Forbidden transfer |
|---|---|---|
| Host/OS/runtime account | Client | Silent vendor mutation |
| Exchange account and capital | Client | Vendor custody or pooling |
| Signer/API wallet | Client | Upload to vendor/license/registry |
| Release artifact/metadata | Vendor | Mutable unidentified binary |
| Config and risk tightening | Client within constitution | Weakening hard Risk floors |
| State/journal/recorder/logs | Client | Automatic vendor collection |
| Live activation/update | Client/operator | Silent remote activation |

The vendor cannot take or manage trades without the client deployment. Optional telemetry and support never become a control plane. A client can revoke vendor registry/support access without disabling local cancel, reconciliation, Recovery or data access.

## Identity and isolation

`installation_id` identifies a deployment boundary. `DeploymentManifest` binds it to image/config/model/time identity. `RunManifest` remains the PASS06 experimental/runtime provenance object. Credentials, volumes and license are unique per installation; no cross-client runtime database or signer is part of the initial architecture.

One live process owns one signer/account authority. Thirty to fifty clients remain independent deployments. Fleet convenience must never collapse capital, state or credentials into a multi-tenant hot path.

## Product boundary

The package can contain the OCI reference/digest/signature, SBOM, `botctl`, Compose and configuration templates, schemas, release notes, license and support procedures. Source need not be shipped. Containerization aids reproducibility and distribution but is not an IP-confidentiality guarantee.

Pricing, client caps, support SLA and entitlement grace duration require explicit commercial decisions. They cannot silently alter safety behavior.
