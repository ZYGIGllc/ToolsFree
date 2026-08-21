# Security Policy

## Our commitment

Every tool in this repo runs entirely client-side: no server-side
processing, no data collection, no analytics or trackers. This is a core
guarantee of the project, not just a preference — a report showing a tool
violates it (e.g. an unexpected network call, an embedded tracker) is
treated as a security issue.

## Reporting a vulnerability

Please **do not** open a public GitHub issue for security reports.

Instead, report privately via:

- GitHub's [private vulnerability reporting](../../security/advisories/new)
  for this repository (preferred), or
- The contact form at [zygig.com/#contact](https://zygig.com/#contact)

Please include:

- Which tool/file is affected
- Steps to reproduce
- Impact (e.g. data exfiltration, XSS, malicious script generation)

We'll acknowledge reports as soon as possible and aim to ship a fix
promptly given the small, static nature of this codebase.

## Scope

In scope:

- Any code path that sends data off-device without explicit user action
  (e.g. clicking a link to an external site)
- XSS or script-injection issues in a tool's UI
- Supply-chain concerns (e.g. a tool pulling in a remote/unpinned script)

Out of scope:

- The correctness of scripts a tool *generates for you to run elsewhere*
  (e.g. the PowerShell output of SP Version Cleanup) — review generated
  scripts before running them in your own environment, as noted in each
  tool's disclaimer.
- Issues in third-party sites linked from the footer/nav (zygig.com).
