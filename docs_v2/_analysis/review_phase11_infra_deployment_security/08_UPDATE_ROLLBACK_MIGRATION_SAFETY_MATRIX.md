# Update, Rollback and Migration Safety Matrix

| Event | Owner handoff | Start state | Economic proof |
|---|---|---|---|
| update | verify candidate, risk-off, stop old | non-ready | reconcile current exchange |
| rollback | known digest/compatibility, stop failed | non-ready | never restore old exposure blindly |
| host move | fence/revoke old authority | non-ready | sync/reconcile/ownership proof |
| uncertain old host | no handoff | halted/no new risk | establish exchange truth first |

Push/deploy/process stop never proves effects undone.
