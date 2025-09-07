```toml
[memory]
filetype = "activeContext"
priority = "high"
```

# Active Context

## Current Focus
- Align site with modular design system (buttons, cards, accordion, tabs).
- Stabilize events listing and fix Liquid filters and collection wiring.
- Standardize references component behavior and links (PubMed/PMC).

## Recent Changes
- Home: migrated `feature_row` buttons to `.btn-modern`; removed legacy classes.
- SEO: added `seo: true` to public pages; confirmed head meta inclusion.
- Nav: added `aria-label` to primary nav; support `rel`; filtered footer nav
  using `footer: false` in `_data/navigation.yml` and removed Instagram from
  footer follow icons.
- Events: declared `events` collection in `_config.yml`; fixed Liquid errors by
  splitting `where_exp` filters; guarded `site.events` nil case.
- Build: corrected `minimal_mistakes_skin` and Gemfile (use `github-pages`; add
  `webrick`); recommend Ruby ≥ 3.1 for local parity.
- References: rebuilt include + JS
  - Prefer explicit `url`; PubMed URL only for digits-only `pmid`.
  - Removed Copy and Back links; hide DOI by default.
  - Added booleans `show_pmid`/`show_doi` (site defaults; per-include override).
  - Badge renders only when enabled and valid PMID; no empty badges.

## Next Steps
- Optional: add `.chips` filters on Events; sample tag taxonomy.
- Add a short DEV.md with Ruby 3.1+ setup and common commands.
- Run Lighthouse and record issues in `progress.md`.

## Decisions & Preferences
- Keep overrides minimal; prefer theme-supported hooks.
- Use conventional commits and document non-obvious choices here.
