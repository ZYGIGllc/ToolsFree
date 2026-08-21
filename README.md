# ToolsFree

Free, client-side browser tools from [zygig](https://zygig.com). No sign-up,
no data collected — everything runs locally in your browser.

## Tools

### SP Version Cleanup

A SharePoint Online version-management script generator. Generates
ready-to-run PowerShell scripts for intelligent versioning, cleanup,
auditing, and bulk operations across SharePoint Online — entirely
client-side, nothing is uploaded or stored.

**Live**: https://zygigllc.github.io/ToolsFree/

## Adding a new tool

Each tool is a single self-contained HTML file (inline CSS/JS, no build
step) so it can be opened directly or served as a static page. To add one:

1. Drop the `.html` file at the repo root (or a subfolder if it needs
   assets alongside it).
2. Link it from this README.
3. If it should be the default landing page, name it `index.html`; otherwise
   it's reachable at `https://zygigllc.github.io/ToolsFree/<filename>.html`
   once GitHub Pages is enabled.

## Hosting (GitHub Pages)

This repo is meant to be served via GitHub Pages:

1. Push `index.html` (and this README) to `main`.
2. In the repo's **Settings → Pages**, set **Source** to "Deploy from a
   branch", branch `main`, folder `/ (root)`.
3. The tool goes live at `https://zygigllc.github.io/ToolsFree/`.

## License

© 2026 zygig. All rights reserved.
