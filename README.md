# Markdown Architectural Decision Records

> "Markdown Architectural Decision Records" (MADR) `[ˈmæɾɚ]` – decisions that [matter `[ˈmæɾɚ]`](https://en.wiktionary.org/wiki/matter#Pronunciation).

For user documentation, please head to <https://adr.github.io/madr/>.

## Quick start

* [`adr-template.md`](template/adr-template.md) has all sections, with explanations about them.
* [`adr-template-minmal.md`](template/adr-template-minimal.md) only contains mandatory sections, with explanations about them. <!-- ### Consequences also contained, though marked as "optional" -->
* [`adr-template-bare.md`](template/adr-template-bare.md) has all sections, which are empty (no explanations).
* [`adr-template-bare-minimal.md`](template/adr-template-bare-minimal.md) has the mandatory sections, without explanations. <!-- ### Consequences also contained, though marked as "optional" -->

Copy it into `docs/decisions`.
For each ADR, copy the template to `nnnn-title.md` and adapt.
Longer explanation: Head to <https://adr.github.io/madr/#applying-madr-to-your-project>.

## Development hints

* MADR follows [Semantic Versioning 2.0.0](https://semver.org/) and documents changes in a `CHANGELOG.md` following [keep a changelog 1.0.0](http://keepachangelog.com/en/1.0.0/).
* Issues can be reported at <https://github.com/adr/madr/issues>.
* Suggestions can be contributed via pull requests. MADR offers pre-configured VS Code web environment at [Gitpod](https://gitpod.io/#https://github.com/adr/madr).
* MADR uses [markdownlint](https://github.com/DavidAnson/markdownlint) as Linter for Markdown files. Use [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) for checking for linting issues in VS Code.
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

| Branch       | Meaning                                                                                                                                      |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `gh-pages`   | Homepage showing the latest released version, rendered at <https://adr.github.io/madr>                                                       |
| `develop`    | Latest developments, including homepage updates which should be published on a release. `gh-pages` should always be merged into this branch. |
| `release/vY` | Branch for latest release Y.x version of MADR. Introduced to fix [#92](https://github.com/adr/madr/issues/92)                                |

The branch name conventions follow the [git flow model](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow).

See also [`CONTRIBUTING.md`](CONTRIBUTING.md).

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
docker run -p 4000:4000 --rm -v "C:\git-repositories\adr.github.io\madr\docs":/site bretfisher/jekyll-serve
```

In case you get errors regarding `Gemfile.lock`, just delete `Gemfile.lock` and rerun.

## Updating just-the-docs

* Adapt `docs/Gemfile` to use newer just-the-docs version. Thereby check <https://github.com/just-the-docs/just-the-docs-template/blob/main/Gemfile> for versions.
* Delete `docs/Gemfile.lock`. Start `bundle install`.
* Check <https://github.com/just-the-docs/just-the-docs/blob/main/CHANGELOG.md>.
* Check <https://just-the-docs.com/migration/>.

## Releasing a new version

1. Update the examples at `docs/index.md` and `docs/examples.md`.
2. Update the concrete decisions in `docs/decisions/*` with the new template.
3. Commit ("Update examples and decisions") and push. Possibly as pull request.
4. Adapt the version reference in `template/0000-use-markdown-architectural-decision-records.md`.
5. Update "template" files in `docs/decisions`:
   * Copy `template/0000-use-markdown-architectural-decision-records.md` to `docs/decisions/0000-use-markdown-architectural-decision-records.md`.
   * Adapt content of `docs/decisions/adr-template.md` based on `template/adr-template.md`.
     Thereby, ensure that the YAML front matter in `docs/decisions/adr-template.md` is kept.
6. Add link to `docs/index.md` at "Older versions" (for the homepage).
7. Copy `.markdownlint.yml` to `template/.markdownlint.yml` (and possibly to `docs/.markdownlint.yml`).
8. Update `CHANGELOG.md`.
9. Commit.
10. Update `package.json` and publish to [npmjs](https://www.npmjs.com/package/madr) using [release-it](https://www.npmjs.com/package/release-it) (do not create a release on GitHub). This also does a commit.
11. Create GitHub release using [github-release-from-changelog](https://www.npmjs.com/package/github-release-from-changelog).
12. Merge `develop` into `gh-pages`

## License

This work is dual-licensed under [MIT](https://opensource.org/licenses/MIT) and
[CC0](https://creativecommons.org/share-your-work/public-domain/cc0/).
You can choose between one of them if you use this work.

```yaml
SPDX-License-Identifier: MIT OR CC0-1.0
```
