# Huang MEGA Lab website

Source of <https://ythuangmyco.github.io> (GitHub Pages, Jekyll, [Beautiful Jekyll](https://beautifuljekyll.com) 3.0 theme).
Pushing to `main` publishes the site within ~1 min.

## Routine edits

| Task | Where |
|---|---|
| Add / move a member | `_data/members.yml` — one entry per person; set `section` (`pi`, `postdoc`, `phd`, `master`, `undergrad`, `visiting`, `alumni`). Alumni get `years:`. The Members page (`pages/member_future.md`) renders from this file; never edit its HTML. |
| Member profile page | `pages/people/<name>.md`, copy `Amira_Ibrahim.md` as template. Photo: `assets/img/people/<name>_500.jpg` (500 px tall) shown on the page, `<name>_circular_200.png` (200×200 circle) on the grid. Ask members for one original ≥1000×1500 px; derive both crops. |
| Add a paper | `_data/publications.yml` — add at the top: `year`, `citation` (Markdown; `**Huang, Y.-T.#**` = corresponding), `url`. |
| News post | `_posts/posts/YYYY-MM-DD-slug.md`, front matter like the existing ones (`thumbnail-img`, `tags`). Appears on the home page. |
| Research project | `_posts/research_posts/…md` with `categories: research_posts`. Appears on `/research` only. |
| Protocols | `pages/protocol.md` (links to protocols.io). |
| Navigation, colours, analytics | `_config.yml` (`navbar-links`, `*-col`, `analytics`). |

Images: keep ≤1600 px on the long side, JPEG for photos, PNG only when transparency is needed. No spaces in filenames.

Unpublished drafts (`published: false` in front matter, kept for reference): TFDCS citizen-science pages, `UMHome`, `LoginPage`/`LogoutPage`, `test.md`, `pages/ambrosia_symbiosis/`.

## Local preview

```bash
docker run --rm -p 4000:4000 -v "$PWD":/srv/jekyll jekyll/jekyll:latest \
  bash -c "gem install jekyll-paginate jekyll-sitemap jekyll-seo-tag --no-document; jekyll serve --future --host 0.0.0.0"
```
Then open <http://localhost:4000>. (GitHub Pages itself builds with the `github-pages` gem from `Gemfile`.)
