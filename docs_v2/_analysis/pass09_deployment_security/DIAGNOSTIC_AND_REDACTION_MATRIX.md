# Diagnostic and Redaction Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Data class | Collect locally | Export | Treatment | Support-safe | Client confirmation |
|---|---:|---:|---|---:|---:|
| App version, Git revision, image digest | Yes | Yes | Plain | Yes | At transfer |
| Schema and model/feature versions | Yes | Yes | Plain | Yes | At transfer |
| Sanitized ResolvedConfig | Yes | Yes | Allowlist; secret fields omitted | Yes after scan | At transfer |
| Config hash | Yes | Yes | Hash | Yes | At transfer |
| Installation/account identity | Yes when needed | Limited | Pseudonymize/hash | Conditional | Explicit |
| Private key, seed, API secret/token | Never in diagnostics | Never | Omit; leak scan | No | Not exportable |
| Registry/license credential | Never as value | Never | Omit | No | Not exportable |
| Orders/fills | Local economic record | Incident subset only | Minimize/pseudonymize | Conditional | Explicit |
| Full balances/history | Local only by default | No default | Omit/aggregate | No default | Explicit exceptional approval |
| Health/readiness/reason codes | Yes | Yes | Plain | Yes | At transfer |
| CPU/memory/disk/clock/network metrics | Yes | Yes | Remove public IP/host identifiers as needed | Yes | At transfer |
| Recent structured logs | Yes | Bounded | Field allowlist plus token/entropy scan | Conditional | Explicit |
| Panic/stack trace | Yes if safe | Conditional | Path/secret/address redaction | Conditional | Explicit |
| Core dump/memory dump | Disabled or tightly protected | Never ordinary bundle | Omit | No | Separate incident process |
| Journal/checkpoint/raw recorder | Yes under PASS06 | No ordinary bundle | Omit; targeted derivation only | No | Separate approval |
| Incident IDs/timestamps | Yes | Yes | Plain/pseudonymous | Yes | At transfer |

Bundle construction is local and produces a manifest of included/omitted fields, hashes and redaction-tool version. A canary-secret/denylist/entropy scan runs before export; any hit fails closed. The client sees the bundle and explicitly initiates transfer. Telemetry uses a separate opt-in contract and cannot silently expand the support-bundle scope.
