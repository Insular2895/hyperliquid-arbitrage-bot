# CORR-04 — Baseline and Scope

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

## Baseline

- `CORR04_BASELINE_COMMIT`: `5a8d5244e2a78da1b4698c4a563b1f3e9972b2be`
- branch: `codex-docs`
- prerequisite: CORR-03 verified complete at baseline
- date: 2026-09-08

## Authorized work

Documentation, repository inspection, current-source verification and benchmark/validation design only. No node deployment, provider purchase, real order, Docker/runtime change, CPU/IRQ/scheduler/sysctl tuning, kernel bypass, firewall/TLS change or transport implementation is authorized.

## Locked boundaries

The public Hyperliquid feed remains the initial canonical baseline. A node is an observe-only challenger until explicit promotion. Every run has exactly one canonical `MarketState` writer and one active economic execution owner. Speculative/uncommitted input is `NON-CANONICAL`, may prepare pure work only, and cannot authorize risk-increasing transmission.

QF-084–QF-093, the Formula Book, Risk hierarchy, actual-fill truth, `UNKNOWN`, Recovery, Reconciliation and CORR-03 completion semantics are unchanged. No additional QF identifier, priority-value formula, new Risk gate or Execution behavior is introduced.

## Deliverable boundary

CORR-04 specifies evidence and escalation gates across feeds, node topology, provider/region, Docker/native, CPU/scheduler/IRQ/network and kernel-bypass research. Human approval remains pending; implementation remains not authorized; CORR-05 is not started.
