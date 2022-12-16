# Continuously deploy to GitHub Pages

<!-- TODO: Add documentation about how this Action works and what it does -->

Here's the complete workflow:

`.github/workflows/deploy.yml`

```yml
on:
  push:
    branches: [main]
    paths: [docs/**, .github/workflows/deploy.yml]
jobs:
  pages:
    runs-on: ubuntu-latest
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    concurrency:
      group: pages
      cancel-in-progress: true
    permissions: write-all
    steps:
      - uses: actions/checkout@v3
      - uses: devcontainers/ci@v0.2
        with:
          runCmd: npm ci && npm pack --dry-run
      - uses: actions/configure-pages@v2
      - uses: actions/upload-pages-artifact@v1
        with:
          path: dist
      - uses: actions/deploy-pages@v1
        id: deployment
```
