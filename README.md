<div align="center">

**🚧 Under construction! 👷‍♂️**

</div>

# Workflows for GitHub Actions

📋 Curated collection of useful GitHub workflows files

<div align="center">

![](https://placekitten.com/600/400)

<!--prettier-ignore-->
**[Overview](https://github.com/akshnz/workflows#readme)**
| [User docs](https://akshnz.github.io/workflows/)
| [Contribute](https://github.com/akshnz/workflows/blob/main/CONTRIBUTING.md)

</div>

<!-- TODO: Add emoji bulleted list of features -->

[🤝 We welcome contributions!] Even if you just have an idea, we want to hear
from you!

## Usage

![GitHub Actions](https://img.shields.io/static/v1?style=for-the-badge&message=GitHub+Actions&color=2088FF&logo=GitHub+Actions&logoColor=FFFFFF&label=)

<!-- TODO: Add usage blurb -->

## Development

This project uses [mdBook] to turn Markdown pages into a fancy website.

⚠️ GitHub Codespaces doesn't work with the IPv6 `[::1]` address that
`mdbook serve` uses by default. You'll need to add a `-n 0.0.0.0` IPv4 hostname
flag to get it to work with the HTTP Preview.

```sh
mdbook serve -n 0.0.0.0
```

🎨 To lint the project, we use [Prettier].

```sh
prettier -w . --ignore-file=.gitignore
```

[🤝 we welcome contributions!]: CONTRIBUTING.md
[mdbook]: https://rust-lang.github.io/mdBook/
[prettier]: https://prettier.io/
