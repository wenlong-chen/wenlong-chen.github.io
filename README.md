# Documentation Site

This is a documentation site built with [Just the Docs](https://just-the-docs.com/), [Jekyll](https://jekyllrb.com/), and [GitHub Pages](https://pages.github.com/).

## Setup

1. Clone this repository
2. Install dependencies:
   ```bash
   bundle install
   ```
3. Run the site locally:
   ```bash
   bundle exec jekyll serve
   ```
4. Visit `http://localhost:4000` in your browser

## Deployment

This site is automatically deployed to GitHub Pages using GitHub Actions. Any push to the `main` branch will trigger a new deployment.

To set up GitHub Pages:

1. Go to your repository settings
2. Navigate to "Pages" section
3. Under "Build and deployment":
   - Source: Deploy from a branch
   - Branch: gh-pages / (root)

## Adding Content

1. Create new markdown files in the `docs` directory
2. Add front matter to your markdown files:
   ```yaml
   ---
   layout: default
   title: Your Page Title
   nav_order: 2
   ---
   ```
3. Write your content in markdown

## Customization

To customize the site:

1. Edit `_config.yml` for site-wide settings
2. Modify theme colors in `_sass/custom/custom.scss`
3. Add custom JavaScript in `_includes/head_custom.html`

## License

This project is open source and available under the [MIT License](LICENSE). 