# Horchata Cafe

Sweet cinnamon! A food blog, migrated from WordPress to Jekyll + GitHub Pages.

## Structure

- `_posts/` — published posts (Markdown, one file per post)
- `_drafts/` — unpublished drafts (not built into the site)
- `assets/images/` — photos, organised by year/month as on the old site
- `_layouts/`, `assets/css/` — the site's look and feel
- `privacy-policy.md` — draft page, `published: false` keeps it off the site

## Publishing on GitHub Pages

1. Create a repository on GitHub and push this folder to it.
2. In the repo: **Settings → Pages → Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
3. The site appears at `https://<username>.github.io/<repo>/` a minute or two later.
4. If the repo is NOT named `<username>.github.io`, set `baseurl: /<repo>` in `_config.yml`.

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
