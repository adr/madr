---
nav_order: 1
---
# Markdown Any Decision Records [![part of ADR](https://img.shields.io/badge/part_of-ADR-blue.svg)](https://adr.github.io)

> "Markdown Any Decision Records" (MADR) `[ˈmæɾɚ]` – decisions that [matter `[ˈmæɾɚ]`](https://en.wiktionary.org/wiki/matter#Pronunciation).

MADR is a lean template to capture any decisions in a structured way.
The template originated from capturing architectural decisions and developed to a template allowing to capture any decisions taken.

<!-- markdownlint-disable-file MD036-->
**Note that this documentation describes MADR 3.0.0-alpha (not yet released) and might not apply to earlier released versions**

* [News](#news)
* [Overview](#overview)
* [Example](#example)
* [Apply it to your project](#apply-it-to-your-project)
  * [Initialization](#initialization)
  * [Create a new ADR](#create-a-new-adr)
  * [Lint ADRs](#lint-adrs)
* [Using in large projects](#using-in-large-projects)
  * [Usage of categories](#usage-of-categories)
* [License](#license)

## News

* 2021-04-25: MADR examples featured in Medium stories ["From Architectural Decisions to Design Decisions"](https://medium.com/olzzio/from-architectural-decisions-to-design-decisions-f05f6d57032b) and ["ADR = Any Decision Record?"](https://medium.com/olzzio/adr-any-decision-record-916d1b64b28d) <!-- and blog post ["ADR = Any Decision Record? Architecture, Design and Beyond"](https://ozimmer.ch/practices/2021/04/23/AnyDecisionRecords.html) -->
* 2021-04-08: MADR recommended as an ADR format in "Design Practice Repository". This ebook is available on [Leanpub](https://leanpub.com/dpr). The decision capturing activity is also described [online](https://socadk.github.io/design-practice-repository/activities/DPR-ArchitecturalDecisionCapturing.html).
* 2020-09-29: MADR presented in the keynote "Markdown Architectural Decision Records: Capturing Decisions Where the Developer is Working" at the workshop "[Second Software Documentation Generation Challenge (DocGen2)](https://dysdoc.github.io/docgen2/index.html)". Slides available at [Speaker Deck](https://speakerdeck.com/koppor/markdown-architecturaldecisionrecords-capturing-decisions-where-the-developer-is-working).
* 2019-07-08: MADR referenced in [Architectural Decisions — The Making Of](https://ozimmer.ch/practices/2020/04/27/ArchitectureDecisionMaking.html), a post in the new blog "The Concerned Architect" by Olaf Zimmermann (shorter version available on [Medium](https://medium.com/@docsoc/y-statements-10eb07b5a177)).
* 2018-04-13: Mentioned in [@vanto](https://github.com/vanto)'s presentation about ADRs: <https://speakerdeck.com/vanto/a-brief-introduction-to-architectural-decision-records>.
* 2018-04-03: Scientific publication: [Markdown Architectural Decision Records: Format and Tool Support](http://ceur-ws.org/Vol-2072/paper9.pdf).

## Overview

An [Architectural Decision (AD)](https://en.wikipedia.org/wiki/Architectural_decision) is a software design choice that addresses a functional or non-functional requirement that is architecturally significant.
This might, for instance, be a technology choice (e.g., Java vs. JavaScript), a choice of the IDE (e.g., IntelliJ vs. Eclipse IDE), a choice between a library (e.g., [SLF4J](https://www.slf4j.org/) vs [java.util.logging](https://docs.oracle.com/javase/8/docs/api/java/util/logging/package-summary.html)), or a decision on features (e.g., infinite undo vs. limited undo).
Do not take the term "architecture" too seriously or interpret it too strongly.
As the examples illustrate, any decisions that might have an impact on the architecture somehow are architectural decisions.

It should be as easy as possible to
a) write down the decisions and
b) to version the decisions.

There are debates what is an architecturally-significant decision and which decisions are not architecturally significant.
Since we believe that any (important) decision should be captured in a structured way, we offer the MADR template to capture any decision.

This repository offers a solution to record any decisions.
It provides files to document any decisions using **M**arkdown and **A**ny **D**ecision **R**ecords.

Before MADR 3.0.0, "MADR" stood for **M**arkdown and **A**rchitectural **D**ecision **R**ecords.
Since MADR 3.0.0, "Architectural" was replaced by "Any".

## Example

```markdown
# Use Markdown Any Decision Records

## Context and Problem Statement

We want to record any decisions made in this project independent whether decisions concern the architecture ("architectural decision record"), the code, or other fields.
Which format and structure should these records follow?

## Considered Options

* [MADR](https://adr.github.io/madr/) 3.0.0 – The Markdown Any Decision Records
* [Michael Nygard's template](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions) – The first incarnation of the term "ADR"
* [Sustainable Architectural Decisions](https://www.infoq.com/articles/sustainable-architectural-design-decisions) – The Y-Statements
* Other templates listed at <https://github.com/joelparkerhenderson/architecture_decision_record>
* Formless – No conventions for file format and structure

## Decision Outcome

Chosen option: "MADR 3.0.0", because

* Implicit assumptions should be made explicit.
  Design documentation is important to enable people understanding the decisions later on.
  See also [A rational design process: How and why to fake it](https://doi.org/10.1109/TSE.1986.6312940).
* MADR allows for structured capturing of any decision.
* The MADR format is lean and fits our development style.
* The MADR structure is comprehensible and facilitates usage & maintenance.
* The MADR project is vivid.
```

The example is rendered at [decisions/0000-use-markdown-any-decision-records.md](decisions/0000-use-markdown-any-decision-records.md).
The full template (with placeholders and some guidance how to use) can be found at [decisions/adr-template.md](decisions/adr-template.md).

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

#### Manual approach

1. Copy `docs/decisions/adr-template.md` to `docs/decisions/NNNN-title-with-dashes.md`, where `NNNN` indicates the next number in sequence.
2. Edit `NNNN-title-with-dashes.md`.

Note you can also use [other patterns for the directory format](https://github.com/joelparkerhenderson/architecture_decision_record#adr-file-name-conventions).
As a consequence, some existing tooling might not be applicable.

The filenames are following the pattern `NNNN-title-with-dashes.md` ([ADR-0005](docs/decisions/0005-use-dashes-in-filenames.md)), where

* `NNNN` is a consecutive number and we assume that there won't be more than 9,999 ADRs in one repository.
* the title is stored using dashes and lowercase, because [adr-tools] also does that.
* the suffix is `.md`, because it is a [Markdown](https://github.github.com/gfm/) file.

Decisions are placed in the subfolder `decisions/` to keep them close to the documentation but also separate the decisions from other documentation.

#### Automatic approach

There is currently no tooling supporting MADR 3.0.0.

### Lint ADRs

ADRs are written using Markdown.
Since markdown allows many styles, formatting can be incosistent.
To notify about inconsistencies, [markdownlint](https://github.com/DavidAnson/markdownlint#markdownlint) has been invented.
There is an initial configuration for it at `template/.markdownlint`.
You can use that configuration in a GitHub workflow.
See [`.github/workflows/lint.yaml`](.github/workflows/lint.yaml) for an example.

## Using in large projects

Large projects may have hunders decision records, where finding them might be hard.
MADR does not enforce any repository or directory organization structure.
In the following proposals from the community are presented

### Usage of categories

However, MADR leans forward to categorize ADRs using sub directories and put the ADRs into these sub folders.

Example folder structure could be as follows:

```tree
.
`-- decisions
    |-- backend
    |   |-- 0001-use-quarkus.md
    `-- ui
        `-- 0001-use-vuejs.md
```

With this approach, all categories are explicit, because the sub directories define the catories.
It is accepted, that numbers of ADRs are not unique throughout the repository any more, but local for a category.

Note that other alternatives are discussed at [ADR-0010](decisions/0010-support-categories.md).

## License

This work is dual-licensed under [MIT](https://opensource.org/licenses/MIT) and
[CC0](https://creativecommons.org/share-your-work/public-domain/cc0/).
You can choose between one of them if you use this work.

```yaml
SPDX-License-Identifier: MIT OR CC0-1.0
```
