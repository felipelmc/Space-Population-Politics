# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this project is

A [Quarto](https://quarto.org) book site containing lecture notes for the graduate course **Espaço, População e Política** (Space, Population and Politics) at IESP-UERJ. Notes are written in Portuguese and published to GitHub Pages via the `docs/` output directory.

## Key commands

```bash
# Render the full book
quarto render

# Preview locally with live reload
quarto preview

# Render a single file
quarto render aulas/aula-02.qmd
```

The rendered output goes to `docs/` (configured in `_quarto.yml`), which is gitignored — GitHub Pages serves directly from that directory.

## Project structure

- `_quarto.yml` — book configuration: chapter order, theme, output format, bibliography
- `index.qmd` — course overview page (introduction, syllabus, reading list)
- `aulas/aula-NN.qmd` — one file per lecture; add new lectures here and register them in `_quarto.yml` under `book.chapters`
- `references.bib` — BibTeX bibliography; all `@citekey` references in `.qmd` files must have entries here
- `custom.scss` — custom styles layered on top of the `cosmo` Bootstrap theme
- `pdfs/` — course PDFs (gitignored, not served)
- `presentation/` — standalone Quarto presentation files (not part of the book)

## Adding a new lecture

1. Create `aulas/aula-NN.qmd` with YAML front matter (`title`, `date`).
2. Add the path to the `chapters` list in `_quarto.yml`.
3. Add any new bibliography entries to `references.bib`.

## Citation style

References use Pandoc citation syntax (`@citekey` or `[@citekey, p. X]`). The bibliography is rendered automatically at the end of each page.
