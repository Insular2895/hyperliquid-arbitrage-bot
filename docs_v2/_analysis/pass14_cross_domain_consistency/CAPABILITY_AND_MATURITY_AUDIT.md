# Capability and Maturity Audit

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

```text
EffectiveCapability = CompiledSupport
                    ∩ ConfiguredEnablement
                    ∩ LicenseEntitlement
                    ∩ ReleaseChannelPolicy
                    ∩ ValidatedCapability
                    ∩ CurrentReadiness
                    ∩ RiskPermission
```

| Claim | What proves it | What does not prove it | Result |
|---|---|---|---|
| specified M0 | complete contract and planned evidence | code existence | PASS |
| unit validated M1 | local unit/property/golden/contract evidence | Replay/live behavior | PASS |
| Replay validated M2 | deterministic point-in-time same-Core Replay | causal market impact | PASS |
| Shadow validated M3 | sustained live-input no-effect evidence | actual fills/fees/cancel race | PASS |
| Micro-live validated M4 | bounded real orders/fills/account calibration | larger q/new market/mode | PASS |
| Live validated M5 | sustained exact-scope economic/safety/ops evidence | permanent/global authority | PASS |
| compiled | artifact contains implementation | configured, licensed, validated or ready | PASS |
| configured | feature/mode enabled in resolved config | validated or Risk-allowed | PASS |
| licensed | commercial entitlement covers scope | technical/safety validity | PASS |
| Stable release | promoted release channel | automatic Live | PASS |
| ready | current state supports named action/scope | maturity or future permission | PASS |

Critical dependency ceiling is monotone: capability maturity cannot exceed the least mature critical dependency. Demotion may be automatic for locked safety failures; re-promotion is explicit. `CapabilityManifest` exact-subset matching cannot round size up, substitute models or inherit evidence across markets/modes. Maturity conflations: **0**.
