# grok-trading-lab-2026

Static, content-only site published via GitHub Pages. It is a single landing page (`index.html`) plus standalone markdown report files. There is no build system, no package manager, and no application code in this repo — `index.html` pulls Tailwind from a CDN at runtime.

## Cursor Cloud specific instructions

- This repo is a **static site with no dependencies and no build step**. There is nothing to install; the "update script" is intentionally a no-op.
- `.nojekyll` is present, so GitHub Pages serves the files as-is (the `jekyll-docker.yml` workflow is CI only and does not affect how Pages serves this site). Do **not** add a Jekyll build to the local dev flow — serve the raw files instead.
- To run/preview locally in development, serve the repo root with a static file server, e.g. `python3 -m http.server 8000` (Python 3 is available), then open `http://localhost:8000/`. The markdown reports are reachable at e.g. `http://localhost:8000/stock-wheel-options-bots-report.md`.
- There are no automated tests, lint configs, or build commands. "Verifying" a change means serving the site and visually confirming `index.html` renders.
- Content is paper/simulation only and explicitly not financial advice — preserve the existing disclaimers when editing report content or `index.html`.
