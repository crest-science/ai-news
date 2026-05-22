# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A single-page GitHub Pages site for a research laboratory, hosting AI-related
content (readings, article monitoring, notes). All content lives in `index.md`;
there are intentionally no per-area pages.

## Structure

- `index.md` — the entire site. Sections: **Latest News**, then one per laboratory
  area (Economy, Sociology, Statistics, Finance, Administration). When adding
  content, append to the relevant section; do not split into separate files.
- `_config.yml` — Jekyll config. Uses the `minima` theme.
- The site is built and deployed by GitHub Pages from the default branch.

## Editing conventions

- Keep **Latest News** short; move older items into the relevant section.
- Section headings currently in use: Latest News, Collective discussion,
  Trainings & ressources. The originally-planned area sections (Economy,
  Sociology, Statistics, Finance, Administration) are not all present yet —
  preserve whatever sections exist and ask before reorganizing.
- Each entry is a single bullet: optional `DD/MM/YYYY:` prefix, then a
  Markdown link, then 1–3 shields.io badges on the same line.

### Badge convention

Use `https://img.shields.io/badge/<text>-<color>` (single-segment form).
For hyphens inside the text, double them (`claude--code` renders as
`claude-code`).

The **text** is a free-form keyword describing the content. The **color**
encodes the laboratory area the entry belongs to — all badges on a single
entry share the same color:

- **blue** — economy
- **orange** — sociology
- **green** — statistics (including mathematics / methodology)
- **yellow** — finance
- **lightgrey** — general / cross-cutting (tooling, tutorials, anything
  not tied to one area)

Keep to 1–3 badges per entry. If an entry spans multiple areas, pick the
dominant one; do not mix colors within a single entry.

## Local preview (optional)

GitHub Pages renders the site on push; no build step is required to ship changes.
To preview locally with Jekyll:

```
bundle init && bundle add jekyll
bundle exec jekyll serve
```
