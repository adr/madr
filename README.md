# Markdown Any Decision Records

> "Markdown Any Decision Records" (MADR) `[ˈmæɾɚ]` – decisions that [matter `[ˈmæɾɚ]`](https://en.wiktionary.org/wiki/matter#Pronunciation).

For user documentation, please head to <https://adr.github.io/madr/>.

## Development Hints

* MADR follows [Semantic Versioning 2.0.0](https://semver.org/) and documents changes in a `CHANGELOG.md` following [keep a changelog 1.0.0](http://keepachangelog.com/en/1.0.0/).
* Issues can be reported at <https://github.com/adr/madr/issues>.
* Suggestions can be contributed via pull requests. MADR offers pre-configured VS Code web environment at [Gitpod](https://gitpod.io/#https://github.com/adr/madr).
* Use [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
* `template/adr-template.md` is mirrored to `docs/decisions/adr-template`.
  However, following YAML front matter is added to make it handled properly by the [Just the Docs Jekyll Template](https://just-the-docs.github.io/just-the-docs/). <!-- markdownlint-disable-next-line MD031 -->
  ```markdown
  ---
  parent: Decisions
  nav_order: 100
  title: ADR Template
  ---
  ```

## How to start Jekyll locally

For rendering the `docs` directory, Jekyll is needed.

For local development, follow the [Jekyll installation instructions](https://jekyllrb.com/docs/installation/).
Installing the latest version of ruby followed by `gem install bundler` should be enough.

Afterwards, run

```terminal
bundle install
jekyll serve --livereload
```

and go to <http://localhost:4000/madr/> in your browser.

On Windows, using a dockerized environment is recommended:

```terminal
docker run -p 4000:4000 --rm --volume="C:\git-repositories\adr.github.io\madr\docs":/srv/jekyll jekyll/jekyll:4 jekyll serve
```

In case you get errors regarding `Gemfile.lock`, just delete `Gemfile.lock` and rerun.

## Releasing a new version

1. Update `CHANGELOG.md`.
2. Update the examples at `docs/index.md` and `docs/examples.md`.
3. Update `docs/decisions/*` with the new template.
4. Check that the YAML front matter in `docs/decisions/adr-template.md` is kept.
5. Copy `.markdownlint.yml` to `template/.markdownlint.yml`
6. Adapt the version reference in `template/0000-use-markdown-any-decision-records.md`.
7. Copy `template/0000-use-markdown-any-decision-records.md` to `docs/decisions/0000-use-markdown-any-decision-records.md`.
8. Update `package.json`, publish to [npmjs](https://www.npmjs.com/package/madr), create GitHub release.\
   Use [release-it](https://www.npmjs.com/package/release-it) (do not create a release on GitHub) and [github-release-from-changelog](https://www.npmjs.com/package/github-release-from-changelog).

## License

This work is dual-licensed under [MIT](https://opensource.org/licenses/MIT) and
[CC0](https://creativecommons.org/share-your-work/public-domain/cc0/).
You can choose between one of them if you use this work.

```yaml
SPDX-License-Identifier: MIT OR CC0-1.0
```
