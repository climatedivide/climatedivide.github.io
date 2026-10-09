# Theme (local copy)

This folder holds the theme the site is built with: the last release of the
**Hugo Blox Bootstrap** framework (formerly Wowchemy), made of three parts:

| Folder | What it does |
| --- | --- |
| `blox-bootstrap/` | Layouts, styles, scripts, translations (the theme proper) |
| `blox-core/` | Small helper partials used by the theme |
| `blox-seo/` | Meta tags, structured data, Google Analytics partial |

## Origin

Copied from <https://github.com/HugoBlox/hugo-blox-bootstrap> at commit `8069eb7`
(January 2026), which contains the final code of the Hugo Blox monorepo modules
(`modules/blox-bootstrap/v5`, `blox-core`, `blox-seo`, August 2025). HugoBlox has
archived this Bootstrap framework and no longer maintains it; its successor is the
Tailwind-based HugoBlox Kit, which would mean rebuilding the site. Keeping a local
copy means the site no longer depends on Go or Hugo Modules, and we can patch it.

Licence: MIT, see `LICENSE.md` in this folder.

## Local patches (to keep it working on current Hugo)

Applied for Hugo 0.167:

- Imports between the three parts point to these folders (`blox-core`, `blox-seo`)
  instead of the Go module paths.
- Deprecated template APIs replaced: `site.Data` → `hugo.Data`,
  `site.LanguageCode` → `site.Language.Locale`, `.IsNode` → `not .IsPage`,
  `resources.ToCSS`/`toCSS` → `css.Sass`.
- Removed `blox-seo/layouts/_markup/sitemap.xml`, which Hugo never used
  (Hugo's built-in sitemap is used, as before).

Site-specific changes do **not** go here: they live in the project's `layouts/`,
`data/` and `assets/` folders, which override files in this theme.

## Checking a new Hugo version

Build with `hugo --logLevel info` and look for `deprecated` or `WARN` lines; fix
them in the files above (or in the project's `layouts/`) before they become errors.
