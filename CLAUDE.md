# Credential Validation prototype

Live prototype published with GitHub Pages. The owner is a designer, not a developer: explain things in plain language and preview changes before publishing.

## How the page gets here
- `Main.dc.html`, `support.js`, `vendor/`, `ds/` and `assets/` are an **export from Claude Design**: board 1 of the Credential Validation canvas (https://claude.ai/artifact/6npDNv2EhkjjiWLFzegjyc), downloaded with the board's download button › **HTML (.zip)**.
- Don't hand-edit the export. Changes are made on the canvas and re-exported; edits here would be overwritten.
- After a new export, replace the files and re-add the shared-tokens line in `Main.dc.html`, right after the `ds/cc/tokens.css` link:
  `<link rel="stylesheet" href="https://pricetn3.github.io/CC-Design-System/tokens.css" data-cc-shared-tokens>`
  (`tools/link_tokens.py` in CC-Design-System only handles single-file exports, so it skips this page.)
- `index.html`, `README.md` and this file are hand-written and can be edited directly.

## Accessibility standard
Everything here must meet **WCAG 2.2 AA** (the most recent WCAG version at level AA). Flag anything that doesn't, in plain language with the criterion number, even when it wasn't asked about.

## Design system
Lives in `~/Documents/GitHub/CC-Design-System` (https://pricetn3.github.io/CC-Design-System/). Its `CLAUDE.md` has the full workflow. The master is the Credential Connections Design System in Claude Design.

The drift check (`python3 tools/drift_check.py <path to Main.dc.html>` from CC-Design-System) reports every built-in token as an error because this export writes colors as hex and the system writes `rgb()`. The values match; read the warnings instead.

## Previewing
Serve the folder over HTTP rather than opening the file (the runtime's scripts need it): `python3 -m http.server` in this folder, then open http://localhost:8000.

## Publishing
This terminal has no GitHub sign-in (company-managed Mac, no admin rights). Commit on a branch, merge it into `main`, then ask the owner to click **Push origin** in GitHub Desktop. GitHub Pages goes live about 30 seconds later.
