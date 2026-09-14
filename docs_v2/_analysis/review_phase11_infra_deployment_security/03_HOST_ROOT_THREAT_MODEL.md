# Host-Root Threat Model

| Attacker | Container hardening helps? | Remaining authority |
|---|---:|---|
| app process | yes | bounded mounts/capabilities/network |
| adjacent unprivileged container | yes | runtime/kernel controls |
| malicious host root/VPS control plane | no reliable boundary | can inspect memory/files/network/runtime |
| registry attacker | digest/signature verification | cannot pass independent trust root |
| vendor support | no implicit access | client-controlled audited session only |

Docker is isolation/hardening, not protection from compromised host root.
