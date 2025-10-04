# Knowledge Journal (Quarto Blog)

Welcome to the Knowledge Journal, a Quarto-powered blog and digital garden. This guide provides everything a new or returning contributor needs to work efficiently on this project.

## Prerequisites

Before you begin, make sure you have the following installed:

- **Quarto:** Follow the official instructions at [quarto.org/docs/get-started/](https://quarto.org/docs/get-started/) to install Quarto.
- **git-cliff:** This tool is used for automating changelog generation. Install it by running `cargo install git-cliff` or by downloading a pre-built binary from the [git-cliff releases page](https://github.com/orhun/git-cliff).

## Quick Start

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    ```
2.  **Create a new branch:**
    ```bash
    git checkout -b feature/your-change-name
    ```
3.  **Preview the site:**
    ```bash
    quarto preview
    ```
    This command starts a local server and automatically reloads the browser when you make changes.

## Repository Structure

-   `index.qmd`: The main landing page, which lists all blog posts.
-   `about.qmd`: The author's profile and about page.
-   `posts/`: Contains all the blog post files in `.qmd` format.
    -   `_metadata.yml`: Sets default options for all posts in this directory.
-   `topics/`: Contains topic-specific landing pages.
-   `images/`: Stores all image assets.
-   `resources/`: For downloadable files like PDFs or datasets.
-   `_quarto.yml`: The main Quarto project configuration file.
-   `styles.css`: Custom CSS for additional styling.
-   `docs/`: The output directory for the rendered production website. **Do not edit files in this directory directly.**

## Writing Workflow

1.  **Create a new post:** Create a file in the `posts/` directory using the naming convention `YYYY-MM-DD-your-title-in-kebab-case.qmd`.
2.  **Add front matter:** At the top of your new file, add a YAML front matter block. You can copy from an existing post or use the template below:
    ```yaml
    ---
    title: "Your Post Title"
    description: "A brief but informative description of your post's content."
    date: "YYYY-MM-DD"
    categories: [tag1, tag2]
    ---
    ```
3.  **Write your content:** Use Markdown to write your post.
4.  **Preview your work:** Use `quarto preview` to check for any formatting or rendering issues.

## Style and Accessibility

-   Write in an active voice with clear and concise sentences.
-   Keep line lengths to around 80 characters to make code reviews easier.
-   Provide descriptive alt text for every image: `![A description of the image](images/your-image.png)`.
-   Use absolute URLs for external links and relative paths for internal links.

## Media and Assets

-   Place all images in the `images/` directory.
-   Compress images before committing them to keep the repository lightweight.
-   For large files (videos, large datasets), host them externally and link to them in your posts.

## Build and Validation

-   `quarto preview`: For live-reloading during development.
-   `quarto render`: To generate a production build of the site in the `docs/` directory.
-   `quarto check`: To validate the project, checking for broken links and other common issues. Run this before submitting your work.

## Changelog and Collaboration

-   **Commit messages:** Write clear, present-tense commit messages (e.g., `feat: add new post on Quarto`).
-   **Changelog:** Before creating a pull request, update the changelog by running:
    ```bash
    git cliff --unreleased --output CHANGELOG.md
    ```
-   **Pull requests:** Ensure your branch is up-to-date with the `main` branch before submitting a pull request. Provide a clear summary of your changes in the PR description.

## Publishing

1.  Generate the final version of the site: `quarto render`.
2.  Commit the updated source files and the regenerated `docs/` directory.
3.  Push your changes and open a pull request.
4.  Once approved, your changes will be merged into `main` and deployed.

## Support

-   For questions about Quarto, consult the official [Quarto documentation](https://quarto.org/docs/).
-   For any issues with the repository, please open an issue on GitHub.