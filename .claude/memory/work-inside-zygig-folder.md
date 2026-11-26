---
name: work-inside-zygig-folder
description: "Keep all Claude working files (scripts, worktrees, venv, outputs) inside ~/Code/Zygig/claude-workspace, not /tmp or Desktop"
metadata:
  node_type: memory
  type: feedback
  modified: 2026-11-23T00:02:33.094Z
---

Keep everything Claude needs for the Zygig work inside `/Users/rajyabhaiya/Code/Zygig/claude-workspace/` (`tools/` for scripts and the venv, `worktrees/` for git worktrees, `out/` for logs, screenshots and generated output). Do not put working files in /tmp, the session scratchpad, `~/Desktop` or `~/Downloads`.

**Why:** paths outside the Zygig folder trigger permission prompts, and the user (2026-11-22) asked that Claude stop asking for permissions outside that folder.

**How to apply:** create worktrees under `claude-workspace/worktrees/`, write generated files to `claude-workspace/out/`, run the App Store Connect helpers from `claude-workspace/tools/` (venv at `tools/venv`, helper `asc.py`). The App Store Connect API key stays at `~/.appstoreconnect/private_keys` (a secret; never copy it into the folder). Existing Desktop output folders (zygig-liquid-glass, zygig-settings-feedback, zygig-frame, zygig-screenshots-new) were left in place. See [[skip-ci-on-commits]] for the commit rule.
