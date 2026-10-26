# JT App Manager — J Tech Digital World

JT App Manager is the JT product catalogue and local rollout checklist. This starter provides:

- Searchable and category-filtered catalogue for the JT ecosystem
- Source repository, Actions/build, and Releases links for each product
- A local review/configuration checklist and notes
- JSON export of the catalogue and checklist
- Print-friendly overview and responsive Electron desktop shell

## Important boundaries

The checklist is not proof that an app is installed or that CI passed. This version does not scan installed software, execute installers, verify signatures, silently install updates, or apply updates. Build status and release availability must be confirmed in each product's own GitHub repository. It does not fetch live statuses in the background.

## Development

Requires Node.js 20+.

```bash
npm install
npm run check
npm start
```

Browser mode: `npm run serve`, then open http://localhost:4173.
Desktop packaging: `npm run dist`.

## Builds

GitHub Actions attempts Windows x64/x86/ARM64, macOS Intel/Apple Silicon, and Linux x64/ARM64 artifacts. Only use a platform package after its individual CI job succeeds and the artifact is checked. The workflow uploads temporary build artifacts only and never publishes GitHub Releases automatically. Packages are unsigned by default; macOS signing/notarization is not configured.

The JT product catalogue intentionally does not install or run code without an explicit user action. Future update support should verify package signatures/checksums and require confirmation before installation.
