# Single Owner and Cross-Host Fencing Audit

| Scenario | Local lock enough? | Cross-host proof? | New risk? |
|---|---:|---:|---:|
| second process same host | yes | no | owner only |
| second process/new VPS | no | yes | no until handoff |
| normal migration | no | yes | after proof/reconcile |
| old host unreachable | no | revoke/fence | no |
| reboot same host | recreated | reconcile | not immediately |
| future hot standby | no | distributed fencing | Future |

`LOCAL LOCK != DISTRIBUTED FENCING`. Economic scope is account/signer authority, not installation ID alone.
