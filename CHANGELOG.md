# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## [unreleased]

### Added

- Add installation instructions using `npm`.

### Changed
- Placeholders changed from `*[PLACEHOLDER]*` to `[PLACEHOLDER]` to have a single pair of enclosing characters (`[]`) instead of two (`*[]*`).
- Rename `argument 1 pro` to `pro point` and `argument 1 con` to `con point`

## [1.1.1] – 2017-12-05

### Changed

- Simplify `package.json` and fix name.

## [1.1.0] – 2017-12-04

### Changed

- No change in the template itself.
- Use [adr-log](https://adr.github.io/adr-log/) to generate links to the ADRs in `docs/adr/index.md`.
- `template.md` is not part of the log, but a separate text block in `docs/adr/index.md`.
- Link to new homepage of MADR: <https://adr.github.io/madr/>.
- Refined justification of [ADR-0000](docs/adr/0000-use-markdown-architectural-decision-records.md).
- Refined `README.md`.

### Fixed

- Fixed internal links in `docs/adr/index.md`.
- Fixed typo in `docs/adr/0000-use-markdown-architectural-decision-records.md`.

## [1.0.0] – 2017-09-09

First release of Markdown Architectural Decision Records.

[unreleased]: https://github.com/adr/madr/compare/1.1.1...master
[1.1.1]: https://github.com/adr/madr/compare/1.1.0...1.1.1
[1.1.0]: https://github.com/adr/madr/compare/1.0.0...1.1.0
[1.0.0]: https://github.com/adr/madr/releases/tag/1.0.0
