# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
quarto preview        # live preview in browser
quarto render         # build site to docs/
```

The site is deployed via GitHub Pages from the `docs/` output directory (configured in `_quarto.yml`).

## Architecture

This is a single-page Quarto academic website for Jared Kalow, a political science PhD candidate at MIT.

- **`index.qmd`** — the entire site content: bio, publications, working papers, research in progress, and teaching. This is the only page that matters; `about.qmd` is an unused placeholder.
- **`_quarto.yml`** — site config: output to `docs/`, site URL, navbar, Google Analytics, Plausible analytics, and CSS reference.
- **`style.css`** — all custom styles. Uses EB Garamond font, minimal layout (max-width 40em), firebrick (`#B22222`) headings with dotted underlines, and custom `<details>`/`<summary>` styling for collapsible abstracts.
- **`styles.css`** — empty (ignore).
- **`kalow_cv2.pdf`** — CV linked from the homepage; also copied into `docs/`.

Abstracts for publications and working papers use native HTML `<details>`/`<summary>` elements with a `.abstract` div inside. The CSS hides the default disclosure triangle and replaces it with `▾`/`▴` arrows via `::after`.
