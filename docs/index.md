# Test Docs Portal

This site is built with MkDocs (Material theme) and supports **selectable legacy versions**.

## repositories
- Frontend
- Backend
- Infra(Todo)

## How versioning works
- Each released documentation snapshot is stored as a **Git tag** (for example: `v1.1`, `v1.2`, `v1.3`).
- The site is published with **mike**, which deploys each tag into a dedicated path on the `docs-dist` branch.
- The Material theme reads the version list from mike and renders a version selector automatically.

> Tip: Use `mike serve` locally to preview multiple versions (requires tags).


