<img src="images/cmumc-avatar.jpg" alt="A Minecraft grass block in Carnegie Mellon tartan." width="96" align="right">

# Minecraft Multiplayer Server

The site for Carnegie Mellon's Minecraft server, at https://cmumc.github.io/cmumc-web/.
It started as [minecraft.alumni.cmu.edu](https://web.archive.org/web/20210214034920/https://minecraft.alumni.cmu.edu/),
kept as release [1.0.0](https://github.com/CMUMC/cmumc-web/releases/tag/1.0.0),
and is now built with the
[Carnegie Mellon Web Jekyll Theme](https://cmu-web.github.io/cmu-web-jekyll/)
on CMU's web template and the
[Carnegie Mellon Web Kit](https://cmu-web.github.io/cmu-web-kit/). The server
itself lives in [mc-server](https://github.com/CMUMC/mc-server).

## Pages

| Page                | What's on It                                                  |
| ------------------- | ------------------------------------------------------------- |
| `index.html`        | Welcome, the beginners' webinar and Homecoming events         |
| `get-started.html`  | Connecting to `mc.andrew.cmu.edu` in 10 steps                 |
| `ways-to-play.html` | Coming soon: the worlds and the Build Competition rules       |
| `gallery.html`      | Coming soon: Build Competition entries and the Virtual Campus |
| `about-us.html`     | Coming soon: who built the server                             |

Each page is HTML with the theme's `sections` layout; the header, navigation
and footer come from `_config.yml`. Write new docs pages in Markdown, and the
theme's default layout puts them in one column. The site has no CSS of its
own: if a page needs something the template and the kit don't have, propose it
for the kit or the theme first.

## Work on It

Use the Ruby version in `.ruby-version` and the Node version in
`.node-version`, then once per checkout:

```bash
bundle install
npm ci
npx prek install
```

Preview at http://localhost:4000 with `npm run serve`, which rebuilds as you
save. Check every changed page at 1300px and 390px wide.

`npm run build` builds the site into `_site/`, and then `npm run check` runs
Prettier's check and html-validate on it. The pre-commit hooks run Prettier.
CI builds and runs all of it, plus a link check, weekly as well as on every
push. Pushing to `main` publishes to GitHub Pages.
