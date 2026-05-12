# Repository Guidelines

## Project Structure & Module Organization

This is an Academic Pages Jekyll site. Site configuration lives in `_config.yml`, with Docker-only overrides in `_config_docker.yml`. Content is organized as Jekyll collections: `_pages/` for static pages, `_posts/` for blog posts, `_publications/`, `_talks/`, `_teaching/`, and `_portfolio/` for academic profile content. Layout templates are in `_layouts/`, reusable snippets are in `_includes/`, data files are in `_data/`, and styles are in `_sass/` plus `assets/css/`. JavaScript sources are in `assets/js/`; `assets/js/main.min.js` is generated. Public downloads belong in `files/`, and images belong in `images/`.

## Build, Test, and Development Commands

- `bundle install`: install Ruby/Jekyll dependencies from `Gemfile`.
- `bundle exec jekyll serve -l -H localhost`: serve the site locally at `http://localhost:4000` with live reload.
- `docker compose up`: build and run the Jekyll container, also serving on port `4000`.
- `npm install`: install JavaScript tooling and browser libraries.
- `npm run build:js`: rebuild `assets/js/main.min.js` from vendored libraries and local JS.
- `npm run watch:js`: rebuild JavaScript when files under `assets/js/` change.

There is no dedicated automated test suite. Use a clean Jekyll build or local preview as the main validation step before opening a PR.

## Coding Style & Naming Conventions

Use two-space indentation for YAML, Liquid templates, Markdown front matter, SCSS, and JavaScript to match the existing project style. Keep collection item filenames date-prefixed where established, for example `_posts/YYYY-MM-DD-title.md`, `_talks/YYYY-MM-DD-talk-name.md`, and `_publications/YYYY-MM-DD-paper-title.md`. Keep front matter keys consistent with nearby examples. Edit source JavaScript such as `assets/js/_main.js`; regenerate `main.min.js` instead of hand-editing it.

## Testing Guidelines

Before submitting changes, run `bundle exec jekyll serve -l -H localhost` and check the affected pages in a browser. For configuration, layout, SCSS, or collection changes, confirm Jekyll starts without errors and generated navigation, links, and assets render correctly. For talk map changes, note that `.github/workflows/scrape_talks.yml` executes `talkmap.ipynb` on relevant pushes.

## Commit & Pull Request Guidelines

The Git history is minimal; use concise, imperative commit subjects such as `Update publication metadata` or `Fix talk map rendering`. PRs should follow `.github/PULL_REQUEST_TEMPLATE.md`: identify whether the change is a bug fix, enhancement, or documentation update; include a clear summary; and link related issues when applicable. Include screenshots for visible site changes and mention the local validation command used.
