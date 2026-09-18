# My New Site (Pixyll + GitHub Pages)

A minimal [Jekyll](https://jekyllrb.com) site using the
[Pixyll](https://github.com/johnotander/pixyll) theme, deployed with
[GitHub Pages](https://pages.github.com).

## What's in here

```
.
├── _config.yml        # site settings, theme, plugins
├── _posts/            # blog posts (Markdown)
├── about.md           # example page
├── index.html         # homepage (post listing)
├── Gemfile             # for local preview
└── .gitignore
```

## 1. Publish it on GitHub Pages (no local setup required)

1. Create a new **public** repository on GitHub.
   - For a **user/organization site**, name it `yourusername.github.io`
     and leave `baseurl: ""` in `_config.yml`.
   - For a **project site** (any other repo name), set
     `baseurl: "/your-repo-name"` in `_config.yml`.
2. Push these files to the repo's default branch (usually `main`):
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Pixyll site"
   git branch -M main
   git remote add origin https://github.com/yourusername/your-repo-name.git
   git push -u origin main
   ```
3. On GitHub, go to **Settings → Pages**, and under "Build and deployment"
   set **Source** to "Deploy from a branch", branch `main`, folder `/ (root)`.
4. Wait a minute or two, then visit the URL GitHub shows you
   (`https://yourusername.github.io` or `https://yourusername.github.io/your-repo-name`).

GitHub Pages builds Jekyll sites automatically — no build step to configure.
`remote_theme` in `_config.yml` is what pulls in Pixyll; it's a GitHub-Pages
approved plugin, so it works out of the box with no extra setup.

## 2. Preview it locally (optional)

Requires Ruby installed.

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Customize

- **Title, description, author, social links** — edit the top of `_config.yml`.
- **New post** — add a file to `_posts/` named `YYYY-MM-DD-title.md` with
  the same front matter (`layout: post`, `title`, `subtitle`, `tags`) as the
  example post.
- **New page** — add a `.md` file at the root (like `about.md`) with
  `layout: page` and a `permalink`.
- **Colors/fonts/CSS** — Pixyll's source (loaded via `remote_theme`) lives at
  https://github.com/johnotander/pixyll. To override styles, add your own
  CSS file and include it, or fork Pixyll and point `remote_theme` at your fork.
