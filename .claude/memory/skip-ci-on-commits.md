---
name: skip-ci-on-commits
description: "User wants CI skipped on Claude's commits ([skip ci]) and PR merges not blocked on checks"
metadata:
  node_type: memory
  type: feedback
  modified: 2026-11-19T21:36:44.883Z
---

Add `[skip ci]` to every git commit message Claude writes in the ZYGIGllc repos, and merge PRs without waiting for CI checks. Do not disable Actions or change repo/workflow settings.

**Why:** GitHub Actions on the ZYGIGllc account fails instantly ("recent account payments have failed or your spending limit needs to be increased"), so every check shows FAILURE and blocks nothing useful. The user chose "skip CI on my commits only" over disabling Actions in all 29 repos (asked 2026-11-19).

**How to apply:** put `[skip ci]` in the commit subject or body (before the Co-Authored-By trailer). Still report that checks did not run when merging. If the billing is fixed, ask before continuing to skip. See [[github-actions-billing-blocked]].
