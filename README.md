# Knowledge Journal (Quarto Blog)

This repository is a clean Quarto website configured as a blog.

## Prerequisites
- Install Quarto: https://quarto.org/docs/get-started/

## Develop
- Preview locally: `quarto preview`
- Render site: `quarto render`

## Create a New Post
1. Create a file in `posts/` named like `YYYY-MM-DD-title.qmd`.
2. Add front matter:

   ```
   ---
   title: "Your Title"
   date: 2025-01-15
   categories: [tag1, tag2]
   ---
   ```

3. Write your content in Markdown/Quarto.

The home page (`index.qmd`) lists posts from `posts/`, supports categories and an RSS feed.

## Changelog Automation
- Install [git-cliff](https://github.com/orhun/git-cliff) (`cargo install git-cliff` or grab a prebuilt binary) to generate release notes locally.
- Run `git cliff --unreleased --output CHANGELOG.md` to refresh the changelog before opening a PR.
- A GitHub Action keeps the changelog in sync during releases.
