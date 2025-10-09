# Repository Guidelines

Complement this guide with the broader project overview in [README.md](README.md).

## Project Structure & Module Organization
- Core pages live in `index.qmd` and `about.qmd`; individual posts reside in `posts/` (defaults set via `posts/_metadata.yml`).
- Topic landing pages live under `topics/`; shared assets belong in `images/` and `resources/`.
- Project-wide configuration sits in `_quarto.yml`, with visual tweaks handled by `styles.css`.
- Rendered output belongs in `docs/`; treat it as build artifacts and edit only when publishing updates.

## Build, Test, and Development Commands
- `quarto preview` launches a live-reloading dev server in your browser.
- `quarto render` produces the production build inside `docs/`; use before shipping changes.
- `quarto check` validates links, syntax, and project health—run before review.
- `git cliff --unreleased --output CHANGELOG.md` refreshes `CHANGELOG.md` with unreleased entries.

## Coding Style & Naming Conventions
- Author posts as `YYYY-MM-DD-title.qmd`; keep filenames lowercase and kebab-cased.
- Start each `.qmd` with front matter containing `title`, `description`, `date`, and `categories`.
- Prefer concise, active prose; wrap lines near 80 chars to ease reviews.
- Provide descriptive image alt text (`![Brief context](images/example.png)`) and keep Markdown accessibility-friendly.

## Testing Guidelines
- Run `quarto check` for structural validation; investigate and resolve all warnings.
- Manually confirm visual changes via `quarto preview`, focusing on navigation, typography, and internal links.
- No automated unit tests exist—document manual verification steps in your PR.

## Commit & Pull Request Guidelines
- Use present-tense, conventional commits where possible (e.g., `feat: add tiling post layout`).
- Open PRs from topic branches such as `feature/post-topic` or `fix/navigation-bug`.
- Summarize user-facing changes, list validation steps (commands run, screenshots if UI shifts), and link any related issues.
- Before requesting review, ensure `CHANGELOG.md` is current, source files are formatted, and only relevant artifacts are staged.
