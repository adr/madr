# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/)
and this project adheres to [Semantic Versioning](https://semver.org/).

## [unreleased]

### Changed

- Changed wording in "Confirmation" section. [#162](https://github.com/adr/madr/pull/162)

## [4.0.0] – 2024-09-17

### Fixed

- `adr-template.md`: Re-add quotes around chosen option name.
- `adr-template-minimal.md`: Place holder in one line.
- `adr-template-bare.md`: Keep fixed template text as normal markdown (and not as comment).
- `adr-template-bare.md` and `adr-template-bare-minimal.md`: Always use `<!-- … ->` als place holder instead of `{…}`.

## [4.0.0-beta] – 2024-09-02

### Added

- Bare an minimal templates: [#88](https://github.com/adr/madr/issues/88)
  - [`adr-template-minmal.md`](template/adr-template-minimal.md) only contains mandatory sections, with explanations about them. <!-- ### Consequences also contained, though marked as "optional" -->
  - [`adr-template-bare.md`](template/adr-template-bare.md) has all sections, wich are empty (no explanations).
  - [`adr-template-bare-minimal.md`](template/adr-template-bare-minimal.md) has the mandatory sections, without explanations. <!-- ### Consequences also contained, though marked as "optional" -->
- Added example for "Confirmation". [#135](https://github.com/adr/madr/issues/135)

### Changed

- Put the content of `status:` in quotes to tell YAML it's a string. [#91](https://github.com/adr/madr/issues/91)
- Renamed "Validation" to "Confirmation" and put it as sub element of "Decision Outcome". [#87](https://github.com/adr/madr/pull/87)
- Renamed "Deciders" to "Decision Maker(s)" (`decision-makers:`). [#101](https://github.com/adr/madr/issues/101)
- Rename template name "Markdown Any Decision Record" back to "Markdown Architectural Decision Record"
- Rename `0000-use-markdown-any-decision-records.md` to `0000-use-madr.md`.
- All placehodlers are are now one liners.

### Removed

- Removed link to ADR in `status` field. Only identifier should be put. [#150](https://github.com/adr/madr/pull/150)

## [3.0.0] – 2022-10-09

### Added

- Added comments to [markdownlint rules](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md#rules) in `.markdownlint.yml` files.

### Changed

- Moved section "Validation" directly after "Decision Outcome"
- Merged sections "Positive Consequences" and "Negative Consequences" into "Consequences" to enable similar grammar as in "Pros and Cons of the Options". [#75](https://github.com/adr/madr/issues/75)

### Removed

- Removed allowed punctuation in `.markdownlint.yml` rule

## [3.0.0-beta.2] – 2022-05-25

### Added

- Added front matter fields "consulted" and "informed" (inspired by [RACI](https://en.wikipedia.org/wiki/Responsibility_assignment_matrix#Role_distinction)). [#62](https://github.com/adr/madr/issues/62)
- Added section "Validation"

### Changed

- Moved markings for optional content from next to the heading above the heading

## [3.0.0-beta] – 2022-05-17

### Added

- Added YAML front matter to `docs/decisions/adr-template.md`
- Added "Neutral" arguments (in addition to "Good, because", and "Bad, because")
- Refined howto texts
- Disable [markdown-lint](https://github.com/DavidAnson/markdownlint)'s [MD013 - line length](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md013---line-length) for the ADR files.
- Added initial [markdownlint](https://github.com/DavidAnson/markdownlint) configuration file `.markdownlint`.
  This can, for instance, be used by a [GitHub linting workflow](https://github.com/adr/madr/blob/develop/.github/workflows/lint.yaml)

### Changed

- Rename "Markdown Architectural Decision Record" to "Markdown Any Decision Record"
- Place holders for values are denoted by curly braces (`{placehodler}`). Before it was `[placeholder]`. [#35](https://github.com/adr/madr/issues/35)
- Directory of ADRs changed from `docs/adr` to `docs/decisions`. [#33](https://github.com/adr/madr/issues/33)
- Renamed `template.md` to `adr-template.md`. [#36](https://github.com/adr/madr/issues/36)
- Changed `## Links` to `## More information`
- Relaxed content of `More information` section from a bullet list to free text.
- Changed `optional` to `This is an optional element. Feel free to remove.` to make it more clear how to work with an optional element.
- Changed `driver 1` to `decicion driver 1`.
- Changed `e.g., compromising quality attribute, follow-up decisions required, …` to `e.g., compromising one or more desired qualities, …`
- Moved the fields to the YAML front matter
- Renamed `template/index.md` to `template/README.md`, because i) `README.md` is directly rendered on GitHub and ii) for Jekyll-based rendering, the index file has to be adapted (e.g., to show a hint to the doc as MADR does in `docs/decisions/index.md`).
- Replace `{option 1}` place holder to `{title of option 1}`.
- Restructured and streamlined documentation.

### Removed

- Removed `Technical Story: {description | ticket/issue URL} <!-- optional -->`, because all description should go into "Context and Problem Statement"
- Removed files `.adr-dir` and `.adr-type` as tooling should automatically detect the style of the template

## [2.1.2] – 2019-02-17

### Added

- Add more status fields. Source: [#20](https://github.com/adr/madr/pull/20).

### Fixed

- Fixed typos in `README.md`.

## [2.1.1] – 2019-01-21

### Fixed

- Fix typo in heading. Fixes [#18](https://github.com/adr/madr/issues/18)

## [2.1.0] – 2018-06-14

### Changed

- Headings "Positive/negative consequences" now full h3 headings instead of text headings
- Adapted internal ADRs to new format

### Added

- Added ADR-0011 stating that we use an asterisk as list marker

## [2.0.3] – 2018-03-21

### Fixed

- Fix reference to MADR version in ADR-0000 and README.md

## [2.0.2] – 2018-03-16

### Changed

- Streamlined template's ADR-0000.
- Streamlined template by using ellipsis and removing double empty lines.

## [2.0.1] – 2018-03-07

### Fixed

- State MADR 2.0.1 also in template's ADR-0000.

## [2.0.0] – 2018-03-07

### Added

- Optional: Status, Deciders, Date. Fixes [#2](https://github.com/adr/madr/issues/2).
- More explanations of options can now be put next to each option
- Links to other ADRs added at the bottom of the ADR

### Changed

- Rename "User Story" to "Technical Story"
- "Context and Problem Statement" and "Decision Drivers" are a heading now
- The chosen option is now written in quotes to separate the name from the rest of the text
- All bullet lists are now made using `*` (instead of `-` at some lists)

## [1.4.0] – 2018-03-01

### Added

- Version of MADR into `ADR-0000` of the template. Fixes [#5](https://github.com/adr/madr/issues/5)
- `README.md`: Added wints on the filenames.
- More ADRs on MADR
- Added `LICENSE` file

### Changed

- `README.md`: Removed section "Background Information" as the information is contained at <https://adr.github.io>, too. Fixes [#4](https://github.com/adr/madr/issues/4)

## [1.3.1] – 2018-02-13

### Fixed

- Replace "alternative" by "option" in all `md` files
- Update to new "Decision Outcome" format in all `md` files

## [1.3.0] – 2018-01-30

### Changed

- Changed template to be closer to the [Y-Statements](https://www.infoq.com/articles/sustainable-architectural-design-decisions).
  Especially rename "alternative" to "option".
- Restructured syntax of "Decision Outcome".
  Positive and negative consequences as separate bullet list.
- Rename "point" to "argument" (which reverts the change of version 1.2.0)
- Number "arguments" from a to c. Re-use "variables" a to c to guide the author that the same topic should be handled by the enumeration. e..g, performance, ...
- Exchange `+` and `-` by "Good, because ..." and "Bad, because ..."
- Remove emphasize of "User Story:"

## [1.2.0] – 2018-01-26

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
- Use [adr-log](https://github.com/adr/adr-log?tab=readme-ov-file#adr-log-) to generate links to the ADRs in `docs/adr/index.md`.
- `template.md` is not part of the log, but a separate text block in `docs/adr/index.md`.
- Link to new homepage of MADR: <https://adr.github.io/madr/>.
- Refined justification of `ADR-0000`.
- Refined `README.md`.

### Fixed

- Fixed internal links in `docs/adr/index.md`.
- Fixed typo in `docs/adr/0000-use-markdown-architectural-decision-records.md`.

## [1.0.0] – 2017-09-09

First release of Markdown Architectural Decision Records.

[unreleased]: https://github.com/adr/madr/compare/4.0.0...develop
[4.0.0]: https://github.com/adr/madr/compare/4.0.0-beta...4.0.0
[4.0.0-beta]: https://github.com/adr/madr/compare/3.0.0...4.0.0-beta
[3.0.0]: https://github.com/adr/madr/compare/3.0.0-beta.2...3.0.0
[3.0.0-beta.2]: https://github.com/adr/madr/compare/3.0.0-beta...3.0.0-beta.2
[3.0.0-beta]: https://github.com/adr/madr/compare/2.1.2...3.0.0-beta
[2.1.2]: https://github.com/adr/madr/compare/2.1.1...2.1.2
[2.1.1]: https://github.com/adr/madr/compare/2.1.0...2.1.1
[2.1.0]: https://github.com/adr/madr/compare/2.0.3...2.1.0
[2.0.3]: https://github.com/adr/madr/compare/2.0.2...2.0.3
[2.0.2]: https://github.com/adr/madr/compare/2.0.1...2.0.2
[2.0.1]: https://github.com/adr/madr/compare/2.0.0...2.0.1
[2.0.0]: https://github.com/adr/madr/compare/1.4.0...2.0.0
[1.4.0]: https://github.com/adr/madr/compare/1.3.1...1.4.0
[1.3.1]: https://github.com/adr/madr/compare/1.3.0...1.3.1
[1.3.0]: https://github.com/adr/madr/compare/1.2.0...1.3.0
[1.2.0]: https://github.com/adr/madr/compare/1.1.1...1.2.0
[1.1.1]: https://github.com/adr/madr/compare/1.1.0...1.1.1
[1.1.0]: https://github.com/adr/madr/compare/1.0.0...1.1.0
[1.0.0]: https://github.com/adr/madr/releases/tag/1.0.0

<!-- markdownlint-disable-file MD013 MD024 -->
