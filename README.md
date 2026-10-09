# The New Climate Divide — project website

Source of [climatedivide.eu](https://climatedivide.eu/), the website of the DFG Emmy Noether project
*The New Climate Divide* (Die neue klimapolitische Spaltung) at Heidelberg University.

Built with [Hugo](https://gohugo.io/) (extended, v0.167.0) and a local copy of the
Hugo Blox Bootstrap research-group theme in `themes/` (see `themes/README.md`).
Every push to `main` is built and deployed to GitHub Pages by `.github/workflows/publish.yaml`.

## Layout

| Path | What it holds |
| --- | --- |
| `content/en/` | English pages (home, about, people, news, publications, legal pages) |
| `content/de/` | German translations — keep the same folder names and `translationKey` as the English page |
| `content/*/authors/` | Team profiles. `user_groups` decides where a person appears on the People page |
| `config/_default/` | Site settings, menus, languages |
| `layouts/` | Local overrides of theme templates (navbar, footer, people block, consent banner, …) |
| `data/assets.toml` | Points the theme's JS/CSS libraries to the self-hosted copies in `static/vendor/` |
| `themes/` | The theme (archived upstream, kept and patched here) |

## Preview locally

Install Hugo **extended**, version 0.158 or newer (the site is built with 0.167.0;
on macOS: `brew install hugo`). Go is not needed. Then run:

```sh
hugo server
```

and open <http://localhost:1313/>.

## Updating Hugo

Change `WC_HUGO_VERSION` in `.github/workflows/publish.yaml`, then build locally with
`hugo --logLevel info` and fix any `deprecated`/`WARN` lines (see `themes/README.md`).

## Privacy

Google Analytics only loads after a visitor consents in the cookie banner
(`layouts/partials/hooks/body-end/cookieconsent.html`). All scripts, styles and fonts are served
from this site. If you add anything that loads from another domain (embeds, badges, maps, CDN
scripts), put it behind consent and update the privacy policy in `content/*/privacy/`.
