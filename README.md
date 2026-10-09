# The New Climate Divide — project website

Source of [climatedivide.eu](https://climatedivide.eu/), the website of the DFG Emmy Noether project
*The New Climate Divide* (Die neue klimapolitische Spaltung) at Heidelberg University.

Built with [Hugo](https://gohugo.io/) (extended, v0.135.0) and the
[Hugo Blox](https://github.com/HugoBlox/hugo-blox-builder) research-group theme.
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
| `_vendor/` | Pinned copy of the theme modules listed in `go.mod` (refresh with `hugo mod vendor`) |

## Preview locally

```sh
hugo server
```

## Privacy

Google Analytics only loads after a visitor consents in the cookie banner
(`layouts/partials/hooks/body-end/cookieconsent.html`). All scripts, styles and fonts are served
from this site. If you add anything that loads from another domain (embeds, badges, maps, CDN
scripts), put it behind consent and update the privacy policy in `content/*/privacy/`.
