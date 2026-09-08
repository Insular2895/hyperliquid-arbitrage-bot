# Container Security / Performance Contract

`INVARIANT: SECURITY IS A GUARDRAIL AND COST, NOT BENCHMARK NOISE`

Non-root, read-only root filesystem, explicit mounts, dropped capabilities, no privileged mode, no Docker socket, least-privilege signer, local/private admin, firewall and TLS remain. Host network or device access requires a specific threat model and least privilege; it never silently grants host root/PID/clock access.

Every performance treatment lists permissions/capabilities/devices, namespace change, public ports, secret reachability, supply-chain/runtime patching, blast radius, monitoring, recovery and rollback. A technical win is rejected if exposure, fragility or support cost outweighs recoverable value.

Kernel-mitigation, seccomp/AppArmor, firewall or TLS changes are security changes first. They require independent security evidence and explicit approval; CORR-04 authorizes none.
