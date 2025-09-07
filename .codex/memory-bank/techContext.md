```toml
[memory]
filetype = "techContext"
priority = "high"
```

# Tech Context

## Stack
- Jekyll via `github-pages` with Minimal Mistakes remote theme.
- Gems: `github-pages`, `jekyll-include-cache`, `webrick` (for Ruby ≥ 3).
- Structure: `_config.yml`, `_data/`, `_includes/`, `_layouts/`, `_pages/`, `assets/`.
- Assets: CSS/SCSS in `assets/css/` (e.g., `theme.css`, `custom.css`); JS in `assets/js/` (`reveal.js`, `tactile.js`).

## Local Dev
- Ruby: Prefer 3.1.x for dependency parity. Upgrade from 2.6.x to avoid
  nokogiri incompatibilities.
- Install: `bundle install`
- Clean caches: `bundle exec jekyll clean && rm -rf .jekyll-cache _site`
- Build: `bundle exec jekyll build`
- Serve: `bundle exec jekyll serve --livereload`
- Node (optional) for linting/formatting per `package.json`.

## Conventions
- Keep Liquid syntax intact; use theme’s includes and variables.
- Defer/async non-critical JS; avoid global leakage.
- Respect theme spacing/typography; keep SCSS nesting shallow.

## Config Flags
- `_config.yml`:
  - `minimal_mistakes_skin: default`
  - `references.show_doi: false`
  - `references.show_pmid: true`
  - `collections.events` declared with `output: true`

## Tools & Artifacts
- `lighthouse-a11y.json`: audit reference for accessibility improvements.
- `robots.txt`: ensure correct indexing policy for environment.
