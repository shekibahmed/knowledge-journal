# Knowledge Journal Contributor Guide

## Purpose
This document equips new and returning contributors to work efficiently on the Knowledge Journal, a Quarto-powered digital garden. Follow the steps below to keep content consistent, accessible, and easy to publish.

## Quick Start Checklist
- Install [Quarto](https://quarto.org/docs/get-started/) locally; ensure `quarto --version` works.
- Clone the repository and switch to a feature branch named after your change (e.g., `feature/add-neural-notes`).
- Run `quarto preview` to verify the site builds before editing anything.
- Keep `docs/` untouched unless you intentionally render a production build.

## Repository Layout At a Glance
- `index.qmd` — landing page content and featured listings.
- `about.qmd` — profile/about section; keep tone in sync with the main site.
- `posts/` — dated `.qmd` entries. `_metadata.yml` sets default options for the folder.
- `images/` — canonical image assets. Prefer relative references like `images/diagram.png`.
- `assets/` — downloadable files (PDFs, datasets). Organize them by topic folders if volume grows.
- `_quarto.yml` — project configuration (navigation, theme, listings, formats).
- `_site/` — Quarto preview output. Safe to delete; never commit.
- `docs/` — production build for GitHub Pages. Commit only when intentionally publishing.

## Writing Workflow
1. Create a draft file under `posts/YYYY-MM-DD-descriptive-title.qmd` using ISO date prefixes and kebab-case slugs.
2. Copy YAML front matter from a recent post or rely on `_metadata.yml` defaults; add `title`, `description`, and optional `categories`.
3. Structure content using Markdown headings. Keep paragraphs short and embed callouts or code blocks when they improve clarity.
4. When code should not execute during build, add `execute: false` at the chunk or document level.
5. Run `quarto preview` to confirm formatting, link targets, and navigation entries render correctly.

## Style & Accessibility Guidelines
- Use active voice, concise sentences, and descriptive headings (≤60 characters when possible).
- Limit lines to ~80 characters to ease diff reviews.
- Provide alt text for every image (`![Alt text](images/figure.png)`).
- Prefer absolute URLs for external references and relative links for internal cross-links (`[link](../posts/...)`).
- Include callouts (`::: {.callout-note}`) only when they add value; keep them short.

## Working With Media & Assets
- Place reusable images in `images/`; keep filenames kebab-case and descriptive.
- Large media (video, notebooks) should live in external storage; link rather than commit when files exceed a few MB.
- Compress images before committing. Aim for <500 KB PNG/JPEG when practical.
- When adding downloadable files, update any referencing posts to link via `assets/` paths.

## Build & Validation Commands
- `quarto preview` — live reload during writing; safe for continuous use.
- `quarto render` — produce a production-ready build in `docs/`. Run before publishing.
- `quarto check` — catch metadata, link, and dependency issues; run before opening a PR.

## Collaboration & Git Hygiene
- Write commits in present tense under ~60 characters (e.g., `add transformer memory post`).
- Group related edits (post content + images) into a single commit or PR to keep history coherent.
- Rebase or merge `main` before requesting review; resolve conflicts locally.
- For PR descriptions, include: summary of changes, rendered screenshots if visual updates, and mention any follow-up work.
- Avoid committing `_site/` output or temporary notebooks; add `.gitignore` entries if necessary.

## Publishing Workflow
1. Ensure `quarto render` completes without errors and updates `docs/`.
2. Review the rendered site locally in `_site/` or `docs/` for layout regressions.
3. Commit updated source files and, if publishing, the regenerated `docs/` output.
4. Push your branch, open a PR, and request review from a maintainer.
5. Once approved, merge to `main` and deploy via GitHub Pages or `quarto publish gh-pages` as configured.

## Support & Resources
- Consult Quarto documentation for format-specific questions: <https://quarto.org/docs/>
- Check existing posts for tone, structure, and metadata conventions before deviating.
- If you encounter build or dependency issues, open a discussion or issue with logs from `quarto check`.
