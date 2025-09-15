# Knowledge Journal (fast_template)

This site uses [fast_template](https://github.com/fastai/fast_template), a Quarto-based template for blogs, notes, and documentation.

## Quick start

- Edit `index.md` to adjust the homepage and post listing.
- Add new posts in `posts/` as `.qmd` or `.md` with YAML front matter.
- About page lives at `about.qmd`.
- Customize `_quarto.yml` for site metadata, navbar, theme, and footer.

## Deployment

- GitHub Actions renders and publishes to `gh-pages` via `.github/workflows/make_site.yml`.
- Ensure GitHub Pages is set to deploy from the `gh-pages` branch in repo settings.

## Local preview

- Install [Quarto](https://quarto.org).
- Run `quarto preview` in the repo root to serve locally.
