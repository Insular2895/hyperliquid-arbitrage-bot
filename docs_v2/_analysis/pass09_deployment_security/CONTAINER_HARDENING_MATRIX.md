# Container Hardening Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Control | Baseline | Failure consequence | Verification |
|---|---|---|---|
| User | Non-root dedicated `bot` UID/GID | Activation rejected | Runtime identity test |
| Root filesystem | Read-only | Activation rejected unless explicitly justified/tested | Write probe |
| Writable paths | Explicit config/secrets read-only; data/log mounts only | Preflight failure | Mount inspection |
| Linux capabilities | Drop all; add none unless documented | Release gate failure | Runtime capability inspection |
| Privileged mode | Forbidden | Release/installation rejection | Container config audit |
| Docker socket | Forbidden | Installation rejection | Mount audit |
| Host root/PID namespace | Forbidden | Installation rejection | Runtime spec audit |
| Time adjustment | No `CAP_SYS_TIME`; host `chrony` owns clock | Clock unhealthy blocks new risk | Capability and clock check |
| Seccomp/AppArmor | Runtime-supported restrictive profile | Tooling OPEN; deviation recorded | Profile and denial tests |
| Resource limits | Explicit CPU/memory/PID limits, calibrated | Risk degradation before unsafe exhaustion | Stress/pressure test |
| CPU affinity | Optional measured optimization | No unmeasured guarantee | Benchmark comparison |
| Swap/OOM | Host policy plus early `NO_NEW_RISK` thresholds | OOM/restart enters reconciliation | Stress/restart evidence |
| Restart policy | Process may restart automatically | Never grants trading authority | Startup-state test |
| Logging | Structured, bounded, secret-safe | Export disabled on redaction failure | Leak/rotation test |

Exact UID, seccomp profile, resource values and CPU placement remain calibrated/implementation choices. The behavior—least privilege, explicit writes and safe degradation—is locked.
