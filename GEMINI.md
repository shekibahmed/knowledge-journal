# Gemini Customization

This file provides instructions to Gemini on how to interact with this project.

## Project Overview

This is a Quarto blog project. The main technologies used are Quarto and Markdown. The website is generated in the `docs` directory.

## Project Structure

- `_quarto.yml`: The main configuration file for the Quarto project.
- `index.qmd`: The home page of the blog, which lists all the posts.
- `posts/`: This directory contains the blog posts as `.qmd` files.
- `docs/`: This directory contains the generated website. It is the output directory for the Quarto project.
- `images/`: This directory contains images used in the blog.
- `styles.css`: This file contains the custom CSS for the blog.

## How to create a new post

1.  Create a new file in the `posts/` directory with the name `YYYY-MM-DD-title.qmd`.
2.  Add the following front matter to the file:

    ```yaml
    ---
    title: "Your Title"
    date: YYYY-MM-DD
    categories: [tag1, tag2]
    ---
    ```

3.  Write the content of the post in Markdown.

## Development

- To preview the website locally, run the command `quarto preview`.
- To render the website, run the command `quarto render`.
