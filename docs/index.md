---
nav_order: 1
title: About MADR
---
<!-- markdownlint-disable MD025 -->
# Markdown Any Decision Records [![part of ADR](https://img.shields.io/badge/part_of-ADR-blue.svg)](https://adr.github.io)

> "Markdown Any Decision Records" (MADR) `[ˈmæɾɚ]` – decisions that [matter `[ˈmæɾɚ]`](https://en.wiktionary.org/wiki/matter#Pronunciation).

MADR is a lean template to capture any decisions in a structured way.
The template originated from capturing architectural decisions and developed to a template allowing to capture any decisions taken.

## Contents

* [News](#news)
* [Overview](#overview)
* [Example](#example)
* [Applying MADR to your project](#applying-madr-to-your-project)
  * [Initialization](#initialization)
  * [Create a new ADR](#create-a-new-adr)
  * [Lint ADRs](#lint-adrs)
* [Using MADR in large projects and product developments](#using-madr-in-large-projects-and-product-developments)
  * [Usage of categories](#usage-of-categories)
* [License](#license)

## News

* 2023-05-05: Two new blog posts discuss how to [create](https://medium.com/olzzio/how-to-create-architectural-decision-records-adrs-and-how-not-to-93b5b4b33080) and how to [review](https://medium.com/olzzio/how-to-review-architectural-decision-records-adrs-and-how-not-to-2707652db196) ADRs (and how not to). MADR is referenced in both.
* 2022-11-22: MADR Version 1.0 was released five years ago. A new blog post ["The Markdown ADR (MADR) Template Explained and Distilled"](https://medium.com/olzzio/the-markdown-adr-madr-template-explained-and-distilled-b67603ec95bb) is available on Medium.
* 2022-10-09: Release of MADR 3.0.0.\
  The most important change is the merged of sections "Positive Consequences" and "Negative Consequences" into "Consequences" to enable similar grammar as in "Pros and Cons of the Options".
  [[Full Changelog](https://github.com/adr/madr/blob/main/CHANGELOG.md#300--2022-10-09)]
* 2022-05-17: Release of MADR 3.0.0-beta.\
  Besides improvement of the template, there was a renaming from "Markdown Architectural Decision Records" to "Markdown Any Decision Records" to follow the movement ["ADR = Any Decision Record? Architecture, Design and Beyond"](https://ozimmer.ch/practices/2021/04/23/AnyDecisionRecords.html).
  The acronym is still MADR.
* 2021-04-25: MADR examples featured in Medium stories ["From Architectural Decisions to Design Decisions"](https://medium.com/olzzio/from-architectural-decisions-to-design-decisions-f05f6d57032b) and ["ADR = Any Decision Record?"](https://medium.com/olzzio/adr-any-decision-record-916d1b64b28d)
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
# Use Plain JUnit5 for advanced test assertions

## Context and Problem Statement

How to write readable test assertions?
How to write readable test assertions for advanced tests?

## Considered Options

* Plain JUnit5
* Hamcrest
* AssertJ

## Decision Outcome

Chosen option: "Plain JUnit5", because it is a standard framework and the features of the other frameworks do not outweigh the drawbrack of adding a new dependency.
```

For more examples see [examples](examples.md).
For the MADR project itself, all ADRs are rendered at [decisions/](decisions/).
Their source can be found at <https://github.com/adr/madr/tree/main/docs/decisions>.
The latest release of the full template (with placeholders and some guidance how to use) can be found at the [releases page](https://github.com/adr/madr/releases/latest).
By clicking on the number at the tag symbol, you browse the repository at the state of the release.
For the brave, the version under development is available at <https://github.com/adr/madr/blob/main/template/adr-template.md>.
There also is a [CHANGELOG](https://github.com/adr/madr/blob/main/CHANGELOG.md#changelog) listing the changes between the last released version and the currently developed version.

## Applying MADR to your project

### Initialization

Create folder `docs/decisions` in your project.
Copy all files in `template` from the MADR project to the folder `docs/decisions` in your project.

Using `npm`, this can be done using the following command:

```sh
npm install madr && mkdir -p docs/decisions && cp node_modules/madr/template/* docs/decisions/
```

### Create a new ADR

#### Manual approach

1. Copy [`docs/decisions/adr-template.md`](https://github.com/adr/madr/blob/main/template/adr-template.md) to `docs/decisions/NNNN-title-with-dashes.md`, where `NNNN` indicates the next number in sequence.
2. Edit `NNNN-title-with-dashes.md`.

Note you can also use [other patterns for the directory format](https://github.com/joelparkerhenderson/architecture_decision_record#adr-file-name-conventions).
As a consequence, some existing tooling might not be applicable.

The filenames are following the pattern `NNNN-title-with-dashes.md` ([ADR-0005](docs/decisions/0005-use-dashes-in-filenames.md)), where

* `NNNN` is a consecutive number and we assume that there won't be more than 9,999 ADRs in one repository.
* The title is stored using dashes and lowercase, because [adr-tools] also does that.
* The suffix is `.md`, because it is a [Markdown](https://github.github.com/gfm/) file.

Decisions are placed in the subfolder `decisions/` to keep them close to the documentation but also separate the decisions from other documentation.

#### Automatic approach

There is currently no tooling supporting MADR 3.0.0.

### Lint ADRs

ADRs are written using Markdown.
Since Markdown allows many styles, formatting can be inconsistent.
To notify about inconsistencies, [markdownlint](https://github.com/DavidAnson/markdownlint#markdownlint) has been invented.
There is an initial configuration for it at `template/.markdownlint`.
You can use that configuration in a GitHub workflow.
See [`.github/workflows/lint.yaml`](.github/workflows/lint.yaml) for an example.

## Using MADR in large projects and product developments

Large projects may accumulate hundreds of decision records over time, and finding them might be hard.
MADR does not enforce any repository or directory organization structure.
Some proposals from the community are presented in the following.

### Usage of categories

MADR logs may be categorized ADRs by defining sub directories and put the ADRs into these folders.

An examplary folder structure might follow the architectural structure of the system under construction:

```tree
.
`-- decisions
    |-- backend
    |   |-- 0001-use-quarkus.md
    `-- ui
        `-- 0001-use-vuejs.md
```

This approach makes all categories explicit because the sub directory/folder names define the categories.
As a consequence, numbers of ADRs are no longer unique throughout the repository, but locally within a category only.
Ideally, the ADR categorization the same organizing principles as other artifacts such as the code; using architectural structure breakdown is just one option and functional decomposition would be an additional one. This comes down to a meta-decision to be made rather early on.

Note that alternatives to categorization via subfolders are discussed at [ADR-0010](decisions/0010-support-categories.md).

## Full template

The current development version renders as follows:

```markdown
{% include_relative decisions/adr-template.md %}
```

## License

This work is dual-licensed under [MIT](https://opensource.org/licenses/MIT) and
[CC0](https://creativecommons.org/share-your-work/public-domain/cc0/).
You can choose between one of them if you use this work.

```yaml
SPDX-License-Identifier: MIT OR CC0-1.0
```
