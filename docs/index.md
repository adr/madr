---
nav_order: 1
---
# Markdown Architectural Decision Records [![part of ADR](https://img.shields.io/badge/part_of-ADR-blue.svg)](https://adr.github.io)

> "Markdown Architectural Decision Records" (MADR) `[ˈmæɾɚ]` – architectural decisions that [matter `[ˈmæɾɚ]`](https://en.wiktionary.org/wiki/matter#Pronunciation).

**Note that this documentation describes MADR 3.0.0-alpha (not yet released) and might not apply to earlier released versions**

- [News](#news)
- [Overview](#overview)
- [The Template](#the-template)
- [Example](#example)
- [Apply it to your project](#apply-it-to-your-project)
  - [Initialization](#initialization)
  - [Create a new ADR](#create-a-new-adr)
- [License](#license)

## News

- 2021-04-25: MADR examples featured in Medium stories ["From Architectural Decisions to Design Decisions"](https://medium.com/olzzio/from-architectural-decisions-to-design-decisions-f05f6d57032b) and ["ADR = Any Decision Record?"](https://medium.com/olzzio/adr-any-decision-record-916d1b64b28d) <!-- and blog post ["ADR = Any Decision Record? Architecture, Design and Beyond"](https://ozimmer.ch/practices/2021/04/23/AnyDecisionRecords.html) -->
- 2021-04-08: MADR recommended as an ADR format in "Design Practice Repository". This ebook is available on [Leanpub](https://leanpub.com/dpr). The decision capturing activity is also described [online](https://socadk.github.io/design-practice-repository/activities/DPR-ArchitecturalDecisionCapturing.html).
- 2020-09-29: MADR presented in the keynote "Markdown Architectural Decision Records: Capturing Decisions Where the Developer is Working" at the workshop "[Second Software Documentation Generation Challenge (DocGen2)](https://dysdoc.github.io/docgen2/index.html)". Slides available at [Speaker Deck](https://speakerdeck.com/koppor/markdown-architecturaldecisionrecords-capturing-decisions-where-the-developer-is-working).
- 2019-07-08: MADR referenced in [Architectural Decisions — The Making Of](https://ozimmer.ch/practices/2020/04/27/ArchitectureDecisionMaking.html), a post in the new blog "The Concerned Architect" by Olaf Zimmermann (shorter version available on [Medium](https://medium.com/@docsoc/y-statements-10eb07b5a177)).
- 2018-04-13: Mentioned in [@vanto](https://github.com/vanto)'s presentation about ADRs: <https://speakerdeck.com/vanto/a-brief-introduction-to-architectural-decision-records>.
- 2018-04-03: Scientific publication: [Markdown Architectural Decision Records: Format and Tool Support](http://ceur-ws.org/Vol-2072/paper9.pdf).

## Overview

An [Architectural Decision (AD)](https://en.wikipedia.org/wiki/Architectural_decision) is a software design choice that addresses a functional or non-functional requirement that is architecturally significant.
This might, for instance, be a technology choice (e.g., Java vs. JavaScript), a choice of the IDE (e.g., IntelliJ vs. Eclipse IDE), a choice between a library (e.g., [SLF4J](https://www.slf4j.org/) vs [java.util.logging](https://docs.oracle.com/javase/8/docs/api/java/util/logging/package-summary.html)), or a decision on features (e.g., infinite undo vs. limited undo).
Do not take the term "architecture" too seriously or interpret it too strongly.
As the examples illustrate, any decisions that might have an impact on the architecture somehow are architectural decisions.

It should be as easy as possible to
a) write down the decisions and
b) to version the decisions.

This repository offers a solution to record architectural decisions.
It provides files to document Architectural Decisions using **M**arkdown and **A**rchitectural **D**ecision **R**ecords.

Since MADR 3.0.0, the decisions are placed in the folder `docs/decisions` to

1) Enable [GitHub pages](https://pages.github.com/) to render it using the web.
   See <https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/> for more information.
2) Separate the architectural decisions from other documentation.

The filenames are following the pattern `NNNN-title-with-dashes.md` ([ADR-0005](docs/decisions/0005-use-dashes-in-filenames.md)), where

- `NNNN` is a consecutive number and we assume that there won't be more than 9,999 ADRs in one repository.
- the title is stored using dashes and lowercase, because [adr-tools] also does that.
- the suffix is `.md`, because it is a [Markdown](https://github.github.com/gfm/) file.

## Example

```markdown
# Use Markdown Architectural Decision Records

## Context and Problem Statement

We want to record architectural decisions made in this project.
Which format and structure should these records follow?

## Considered Options

* [MADR](https://adr.github.io/madr/) 2.1.2 - The Markdown Architectural Decision Records
* [Michael Nygard's template](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions) - The first incarnation of the term "ADR"
* [Sustainable Architectural Decisions](https://www.infoq.com/articles/sustainable-architectural-design-decisions) - The Y-Statements
* Other templates listed at <https://github.com/joelparkerhenderson/architecture_decision_record>
* Formless - No conventions for file format and structure

## Decision Outcome

Chosen option: "MADR 2.1.2", because

* Implicit assumptions should be made explicit.
  Design documentation is important to enable people understanding the decisions later on.
  See also [A rational design process: How and why to fake it](https://doi.org/10.1109/TSE.1986.6312940).
* The MADR format is lean and fits our development style.
* The MADR structure is comprehensible and facilitates usage & maintenance.
* The MADR project is vivid.
* Version 2.1.2 is the latest one available when starting to document ADRs.
```

The example is rendered at <decisions/0000-use-markdown-architectural-decision-records.md>.
The full template (with placeholders and some guidance how to use) can be found at <decisions/adr-template.md>.

For the MADR project itself, all ADRs exist at [docs/decisions/](https://github.com/adr/madr/tree/main/docs/decisions).

## Apply it to your project

### Initialization

Create folder `docs/decisions` in your project.
Copy all files in `template` from the MADR project to the folder `docs/decisions` in your project.

Using `npm`, this can be done using the following command:

```sh
npm install madr && mkdir -p docs/decisions && cp node_modules/madr/template/* docs/decisions/
```

### Create a new ADR

Manual approach:

1. Copy `adr-template.md` to `NNNN-title-with-dashes.md`, where `NNNN` indicates the next number in sequence.
2. Edit `NNNN-title-with-dashes.md`.
3. Update `index.md`, e.g., by executing `adr-log -d .`
   You can get [adr-log](https://github.com/adr/adr-log) by executing `npm install -g adr-log`.

Note you can also use [other patterns for the directory format](https://github.com/joelparkerhenderson/architecture_decision_record#adr-file-name-conventions), but then the tools cannot be applied.

Automatic approach:

There is currently no tooling supporting MADR 3.0.0.

## License

License: [CC0](https://creativecommons.org/share-your-work/public-domain/cc0)
