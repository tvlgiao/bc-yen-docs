# bc-yen-docs

Documentation site for the **Yen** BigCommerce theme by [PapaThemes](https://papathemes.com).

Production URL: <https://bc-yen-docs.papathemes.com>

This is the URL `meta.documentation_url` points at in the theme's `config.json`, and the
one BigCommerce opens during Theme Marketplace review.

## Local development

Install MkDocs Material once:

```bash
pip install mkdocs-material
```

Run the local dev server:

```bash
mkdocs serve
```

Open <http://127.0.0.1:8000>.

## Build the static site

```bash
mkdocs build --strict
```

Output is written to `site/`. `--strict` turns a broken internal link into a failed build,
which is worth having: every page here links to at least one other.

## Deploy

```bash
mkdocs gh-deploy --clean --force
```

That builds the site and pushes it to the `gh-pages` branch, which GitHub Pages serves.
`docs/CNAME` carries the custom domain and is copied into the build, so the domain survives
each deploy.

## Where the content comes from

Most pages are written here and this repository is their only home.

`docs/settings-reference.md` is the exception: it is **generated** from `schema.json` in
the [bc-yen-theme](https://github.com/tvlgiao/bc-yen-theme) repository by
`scripts/docs/build-settings-reference.js`, and a test there fails when the committed copy
drifts from the schema. When a theme setting is added, regenerate it in that repository and
copy the result here — editing it by hand puts the two out of step, and the theme repo is
the one that gets checked.
