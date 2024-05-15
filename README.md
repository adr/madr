# Markdown Architectural Decision Records

> "Markdown Architectural Decision Records" (MADR) `[ˈmæɾɚ]` – decisions that [matter `[ˈmæɾɚ]`](https://en.wiktionary.org/wiki/matter#Pronunciation).

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

### Branches

| Branch | Meaning |
| -- | -- |
| `gh-pages` | Homepage showing the latest released version, rendered at <https://adr.github.io/madr> |
| `develop` | Latest developments, including homepage updates which should be published on a release. `gh-pages` should always be merged into this branch. |
| `release/v1` | Branch for latest release 1.x version of MADR. Introduced to fix [#92](https://github.com/adr/madr/issues/92) |
| `release/vY` | Branch for version Y.x of MADR. |

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

1. Update the examples at `docs/index.md` and `docs/examples.md`.
2. Update `docs/decisions/*` with the new template.
3. Add link to `docs/index.md` (for the homepage).
4. Commit and push.
5. Update `CHANGELOG.md`.
6. Check that the YAML front matter in `docs/decisions/adr-template.md` is kept.
7. Copy `.markdownlint.yml` to `template/.markdownlint.yml`
8. Adapt the version reference in `template/0000-use-madr.md`.
9. Copy `template/0000-use-madr.md` to `docs/decisions/0000-use-madr.md`.
10. Update `package.json`
11. Publish to [npmjs](https://www.npmjs.com/package/madr) using [release-it](https://www.npmjs.com/package/release-it) (do not create a release on GitHub). This also does a commit.
12. Create GitHub release using [github-release-from-changelog](https://www.npmjs.com/package/github-release-from-changelog).
13. Merge `develop` into `gh-pages`

## License

This work is dual-licensed under [MIT](https://opensource.org/licenses/MIT) and
[CC0](https://creativecommons.org/share-your-work/public-domain/cc0/).
You can choose between one of them if you use this work.

```yaml
SPDX-License-Identifier: MIT OR CC0-1.0
```
