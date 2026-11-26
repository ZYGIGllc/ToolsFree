---
name: github-actions-billing-blocked
description: GitHub Actions is billing-blocked on ZYGIGllc; all CI runs fail without starting
metadata:
  node_type: memory
  type: project
  modified: 2026-11-19T21:36:47.307Z
---

As of 2026-11-19, every GitHub Actions job in the ZYGIGllc org fails within ~2s with "recent account payments have failed or your spending limit needs to be increased". PR checks therefore show FAILURE regardless of code state, and no merged PR has had real CI.

**Why:** billing/spending limit on the GitHub account, not code defects.

**How to apply:** don't treat red checks as code failures; verify locally (e.g. `tsc` + `vitest` in MCPReadiness) when it matters. Related user preference: [[skip-ci-on-commits]].
