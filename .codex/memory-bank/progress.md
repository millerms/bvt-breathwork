```toml
[memory]
filetype = "progress"
priority = "medium"
```

# Progress

## What Works
- Minimal Mistakes theme configured; site structure in place.
- Modular SCSS components active; `.btn-modern` in use.
- Primary nav a11y improved; footer nav filters external links.
- Events list renders Upcoming/Past with robust filters.
- References component: PubMed/PMC links correct; badges only for PubMed.

## In Progress
- Meta, SEO, and a11y audit for completeness.
- Developer documentation for local setup and troubleshooting.

## Blockers
- Local build on Ruby 2.6.x fails due to gem constraints — upgrade Ruby to
  3.1.x recommended (use rbenv/asdf), then `bundle install`.

## Upcoming
- Validate dark mode styles across key pages.
- Ensure JS loads non-blocking and remains accessible.
- Add Events tag filters with `.chips` (optional).

## Known Issues
- Resolved duplicate `custom.css` inclusion (no default page-level css).
- Fixed Liquid parsing errors on events by splitting `where_exp` conditions.
- Fixed reference links and removed empty PMID badges.
