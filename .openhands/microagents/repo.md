# Repository Information

This repository contains the source code for Xuhui's personal academic website. It is built using Jekyll and the al-folio theme, which is designed for academics to showcase their research, publications, and other professional activities.

## General Setup:

To set up and run the website locally:

1. Install Ruby and Bundler if not already installed.
2. Run `bundle install` to install the required gems.
3. To serve the website locally, use the command:
   ```
   bundle exec jekyll serve -P 12000 --lsi --host 0.0.0.0
   ```
   This will start the server on port 12000 and enable Latent Semantic Indexing (LSI).

## Adding New Papers:

To add new papers to the website:

1. Edit the `_bibliography/papers.bib` file.
2. Add a new BibTeX entry for each paper.
3. You can include additional fields like `paper`, `code`, `website`, etc., to provide links to resources.
4. The `abbr` field can be used to specify how the paper should be categorized (e.g., "Preprint", "ICLR 2025").
5. After adding new entries, you may need to update the year sections if papers are from a new year.

## Repository Structure:

- `_bibliography/`: Contains the BibTeX file for publications.
- `_pages/`: Contains Markdown files for various pages of the website.
- `_posts/`: Contains blog posts.
- `_projects/`: Contains information about research projects.
- `assets/`: Contains static assets like images, CSS, and JavaScript files.
- `_config.yml`: The main configuration file for the Jekyll site.
- `_data/`: Contains YAML files with additional data for the site.
- `_includes/` and `_layouts/`: Contains HTML templates for the site structure.
- `_sass/`: Contains SCSS files for styling.

## CI/CD:

There are no specific GitHub Actions workflows in the `.github/` directory. However, it's recommended to:

1. Run `bundle exec jekyll build` locally to ensure the site builds correctly before pushing changes.
2. Test the site locally using `bundle exec jekyll serve` to check for any visual or functional issues.

## Deployment:

Use ./bin/deploy --user to deploy

Remember to update the `_config.yml` file if you need to change any site-wide settings or configurations. Also, be cautious when modifying theme files, as it may affect the overall layout and functionality of the website.