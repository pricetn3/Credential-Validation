# Credential Validation prototype

Interactive prototype of the Credential Validation page: enter a CeDiD, select **Validate**, and see the result.

**Open it:** `index.html` (it forwards to `Main.dc.html`). Once GitHub Pages is on, the site's main address opens the prototype.

## Using the prototype

- **Validate** fills in a CeDiD and shows the result.
- The **Prototype** panel on the right:
  - **State** jumps to *Before validating*, *Valid credential* or *Cannot validate*.
  - **Valid CeDiD** switch (on by default): on shows a valid credential, off shows the "cannot validate" message.
  - The × closes the panel; the tab on the right edge brings it back.

## What's here

| File or folder | What it is |
|---|---|
| `Main.dc.html` | The prototype page, exported from the Credential Validation canvas in Claude Design (board 1) |
| `index.html` | Forwards to `Main.dc.html` |
| `support.js`, `vendor/` | The Claude Design runtime that renders the page (and React) |
| `ds/cc/` | The CC Design System files the page uses |
| `assets/` | The Paradigm and CHEA logos |
| `EXPORT-README.md` | Claude Design's notes on the export |

## Design system

Built with the [CC Design System](https://pricetn3.github.io/CC-Design-System/). `Main.dc.html` also loads the shared `tokens.css` from that site, so token changes there reach this page with no push here.

## Source

Master: the **Credential Validation** canvas in Claude Design. Make changes there, then re-export board 1 (its download button › HTML (.zip)) and replace these files.
