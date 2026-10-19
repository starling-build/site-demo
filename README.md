# Starling Site demo

A site whose pages are Starling Writer documents in this repository,
built static into `docs/` and served by GitHub Pages at
https://starling-build.github.io/site-demo/. There is no server.

- `site.json` names the site and orders its pages.
- `pages/<slug>.json` is each page as the document model.
- `docs/` is the build: the wasm Writer, the pages, a manifest, a search
  index, and one shell page per route with the page's title in meta tags.

Edit it by cloning and opening the folder in Starling Office
(`OfficeApp --site <clone>`): Edit is the whole Writer, Publish builds,
commits and pushes. Or `OfficeApp --site-publish <clone> -m "…"`.
See docs/plans/site.md in starling-build/starling.
