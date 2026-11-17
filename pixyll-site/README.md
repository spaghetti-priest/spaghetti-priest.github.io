# My Notebook (Pixyll + GitHub Pages)

Built on the [Pixyll](https://github.com/johno/pixyll) theme by John Otander (MIT).

## Publish
1. Create a repo named `USERNAME.github.io` (or any name for a project site).
2. Edit `_config.yml`: `title`, `author`, `email`, `url`, `github_username`.
   For a project site, also set `baseurl: "/repo-name"`.
3. Replace `images/me.jpeg` with your own photo (or remove it).
4. Push to `main`, then Settings -> Pages -> Deploy from a branch -> `main` / root.

## Run locally (optional)
    bundle install
    bundle exec jekyll serve

## New post
Add `_posts/YYYY-MM-DD-my-title.md` with `layout: post` and a `title:`.
