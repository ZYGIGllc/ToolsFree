# ToolsFree

Free, client-side browser tools from [zygig](https://zygig.com). No sign-up,
no data collected — everything runs locally in your browser.

**Live**: https://zygigllc.github.io/ToolsFree/ — a landing page (`index.html`)
listing all available tools.

## Structure

```
index.html              landing page — directory of all tools (don't repurpose)
tools/
  <tool-slug>/
    index.html           the tool itself, self-contained (inline CSS/JS)
    ...                  any assets the tool needs, kept alongside it
```

Each tool lives in its own folder under `tools/`, so it can be added,
reviewed, and committed independently of the others.

## Tools

### SP Version Cleanup (`tools/sp-version-cleanup/`)

A SharePoint Online version-management script generator. Generates
ready-to-run PowerShell scripts for intelligent versioning, cleanup,
auditing, and bulk operations across SharePoint Online — entirely
client-side, nothing is uploaded or stored.

**Live**: https://zygigllc.github.io/ToolsFree/tools/sp-version-cleanup/

## Adding a new tool

1. Create `tools/<tool-slug>/index.html` (plus any assets it needs, in the
   same folder). Keep each tool self-contained — inline CSS/JS, no build
   step — so it can be opened directly or served as a static page.
2. Add a card for it in the root `index.html`'s tool grid, linking to
   `tools/<tool-slug>/`.
3. Link it from this README.
4. Commit the new folder on its own.

It's then reachable at
`https://zygigllc.github.io/ToolsFree/tools/<tool-slug>/` once GitHub Pages
is enabled.

## Hosting (GitHub Pages)

This repo is meant to be served via GitHub Pages:

1. Push `index.html`, `tools/`, and this README to `main`.
2. In the repo's **Settings → Pages**, set **Source** to "Deploy from a
   branch", branch `main`, folder `/ (root)`.
3. The landing page goes live at `https://zygigllc.github.io/ToolsFree/`.

## Contributing

Contributions are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md) for the
ground rules (client-side only, no data collection, self-contained tool
folders) and how to add a tool. Please also review our
[Code of Conduct](CODE_OF_CONDUCT.md).

## Security

Found a security issue? Please see [SECURITY.md](SECURITY.md) rather than
opening a public issue.

## License

MIT — see [LICENSE](LICENSE). © 2026 zygig.
