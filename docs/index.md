# Test Docs Portal

v1.2
This site is built with MkDocs (Material theme) and supports **selectable legacy versions**.

## How versioning works
- Each released documentation snapshot is stored as a **Git tag** (for example: `v1.1`, `v1.2`, `v1.3`).
- The site is published with **mike**, which deploys each tag into a dedicated path on the `gh-pages` branch.
- The Material theme reads the version list from mike and renders a version selector automatically.

> Tip: Use `mike serve` locally to preview multiple versions (requires tags).


