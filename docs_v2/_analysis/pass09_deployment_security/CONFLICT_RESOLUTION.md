# PASS 09 Conflict Resolution

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

The authority order is SRC-006 Dossier 5 closure, then later compatible source detail, PASS00 provenance and legacy documentation. The following documentary conflicts are resolved without turning open implementation choices into decisions.

| # | Earlier/exploratory direction | Canonical resolution | Status |
|---:|---|---|---|
| 1 | Central platform may execute for clients | Each client owns an isolated VPS/container/account/signer/capital boundary | Resolved |
| 2 | Multi-service/distributed baseline | One initial host, image and process/container with logical module separation | Resolved |
| 3 | Redis/Postgres/Kafka/Kubernetes as baseline | None required in the initial trading hot path/deployment | Resolved |
| 4 | Vendor license/dashboard dependency in decision path | License and optional telemetry stay outside hot path | Resolved |
| 5 | Image tag as release identity | Immutable digest plus version/provenance is authoritative | Resolved |
| 6 | Production follows `latest` | Explicit version/digest pinning; no production `latest` | Resolved |
| 7 | Image contains mutable config/data | Image replaceable; config/secrets/state/logs have explicit external boundaries | Resolved |
| 8 | Automatic container restart can resume trading | Restart returns to non-ready sync/reconciliation | Resolved |
| 9 | Liveness equals readiness | Process, readiness and trading-health states are separate | Resolved |
| 10 | License failure stops all operations | It blocks new risk but preserves cancel/reconciliation/Recovery/read access | Resolved |
| 11 | Vendor support may pull data remotely | Client builds/inspects/sends redacted bundle explicitly | Resolved |
| 12 | Docker is an IP-secrecy guarantee | Packaging raises distribution convenience only; commercial/legal controls remain | Resolved |
| 13 | Hot standby can be assumed safe | Cold recovery first; standby needs explicit fencing/active-owner validation | Resolved |
| 14 | Update is replace-and-restart | Risk-off, resolve, backup, ownership handoff, reconcile and health gates are mandatory | Resolved |
| 15 | Rollback restores old state | Previous code must reconcile against current exchange truth | Resolved |
| 16 | Config/client may override every risk value | Client may tighten, never weaken constitutional floors | Resolved |
| 17 | Telemetry contains broad trading data | Minimal opt-in diagnostics only; no credentials/raw orders/full balances/history | Resolved |
| 18 | Exact base image/network/signing/provider is already fixed | Behavior is locked; tooling/benchmarked selection remains OPEN | Resolved |

Conflicts found: **18**. Resolved: **18**. Remaining documentary conflicts: **0**. Exact providers, tools, thresholds, grace duration, hardware binding and standby design remain explicit open/calibrated questions rather than conflicts.
