# Continuously deploy `wiki/` folder to GitHub wiki

## Why would you want this?

In [@jcbhmr]'s [conventions for GitHub projects], he recommends using the
`wiki/` folder to store developer-focused documentation for things like:

1. How to get started with a local copy of the project
2. How to add features to the project
3. How the code is structured
4. What code organization patterns are used
5. Reasoning behind design decisions

```yml
on:
  push:
    branches: [main]
    paths: [wiki/**, .github/workflows/deploy-wiki.yml]
concurrency:
  group: wiki
  cancel-in-progress: true
jobs:
  wiki:
    runs-on: ubuntu-latest
    environment:
      name: github-wiki
      url: ${{ steps.deployment.outputs.page_url }}
    steps:
      - uses: actions/checkout@v3
      - uses: jcbhmr/deploy-wiki@main
        id: deployment
```

[@jcbhmr]: https://github.com/jcbhmr
[conventions for github projects]:
  https://dev.to/jcbhmr/my-conventions-for-github-projects-2ibk
