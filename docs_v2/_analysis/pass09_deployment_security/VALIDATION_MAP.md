# PASS 09 Validation Map

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

This map specifies evidence expected by the future Validation pass; it does not claim that implementation tests already exist.

| Contract | Required test/evidence | Pass condition |
|---|---|---|
| Build provenance | Build from pinned revision/lock/toolchain; inspect attestation | Artifact traces to declared inputs |
| Digest pinning | Resolve version and inspect runtime digest | Runtime equals expected immutable digest |
| Signature verification | Verify authorized signer over digest | Valid chain/policy before activation |
| Wrong digest rejection | Substitute mismatched candidate | Candidate rejected before owner change |
| Non-root runtime | Inspect UID and privileged operations | Dedicated non-root; required work succeeds |
| Read-only root filesystem | Write probes outside declared mounts | Writes fail; service remains healthy |
| No Docker socket | Inspect mounts and access attempt | Socket absent/inaccessible |
| No privileged mode | Runtime spec inspection | Privileged false; capabilities policy satisfied |
| Secret absent from image | Scan layers/files/history | Canary/real patterns absent |
| Secret absent from logs | Exercise auth/errors/panic paths with canary | No canary or derived token survives |
| Secret absent from diagnostics | Build/export test bundle with canary | Redaction fails closed; secret absent |
| Invalid config blocks READY | Corrupt/type/range/invariant cases | Stable reason; no new risk |
| Schema incompatibility | Present unsupported config/checkpoint/journal/model/event versions | Unsafe start blocked; evidence retained |
| Startup reconciliation | Seed open orders/fills/balance differences | No READY before resolved truth |
| Safe shutdown | Signal during idle and active execution | Risk-off, cancel/resolve, persist, release owner |
| Update without exposure | Full verified transaction | New digest ready; old owner absent |
| Update with active exposure | Begin update mid-execution | No replacement until resolved/recovery state explicit |
| Update failure | Fail download/verify/start/migration/health phases | Old safe service retained or declared rollback path |
| Rollback | Activate known prior digest | Compatibility checked and reconciliation completes |
| Rollback after exchange change | Change orders/fills after checkpoint | Exchange truth wins; stale state not restored |
| Dual-active prevention | Concurrent start/local and migration scenarios | At most one new-risk owner; ambiguity blocks all |
| License outage | Disconnect validator with cached entitlement | Policy applied outside hot path; safe actions remain |
| License expiry/revocation | Expire/revoke entitlement | New risk off; cancel/reconcile/Recovery usable |
| Local admin binding | Network scan from untrusted interface | Admin/health not publicly exposed |
| Diagnostic redaction | Golden bundle + fuzz/entropy/canary corpus | Forbidden fields absent; manifest accurate |
| Host migration | Follow old→new sequence with interruption cases | No overlap; new host reconciles before READY |
| Release promotion | Trace Code→Stable evidence | No skipped mandatory gate; artifact identity unchanged |

Evidence must identify artifact/config/schema/model/capability versions, installation, time and result. Failure-path evidence is as important as nominal success. Exact thresholds and PASS/FAIL ownership are finalized in PASS10.
