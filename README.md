# Horchata Cafe

Sweet cinnamon! A food blog, migrated from WordPress to Jekyll + GitHub Pages.

## Structure

- `_posts/` — published posts (Markdown, one file per post)
- `_drafts/` — unpublished drafts (not built into the site)
- `assets/images/` — photos, organised by year/month as on the old site
- `_layouts/`, `assets/css/` — the site's look and feel
- `privacy-policy.md` — draft page, `published: false` keeps it off the site

## Publishing on GitHub Pages

The repo is https://github.com/stuartrivero/horchatacafe and `_config.yml` is already set for it.

1. Push this folder to the repo (see below).
2. On GitHub: **Settings → Pages → Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
3. The site appears at **https://stuartrivero.github.io/horchatacafe/** a minute or two later.

To push from this folder:

```sh
git remote add origin https://github.com/stuartrivero/horchatacafe.git
git push -u origin main
```

## Writing a new post

Add a file `_posts/YYYY-MM-DD-some-title.md`:

```markdown
---
layout: post
title: "Some title"
date: 2026-08-26 12:00:00 +0000
---

Text here. Images go in assets/images/ and are embedded with:

![photo]({{ site.baseurl }}/assets/images/2026/08/photo.jpg)
```

Push to `main` and GitHub Pages rebuilds automatically.

## Local preview (optional)

```sh
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.
