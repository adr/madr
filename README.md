# Markdown Architectural Decision Records [![part of ADR](https://img.shields.io/badge/part_of-ADR-blue.svg)](https://adr.github.io)

> "Markdown Architectural Decision Records" (MADR) `[ˈmæɾɚ]` – architectural decisions that [matter `[ˈmæɾɚ]`](https://en.wiktionary.org/wiki/matter#Pronunciation).

For user documentation, please head to <https://adr.github.io/madr/>.

## Development Hints

* MADR follows [Semantic Versioning 2.0.0](https://semver.org/) and documents changes in a `CHANGELOG.md` following [keep a changelog 1.0.0](http://keepachangelog.com/en/1.0.0/).
* Issues can be reported at <https://github.com/adr/madr/issues>.
* Use the [Markdown Style Guide](http://www.cirosantilli.com/markdown-style-guide/) space-sentence:1, wrap:sentence, header:atx, list-marker:asterisk, list-space:1, code:fenced

**Releasing a new version:**

1. Update `CHANGELOG.md`.
1. Update `README.md` with the new template and the example.
1. Adapt the version reference in `template/0000-use-markdown-architectural-decision-records.md`.
1. Copy `template/0000-use-markdown-architectural-decision-records.md` to `docs/decisions/0000-use-markdown-architectural-decision-records.md`.
1. Update `package.json`, publish to [npmjs](https://www.npmjs.com/package/madr), create GitHub release.  
   Use [release-it](https://www.npmjs.com/package/release-it) (do not create a release on GitHub) and [github-release-from-changelog](https://www.npmjs.com/package/github-release-from-changelog).

## License

License: [CC0](https://creativecommons.org/share-your-work/public-domain/cc0)
