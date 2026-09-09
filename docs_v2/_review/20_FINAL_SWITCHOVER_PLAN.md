# Final Switchover Plan

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

This is a deterministic **future** procedure. CORR-06 does not execute it. The recommended policy retains `_analysis` and `_review` inside the promoted canonical documentation for auditability; the human must explicitly accept that retention.

1. Obtain explicit approval quoting the exact current CORR-06 review commit SHA.
2. Record reviewer identity/date, documentation decision, open-item dispositions and Phase 1 decision in the decision form.
3. Verify the approved SHA is reachable from `origin/codex-docs` and the worktree is clean except acknowledged unrelated files.
4. Create a dedicated switchover branch from that exact approved SHA.
5. Re-run current CORR-06/PASS16 inventory, Markdown link, required-file, unchecked-gate and allowed-path validations.
6. Record the current `/docs` tree hash and file inventory as the legacy pre-state.
7. Record the current `/docs_v2` tree hash and file inventory as the candidate pre-state.
8. Confirm no source code, Cargo, Docker, CI, runtime config or test implementation is included.
9. Move existing `/docs` to a uniquely named, commit-local temporary legacy path; do not delete it yet.
10. Move `/docs_v2` to `/docs` without editing semantic content.
11. Retain promoted `/docs/_analysis` and `/docs/_review` unless the recorded human decision explicitly says otherwise.
12. Rewrite only path-relative links that became invalid because of the directory move; do not change meaning.
13. Run a full local Markdown-link and referenced-file check over promoted `/docs`.
14. Verify every 17 Master, 181 deep spec, 22 physical review files, PASS00–16 report, CORR-01..06 report and required register is present.
15. Search for stale `docs_v2` path references and classify each as historical text or a link requiring deterministic rewrite.
16. Diff candidate semantic content against the approved tree, excluding path-only link changes; require zero unapproved semantic drift.
17. Delete the temporary legacy tree only after the promoted tree and diff checks pass; recovery remains available from Git history.
18. Commit the switchover separately with the approved SHA and validation results in the message/body; push for human review, do not merge automatically.
19. Obtain explicit human acceptance of the switchover commit; if rejected, restore by reverting that separate commit and reconcile links.
20. Only after accepted promotion, create a separate Phase 1 implementation branch from the authorized baseline; Phase 2 and every capital-bearing mode remain unauthorized.

If any count, link, tree hash or semantic diff fails, stop before deletion/merge and report the exact mismatch. A post-approval semantic documentation change invalidates the approval and returns to human review.
