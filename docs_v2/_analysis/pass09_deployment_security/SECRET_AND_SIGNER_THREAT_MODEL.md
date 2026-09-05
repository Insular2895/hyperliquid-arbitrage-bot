# Secret and Signer Threat Model

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Protected assets

Client signer/API-wallet private material, exchange tokens, registry credentials, license credentials, host access tokens and any derived signing payload are sensitive. The trading signer must have the minimum exchange permissions and no withdrawal authority.

| Threat | Preventive control | Detection/evidence | Safe response |
|---|---|---|---|
| Secret baked into image/layer | Build-time secret scan; external secret mount | Image/layer audit | Reject artifact, rotate secret |
| Secret in config/env/CLI | Read-only secret file; schema forbids secret fields | Preflight plus process/env inspection | Block READY; remove and rotate |
| Secret in logs/panic/core | Structured allowlist logs; redaction; core dump policy | Canary secret tests | Disable export, rotate, incident response |
| Secret in diagnostic bundle | Field allowlist plus denylist and entropy tests | Bundle inspection before export | Fail closed; client confirmation |
| Registry credential can publish | Read-only client scope | Registry audit | Revoke/rotate credential |
| Signer theft | Strict host/file permissions and host hardening | Auth/account anomaly | New risk off, cancel/reconcile, revoke |
| Signer revoked/missing | Preflight and authenticated exchange check | Readiness reason | No new risk; reconcile with available read authority |
| Vendor backdoor | No inbound vendor control and no secret upload | Network/build audit | Halt and investigate |

## Lifecycle

Provision locally → validate scope/permissions → mount read-only → use only in signer boundary → never serialize/export → rotate under a controlled risk-off procedure → revoke old credential after safe migration → retain an audit record without the secret. Rotation order is: stop new risk, reconcile, replace credential, restart/reload, validate, reconcile and only then restore READY.

Memory zeroization should be used where practical, but does not replace process isolation, minimum privileges and log/export controls.
