# Knowledge Journal (Quarto)

This site now uses Quarto instead of Fastpages/Jekyll.

Quick start:

- Edit `index.md` to adjust the homepage and post listing.
- Add new posts under `posts/` as `.qmd` or `.md` with YAML front matter.
- About page lives at `about.qmd`.

Deploys:

- GitHub Actions renders and publishes to `gh-pages` via `.github/workflows/quarto-publish.yml`.
- Ensure GitHub Pages is set to deploy from the `gh-pages` branch in repo settings.

Local preview (optional):

- Install Quarto from quarto.org, then run `quarto preview` in the repo.
