# joseramonmoran.github.io

Personal academic website for José Ramón Morán, built on the
[Academic Pages](https://github.com/academicpages/academicpages.github.io) Jekyll
template (a fork of Minimal Mistakes) and hosted on GitHub Pages.

Live at <https://joseramonmoran.github.io>.

## How to edit

Everything is a plain text file. Push to `main` and GitHub Pages rebuilds the site
automatically, usually within a minute.

| What you want to change | File to edit |
| --- | --- |
| Name, bio, email, social links, site title | `_config.yml` (the `author:` block near the top) |
| Top menu items | `_data/navigation.yml` |
| Front page text and featured papers | `_pages/about.md` |
| Research page extras (presentations, referee service) | `_pages/research.html` |
| Teaching page | `_pages/teaching.html` |
| CV page | `_pages/cv.md` |

### Adding a paper

Create a file in `_publications/` named `YYYY-MM-DD-short-slug.md`:

```yaml
---
title: "Paper Title"
collection: publications
category: workingpapers      # workingpapers | wip | published
permalink: /publication/YYYY-MM-DD-short-slug
date: YYYY-MM-DD
coauthors: "Name One and Name Two"        # optional
status: "Revise and Resubmit, *Journal*"  # optional
paperfile: Paper.pdf                      # optional; a PDF in the papers repo
# paperurl: 'https://...'                 # optional; use instead of paperfile for an external link
# slidesurl: 'https://...'                # optional
---

**Abstract.** ...
```

Papers are listed newest first *within* each category, ordered by `date`. The
category headings and their order come from `publication_category` in `_config.yml`.

Note that YAML front matter is **not** processed by Liquid, so `{{ site.papersurl }}`
does not work there. Put the bare filename in `paperfile` and the template builds the
full URL; use `paperurl` only for links outside the papers repo (e.g. an IMF or journal
page).

### Paper PDFs

PDFs live in the separate [`joseramonmoran/papers`](https://github.com/joseramonmoran/papers)
repo on its `gh-pages` branch, and are served from
<https://joseramonmoran.github.io/papers/>. The `papersurl` variable in `_config.yml`
points there, so `{{ site.papersurl }}/ROO_v3.pdf` resolves to the right URL. To add a
new paper, upload the PDF to that repo and reference it the same way.

### Adding a photo

Drop a square image into `images/` and set `avatar` in the `author:` block of
`_config.yml` to its filename. Until then, the profile block renders without a photo.

## Running it locally (optional)

Requires Ruby.

```sh
bundle install
bundle exec jekyll serve -l -H localhost
```

Then open <http://localhost:4000>.
