# GitHub workflows

📋 Curated collection of useful GitHub workflows files

<div align="center">

![](https://i.imgur.com/lToQ3b4.png)

<!--prettier-ignore-->
**[Overview](https://github.com/jcbhmr/github-workflows#readme)**
| [Contribute](https://github.com/jcbhmr/github-workflows/blob/main/CONTRIBUTING.md)
| [Wiki](https://github.com/jcbhmr/github-workflows/wiki)

</div>

👷‍♂️ Premade for 80% of usecases \
©️ No license header or attribution needed \
✏️ Ready for customization

🤝 [We welcome contributions]! Even if you just have an idea, we want to hear from you!

## Usage

![GitHub Actions](https://img.shields.io/static/v1?style=for-the-badge&message=GitHub+Actions&color=2088FF&logo=GitHub+Actions&logoColor=FFFFFF&label=)

1. Select a `src/$NAME.yml` workflow file from this repo
2. Copy the entire contents of the file
3. Create a new `.github/workflows/$NAME.yml` file in your own repo
4. Paste the contents into your new file
5. Commit & push it to GitHub
6. Profit! 🎉

### List of workflows

- **[`deploy.yml`]:** Deploys a Bikeshed specification to GitHub Pages
- **[`docs.yml`]:** Deploys the `docs/` npm workspace project to GitHub Pages
- **[`publish.yml`]:** Publishes an npm package to [npmjs.com]
- **[`test.yml`]:** Runs tests for an npm package
- **[`wiki.yml`]:** Publishes the `wiki/` subfolder to the GitHub wiki

[`deploy.yml`]: src/deploy.yml
[`docs.yml`]: src/docs.yml
[`publish.yml`]: src/publish.yml
[`test.yml`]: src/test.yml
[`todo.yml`]: src/todo.yml
[`wiki.yml`]: src/wiki.yml
[we welcome contributions]: CONTRIBUTING.md
[npmjs.com]: https://www.npmjs.com/
