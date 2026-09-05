# 03 — Container Runtime Hardening and Filesystem

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Runtime profile

The initial physical topology is one VPS, one OCI image and one process/container. Logical engine modules remain separate in code/data ownership; this does not require a service mesh, Kubernetes, Redis, Kafka or PostgreSQL.

The container:

- runs as a dedicated non-root user;
- uses a read-only root filesystem;
- writes only to declared state/recorder/model/log paths;
- drops all capabilities unless a documented tested exception exists;
- is not privileged and cannot access the Docker socket, host root or host PID namespace;
- cannot adjust host time;
- receives explicit PID/CPU/memory policy and bounded logging;
- starts with no trading authority.

## Persistent boundary

Configuration and secrets are read-only inputs. State, journal, recorder data, separately promoted models and logs are declared persistent mounts. The image contains no client-specific mutable truth. Replacing it cannot erase or overwrite mounted data outside an explicit migration transaction.

Logs rotate and are operational evidence, not the fill/account ledger. PASS06 owns record priority and retention. Under disk pressure, the runtime preserves unique fills, journal/account truth, coherent checkpoints and active trade/incident windows before lower-priority data. It enters no-new-risk before safe persistence is lost.

## Host responsibility

The host supplies clock discipline, disk durability/capacity, kernel/runtime patching, firewall, access control, backup target and supervisor. Container isolation is defense in depth, not a substitute for host hardening.

## Verification

Installation evidence includes runtime UID, mount modes, root write probes, capability/privilege/namespace/socket inspection, resource-pressure behavior, restart/reconciliation behavior and absence of secrets from layers. Exact seccomp/AppArmor profile, UID, limits, affinity and swap policy are calibrated/open implementation details.
