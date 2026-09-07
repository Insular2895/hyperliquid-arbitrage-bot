# Deployment Topology

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

```text
ONE CLIENT VPS / HOST
├── host clock synchronization
├── local operator + botctl/diagnostics
├── OCI trading container
│   ├── immutable digest-pinned Rust runtime
│   ├── non-root/read-only/drop capabilities
│   └── one active account execution owner
├── read-only resolved config mount
├── protected secret/signer boundary
├── state/journal/checkpoint mount
└── RAW/data/log mount

EXTERNAL
├── Hyperliquid public + authenticated endpoints
├── artifact registry/update source
└── signed license service outside hot path

RESEARCH ENVIRONMENT
└── Python lab + archived point-in-time datasets/artifacts
```

## Boundaries

One installation maps to one VPS/container/account/signer/capital/config/data/log/license context. The client owns account/signer/capital. No vendor custody and no shared central trading process exist. Diagnostics remain local/redacted until explicit client export.

The container cannot defend against malicious host root. It has no Docker socket, host-root/host-PID or clock-setting access. External network paths are allowlisted by role. Config/secrets/state/data/logs do not enter the immutable image.

Initial infrastructure is a lightweight Tokyo candidate using public feed, subject to current revalidation and benchmark. A node, separate Recorder, second host or standby is added only after evidence and new trust/failure analysis. Standby requires fencing and single active ownership.

Update/rollback/migration follows risk-off → resolve → persist → transfer owner → verify artifact → non-ready boot → sync/reconcile → validate readiness. Software rollback never rolls back exchange state.
