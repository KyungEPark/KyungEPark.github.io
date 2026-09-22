# kyungepark.github.io

Personal academic website of Kyung eun (Trixie) Park — live at
<https://kyungepark.github.io>.

Built with [Academic Pages](https://github.com/academicpages/academicpages.github.io),
a Jekyll template, and served by GitHub Pages. Pushing to `master` rebuilds
the site automatically; no local build is required.

## Where things live

| What | Where |
| --- | --- |
| Site settings, sidebar profile, social links | `_config.yml` |
| Top navigation menu | `_data/navigation.yml` |
| Homepage / about text | `_pages/about.md` |
| CV | `_pages/cv.md` |
| Publications | `_publications/*.md` |
| Talks | `_talks/*.md` |
| Teaching | `_teaching/*.md` |
| Blog posts | `_posts/YYYY-MM-DD-slug.md` |
| PDFs and other downloads | `files/` (served at `/files/<name>.pdf`) |
| Images | `images/` |

## Adding a publication

Create `_publications/<year>_<name>.md`:

```yaml
---
title: "Paper title"
collection: publications
permalink: /publication/2025_example
date: 2025-01-01          # must be a full date, not a bare year
venue: 'Journal name'
paperurl: 'https://doi.org/...'   # optional, adds a "Download Paper" link
citation: 'Full citation text.'
---
```

Note the `date` field: a bare `2025` is parsed as a number and rendered as
1970, so always write the full `YYYY-MM-DD`.

## Adding a blog post

Copy `_drafts/post-template.md` into `_posts/` and rename it
`YYYY-MM-DD-slug.md`:

```yaml
---
title: 'Post title'
date: 2026-01-01
permalink: /posts/2026/01/slug/
tags:
  - entrepreneurship
---
```

Layout, sidebar and reading time come from the `defaults` block in
`_config.yml`, so they do not need to be set per post. Keep the filename
date and the `date` field in agreement, and give every post a unique
`permalink` - duplicates silently overwrite one another.

Posts appear at `/year-archive/`, linked as "Blog Posts" in the nav.

## Local preview (optional)

Requires Ruby. Without it, just push and let GitHub build.

```sh
bundle install
bundle exec jekyll serve -l -H localhost
```
