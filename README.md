# test-docs-portal

## Overview
This repository contains an MkDocs site (Material theme) that supports **selectable legacy versions**.

Instead of bundling multiple versions into a single build, this repo follows a more scalable approach:

- **Version = Git tag** (e.g. `v1.1`, `v1.2`, `v1.3`)
- **Publishing = mike** (deploy each tag to `gh-pages/<tag>/`)
- **Version selector = Material built-in** (no custom JS/CSS needed)

## Local development
Install dependencies:

```bash
pip install mkdocs-material mike
```

Serve the current working tree:

```bash
mkdocs serve
```

Serve multiple versions locally (requires tags):

```bash
mike serve
```

## Publishing (GitHub Pages)
1. Configure GitHub Pages to publish from:
   - Branch: `gh-pages`
   - Folder: `/` (root)
2. Push a tag (for example `v1.3`). A GitHub Actions workflow will deploy that version using `mike`.

### Manual publish (if you want to run it locally)

```bash
mike deploy --push --update-aliases v1.3 latest
mike set-default --push latest
```

## Notes
- `legacy_docs/` is a helper directory with sample legacy pages. It is **not** included in the build.
  In a real project, the legacy content should live in the Git tag history.
