# guides — Palikkaoppaat

Content for the association's guides site (<https://oppaat.palikkaharrastajat.fi>).

This is a **content-only repository**: Markdown pages + `config.toml` + images.
It has no build tooling of its own. The site is built and deployed by the
[`master-builder`](https://github.com/Suomen-Palikkaharrastajat-ry/master-builder)
pipeline at CI — see `.github/workflows/deploy.yml`, which calls
master-builder's reusable `deploy-content.yml` workflow.

## Editing

- Each `*.md` file is a page; frontmatter fields: `title`, `description`,
  `published`, `nav`, `navTitle`, `order`. See master-builder's docs for the
  full content contract.
- Content can be nested in subdirectories (e.g. `jasenpalvelut/`).
- `config.toml` holds site-wide settings (URL, colors, navigation).

Push to `main` to publish. Use the workflow's `builder_ref` input to test against
a specific master-builder branch.
