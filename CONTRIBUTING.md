# Contributing to ToolsFree

Thanks for considering a contribution! This repo hosts small, free,
client-side browser tools — there's no build step and no backend, so the
bar to contribute is low.

## Ground rules

- **Client-side only.** No tool may call out to a server, load remote
  scripts/trackers, or transmit user input anywhere. Everything must work
  the same with the network disconnected after the page loads.
- **No data collection.** No analytics, no cookies, no fingerprinting.
- **Self-contained.** Each tool is a single folder under `tools/<slug>/`
  with an `index.html` that inlines its own CSS/JS (plus any local assets
  it needs alongside it). No package manager, no build pipeline.
- **No frameworks required.** Plain HTML/CSS/JS is preferred so a tool can
  be opened straight from disk or served as-is via GitHub Pages.

See `README.md` for the exact folder layout and how the landing page links
to each tool.

## Adding a new tool

1. Fork the repo and create a branch.
2. Add `tools/<tool-slug>/index.html` (self-contained, as above).
3. Add a card for it in the root `index.html`'s tool grid.
4. Add an entry under **Tools** in `README.md`.
5. Open a pull request. Please describe what the tool does and confirm it
   makes no network requests.

## Fixing/improving an existing tool

- Keep changes scoped to that tool's folder where possible.
- Preserve the "100% client-side, zero data collection" guarantee — this is
  the core promise of the project.
- If you're changing behavior a script generator produces (e.g. PowerShell
  output), call that out clearly in the PR description.

## Reporting bugs / suggesting tools

Open an issue using the templates under **Issues → New issue**. For
security-relevant reports, see `SECURITY.md` instead of a public issue.

## Code style

- 2-space indentation, UTF-8, LF line endings (see `.editorconfig`).
- Match the existing visual language (see the shared `.site-nav` /
  `.site-footer` styles in the current tool) unless there's a good reason
  to diverge.

## License

By contributing, you agree your contribution is licensed under this
repo's [MIT License](LICENSE).
