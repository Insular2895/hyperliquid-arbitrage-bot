# Infrastructure, Deployment and Security Review

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Baseline product topology

- One isolated deployment per client account; the client owns signer, capital and persistent data.
- Signed immutable OCI release by digest, least-privilege container/user, bounded resources, explicit filesystem/network policy and auditable upgrade/rollback.
- Secrets are never embedded in images, configs committed to Git, logs, telemetry or support bundles.
- Startup preflight plus exchange reconciliation precede readiness.
- Safe shutdown stops new risk, contains/reconciles external state and preserves evidence.
- A second instance must not trade the same account; account-scoped ownership fencing is mandatory.
- Licensing and optional telemetry remain outside the hot path. Failure can narrow/stop new activity but cannot block Recovery/Reconciliation or strand exposure.
- No baseline vendor custody, centralized multi-tenant trading engine or mandatory remote admin.

## Evidence-gated choices

Provider, region, bridge versus host networking, CPU/memory/storage, retention, health windows, telemetry backend, license mechanism, runtime/base-image/toolchain and node/private-feed options are not universal constants. Source prices/specifications are historical snapshots. Selection requires current revalidation, comparable controlled benchmarks, security review and robust net economic evidence.

Infrastructure economics compare incremental captured value with incremental all-in cost and downside using confidence bounds and a safety factor. A faster median is insufficient; jitter, tails, gaps, failure containment, recovery time and operational cost matter. `OPEN-005/023` retain the exact LCB/alpha/safety-factor convention.

## Failure and rollback semantics

Deployment rollback reverts software/config artifacts, not exchange effects. After crash, update or rollback, Reconciliation must restore orders→fills→balances before readiness. Critical vulnerability, secret exposure, signature failure, unsupported runtime, storage exhaustion or owner-fence loss causes a scoped less-active state and incident/runbook flow.

All numerical defaults in this domain are either calibration candidates, measured limits or external facts to revalidate. None is certified by this documentation package.
