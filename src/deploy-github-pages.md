# Continuously deploy to GitHub Pages

Static site generators are software tools that allow users to create websites by
writing content in a markup language like HTML, Markdown, or AsciiDoc, and then
using templates to define the layout and design of the site. The resulting HTML
files can be served by any web server without the need for dynamic content
generation, making static sites faster and more secure than dynamic sites. There
are many different static site generator software tools available, each with
their own unique features and capabilities.

One popular static site generator is Jekyll, which is written in Ruby and uses
the Liquid template engine. Jekyll is often used for blogs, documentation sites,
and personal portfolios, and it integrates seamlessly with GitHub Pages for easy
deployment. Another popular static site generator is Hugo, which is written in
Go and uses the Go template language. Hugo is known for its fast build times and
is often used for larger websites and documentation projects.

Other static site generators include Gatsby, which is built on React and uses
GraphQL to pull data from a variety of sources, and Eleventy, which is written
in JavaScript and has a flexible data model that allows users to work with
content in a variety of formats. Each of these static site generators has its
own unique set of features and capabilities, making them suitable for different
types of projects and use cases.

## Node.js static site generator GitHub Pages deployment workflow

Make sure you have your `"prepack": "<your build command>"` script set in
`package.json`! You can also replace the `npm pack --dry-run` generic build
command with your own framework-specific tool.

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

🐳 This workflow also uses [devcontainers] to configure the build environment.

[devcontainers]: https://code.visualstudio.com/docs/devcontainers/tutorial
