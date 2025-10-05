# Agent Operating Guide

## Project Context
- Quarto-powered digital garden and blog.
- Source content lives in `.qmd` files; rendered output resides in `docs/` (keep hands off unless publishing).
- Markdown, YAML front matter, and lightweight CSS are the dominant technologies.

## Primary Objectives
- Understand each request before editing; inspect related files when unsure.
- Preserve the editorial voice: concise, friendly, active, and informative.
- Keep the workspace tidy—prefer small, focused changes and avoid collateral edits.
- Surface risks, open questions, and validation steps to the user.

## Workflow Expectations
1. **Assess the task**
   - Review `README.md` or relevant `posts/`, `topics/`, or config files for context.
   - Confirm whether work touches content, configuration, or build assets.
2. **Implement deliberately**
   - Respect front matter conventions (`title`, `description`, `date`, `categories`).
   - Keep Markdown accessible: add alt text, limit inline HTML, break long lines.
   - Avoid modifying the generated `docs/` directory; prefer source `.qmd` files.
3. **Validate and summarize**
   - Run `quarto preview`, `quarto render`, or `quarto check` when changes warrant it.
   - Report which commands ran (or why they were skipped) in the final message.
   - Highlight follow-up actions the user might consider (tests, publishing, etc.).

## Communication Style
- Lead with the outcome, then explain what changed and where.
- Reference files with repo-relative paths (e.g., `posts/2024-01-01-example.qmd`).
- Mention validation results and remaining uncertainties explicitly.
- Offer next-step suggestions only when they add value.

## Constraints & Non-Goals
- Do **not** delete or rename existing files unless explicitly instructed.
- Do **not** invent posts, data, or screenshots; work with repository assets.
- Treat `CHANGELOG.md` as source-of-truth; update via `git-cliff` if required.
- Respect the ASCII default—only introduce other characters when necessary.

## Handy References
- `README.md`: contributor quick start and repository etiquette.
- `_quarto.yml`: global site configuration and navigation.
- `posts/_metadata.yml`: default post options.
- `styles.css`: custom styling overrides.
- `resources/` & `images/`: storage for downloads and media.

## Pre-Submit Checklist
- [ ] Relevant files reviewed before editing.
- [ ] Changes confined to required scope (no stray whitespace or rebuild artifacts).
- [ ] Validation commands executed or consciously deferred.
- [ ] Final response notes changes, validations, and recommended next steps.