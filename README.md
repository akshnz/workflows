# GitHub workflows

📋 Curated collection of useful GitHub workflows files

<div align="center">

![](https://i.imgur.com/lToQ3b4.png)

<!--prettier-ignore-->
**[Overview](https://github.com/jcbhmr/github-workflows#readme)**
| [Contribute](https://github.com/jcbhmr/github-workflows/blob/main/CONTRIBUTING.md)

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

- **[`nodejs/deploy-docs.yml`]:** Deploys the `docs/` npm workspace to GitHub Pages
- **[`nodejs/publish.yml`]:** Publishes an npm package to [npmjs.com]
- **[`nodejs/test.yml`]:** Runs tests for an npm package
- **[`spec/deploy.yml`]:** Deploys a Bikeshed specification to GitHub Pages
- **[`deploy-wiki.yml`]:** Publishes the `wiki/` subfolder to the GitHub wiki

[`nodejs/deploy-docs.yml`]: src/nodejs/deploy-docs.yml
[`nodejs/publish.yml`]: src/nodejs/publish.yml
[`nodejs/test.yml`]: src/nodejs/test.yml
[`spec/deploy.yml`]: src/spec/deploy.yml
[`deploy-wiki.yml`]: src/deploy-wiki.yml
[we welcome contributions]: CONTRIBUTING.md
[npmjs.com]: https://www.npmjs.com/
