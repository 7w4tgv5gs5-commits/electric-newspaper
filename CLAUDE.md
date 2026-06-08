# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Project Is

A static HTML archive of *The Electric Newspaper* — Adelaide's first independent online daily newspaper (February–July 1998), restored from the original Internode Unix server tar file and published to GitHub Pages. No build system, no dependencies, no package manager. Everything is plain HTML, CSS, and vanilla JavaScript.

## Viewing the Site

Open `index.html` in a browser directly, or serve locally to avoid iframe restrictions:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

GitHub Pages live site is at the URL in `README.md`.

## File Structure

- **`index.html`** — Entrance page: brief intro, Enter the Archive button, stats, learn-more ToC, and section links
- **`about.html`** — About the Electric Newspaper: what it was, where it came from, why it matters, origin & context
- **`history.html`** — Origin & Content: timeline, the people (full contributor profiles), and the stories that defined the paper
- **`restoration.html`** — About This Archive: how the 1998 Unix server tar file was recovered and restored
- **`articles.html`** — Searchable/sortable article index; all article metadata is embedded as a JavaScript array with client-side filtering (no server required)
- **`netscape.html`** — Simulated Netscape Navigator 4 browser chrome; loads `archive/INDEX.HTM` in an iframe
- **`site.css`** — Shared stylesheet used by all site pages (index, about, history, restoration, articles)
- **`archive/`** — The complete 1998 newspaper content (711 HTML articles + images)

## Architecture Notes

**The Netscape simulation** (`netscape.html`) wraps the archive in an `<iframe>` and provides a working Back/Forward history stack, animated N logo, a location bar that shows the original `http://www.electric.on.net/` URLs (via `toRetroURL()`), and a fake progress bar. The `?page=` query parameter lets it deep-link directly to a specific article on load.

**The article index** (`articles.html`) embeds all article metadata inline as a JS array. If you add or rename articles, you must manually update this array. The table is client-side sorted and filtered — no server calls.

**Case sensitivity is critical.** The archive filenames are uppercase (`INDEX.HTM`, `NEWS/`, `BUTTONS/`) because the original Unix server was case-sensitive, and GitHub Pages runs on Linux (also case-sensitive). macOS is case-insensitive and will hide bugs locally. Always use the exact uppercase names when writing links or paths into archive files.

**Image path conventions in the archive:** Article files use relative paths to images. After the 2024 restoration, all broken 8-character-truncated filenames were remapped. The two genuinely missing files are `news/logosa4.jpg` and `news/newlogosmall1.gif` — don't attempt to recover these.

**The rollover button JavaScript** in archive article pages is the original Netscape 3-era script by Dave Sag and Mark King (Virtual Artists, 1997). It has been disabled for browser compatibility, with the original source preserved verbatim in HTML comments. Do not remove those comments.

## Deployment

Push to `main` — GitHub Pages deploys automatically. There are no build steps.

## Content Integrity Rule

The article text and body HTML inside `archive/` is original and must remain unmodified. The only permitted changes to archive article files are: image path corrections, navigation link fixes, and the already-applied rollover script disabling. Do not edit article prose.
