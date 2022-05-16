# Markdown Any Decision Records [![part of ADR](https://img.shields.io/badge/part_of-ADR-blue.svg)](https://adr.github.io)

> "Markdown Any Decision Records" (MADR) `[ˈmæɾɚ]` – decisions that [matter `[ˈmæɾɚ]`](https://en.wiktionary.org/wiki/matter#Pronunciation).

For user documentation, please head to <https://adr.github.io/madr/>.

## Development Hints

* MADR follows [Semantic Versioning 2.0.0](https://semver.org/) and documents changes in a `CHANGELOG.md` following [keep a changelog 1.0.0](http://keepachangelog.com/en/1.0.0/).
* Issues can be reported at <https://github.com/adr/madr/issues>.
* Use the [Markdown Style Guide](http://www.cirosantilli.com/markdown-style-guide/) `space-sentence:1, wrap:sentence, header:atx, list-marker:asterisk, list-space:1, code:fenced`
* Use [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
* `template/adr-template.md` is mirrored to `docs/decisions/adr-template`.
  However, following YAML front matter is added to make it handled properly by the [Just the Docs Jekyll Template](https://just-the-docs.github.io/just-the-docs/).

  ```markdown
  ---
  parent: Decisions
  nav_order: 100
  title: ADR Template
  ---

## Releasing a new version

1. Update `CHANGELOG.md`.
2. Update the example at `docs/index.md`.
3. Update `docs/decisions/*` with the new template
4. Check that the YAML front madder in `docs/decisions/adr-template.md` is kept.
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
