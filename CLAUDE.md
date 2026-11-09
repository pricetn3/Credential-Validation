# Credential Validation prototype

Live prototype published with GitHub Pages. The owner is a designer, not a developer: explain things in plain language and preview changes before publishing.

## How the page gets here
- `Main.dc.html`, `support.js`, `vendor/`, `ds/` and `assets/` are an **export from Claude Design**: board 1 of the Credential Validation canvas (https://claude.ai/artifact/6npDNv2EhkjjiWLFzegjyc), downloaded with the board's download button › **HTML (.zip)**.
- Publish the export **exactly as exported**. Don't hand-edit it or add links to it; changes are made on the canvas and re-exported.
- **One exception, still to carry over:** on 2026-11-09 the canvas couldn't be reached, so two changes were made by hand in `Main.dc.html`. They are the page container (`.cv-page`: 1160px wide and centered, 94% of the window below 1260px, 90% below 760px, matching the developed site; outer padding `48px 0 64px`) and the Paradigm logo at 48px tall (was 32px). Make the same changes on the canvas before the next export, or the next export will undo them.
- `index.html`, `README.md` and this file are hand-written and can be edited directly.
- The prototype's job is to show the new Experiential Learner Record button on the existing page. It isn't tied to the CC Design System: don't link it to the shared tokens or run the design system's drift check on it.

## Accessibility standard
Everything here must meet **WCAG 2.2 AA** (the most recent WCAG version at level AA). Flag anything that doesn't, in plain language with the criterion number, even when it wasn't asked about.

## Previewing
Serve the folder over HTTP rather than opening the file (the runtime's scripts need it): `python3 -m http.server` in this folder, then open http://localhost:8000.

## Publishing
This terminal has no GitHub sign-in (company-managed Mac, no admin rights). Commit on a branch, merge it into `main`, then ask the owner to click **Push origin** in GitHub Desktop. GitHub Pages goes live about 30 seconds later.
