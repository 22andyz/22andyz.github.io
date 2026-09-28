# Personal Site (Jekyll)

## Run locally

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000

## Structure

- `_config.yml` — site title, author info, plugins
- `_layouts/` — `default.html` (base), `post.html`, `project.html`
- `_includes/` — `header.html`, `footer.html`
- `_posts/` — photography posts, filename format `YYYY-MM-DD-title.md`, listed at `/photography/`
- `_projects/` — project entries (a Jekyll collection), rendered at `/projects/<slug>/`
- `_other/` — miscellaneous posts (a Jekyll collection), rendered at `/other/<slug>/`
- `_sass/main.scss` + `assets/css/style.scss` — styling
- `index.md`, `contact.md`, `cv.md`, `photography/index.md`, `projects/index.md`, `other/index.md` — pages

## Customize

1. Edit `_config.yml`: title, tagline, description, `url`, and your GitHub/Twitter/LinkedIn handles under `author`.
2. Replace the placeholder text in `index.md` (this is now both the homepage and the "About Me" content) and `contact.md`.
3. Delete `_posts/2026-01-15-welcome-to-my-site.md` and `_projects/example-project.md` once you've added your own.
4. Colors/fonts live in `_sass/main.scss` under the `$variables` at the top.

## Deploy

**GitHub Pages:** push to a repo named `<username>.github.io` (or enable Pages on any repo and set the source to your branch). Set `url` in `_config.yml` to the Pages URL.

**Other hosts (Netlify, Vercel, etc.):** build command `bundle exec jekyll build`, publish directory `_site`.
