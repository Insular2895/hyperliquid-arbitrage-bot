# Speculative Failure Matrix

`COMMON EXPECTATION: canonical economic truth and permissions are unchanged`

| ID | Scenario | Allowed research response | Required safe result |
|---|---|---|---|
| `S-01` | commits identically | label exact; parity-test reuse | canonical reducer applies canonical event once |
| `S-02` | commits with changed quantity | discard economic precompute | fresh canonical recomputation |
| `S-03` | commits reordered | retain arrival/order evidence | canonical order governs state |
| `S-04` | never commits | label disappeared; expire scratch | no canonical mutation or send |
| `S-05` | canonical arrives before speculative work finishes | cancel/ignore stale scratch | canonical path does not wait |
| `S-06` | speculative feed disconnects | alert research quality; stop lane | canonical readiness unaffected unless shared resource is harmed |
| `S-07` | speculative feed leads then goes stale | mark invalid/expired | no fallback authority or increased action |
| `S-08` | duplicate speculative event | deduplicate within research identity | no canonical duplicate |
| `S-09` | speculative sequence gap | mark invalid range; resync lane | no guessed event/state |
| `S-10` | node resync/reorg-equivalent correction if applicable | invalidate affected speculative lineage | rebuild research state; canonical committed lane remains authoritative |

Fault tests also assert separate metrics/IDs, no CORR-01 canonical funnel increment, no P0/P1 Recorder loss and no future-outcome leakage.
