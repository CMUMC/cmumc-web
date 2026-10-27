<img src="images/cmumc-avatar.jpg" alt="A Minecraft grass block in Carnegie Mellon tartan." width="96" align="right">

# Minecraft Multiplayer Server

The site for Carnegie Mellon's Minecraft server, at https://cmumc.github.io/.
It brings back [minecraft.alumni.cmu.edu as of February 14, 2021](https://web.archive.org/web/20210214034920/https://minecraft.alumni.cmu.edu/),
rebuilt on CMU's web template and the
[Carnegie Mellon Web Kit](https://cmu-web.github.io/). The server
itself lives in [mc-server](https://github.com/CMUMC/mc-server).

## Pages

| Page                | What's on It                                                  |
| ------------------- | ------------------------------------------------------------- |
| `index.html`        | Welcome, the beginners' webinar, and Homecoming events        |
| `get-started.html`  | Connecting to `mc.andrew.cmu.edu` in ten steps                |
| `ways-to-play.html` | Coming soon: the worlds and the Build Competition rules       |
| `gallery.html`      | Coming soon: Build Competition entries and the Virtual Campus |
| `about-us.html`     | Coming soon: who built the server                             |

Plain HTML, no build step, and no CSS of its own: everything comes from the
template and the kit. If a page needs something neither has, propose it for
the kit first.

## Work on It

Use the Node version in `.node-version`, then once per checkout:

```bash
npm ci
npx prek install
```

Preview at http://localhost:8000 with `npm run serve`. Check every changed
page at 1300px and 390px wide.

`npm run check` runs Prettier's check and html-validate, and the pre-commit
hooks run the same. CI also checks links, weekly as well as on every push.
Pushing to `main` publishes to GitHub Pages.
