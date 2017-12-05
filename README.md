# Markdown Architectural Decision Records

> "Markdown Architectural Decision Records" (MADR) `[ˈmæɾɚ]` – architectural decisions that [matter `[ˈmæɾɚ]`](https://en.wiktionary.org/wiki/matter#Pronunciation).

An [Architectural Decision (AD)](https://en.wikipedia.org/wiki/Architectural_decision) is a software design choice that addresses a functional or non-functional requirement that is architecturally significant. 
This might, for instance, be a technology choice (e.g., Java vs. JavaScript), a choice of the IDE (e.g., IntelliJ vs. Eclipse IDE), a choice between a library (e.g., [SLF4J](https://www.slf4j.org/) vs [java.util.logging](https://docs.oracle.com/javase/8/docs/api/java/util/logging/package-summary.html)), or a decision on features (e.g., infinite undo vs. limited undo).
Do not take the term "architecture" too serious or interpret it too strong.
As the examples illustrate, any decision might have impact on the architecture somehow are architectural decisions.

It should be as easy as possible to
a) write down the decisions and
b) to version the decisions.

This repository offers a solution to record architectural decisions.
It provides provides an initial directory structure and files to document Architectural Decisions using **M**arkdown and **A**rchitectural **D**ecision **R**ecords.

## Table of Contents

<!-- toc -->

- [The Template](#the-template)
- [Example](#example)
- [Apply It To Your Project](#apply-it-to-your-project)
  * [Initialization](#initialization)
  * [Create a new ADR](#create-a-new-adr)
- [Background Information](#background-information)
- [License](#license)

<!-- tocstop -->

## The Template

The template reads as follows:

```markdown
# *[short title of solved problem and solution]*

**User Story:** *[ticket/issue-number]* <!-- optional -->

*[context and problem statement]*
*[decision drivers | forces]* <!-- optional -->

## Considered Alternatives

* *[alternative 1]*
* *[alternative 2]*
* *[alternative 3]*
* *[...]* <!-- numbers of alternatives can vary -->

## Decision Outcome

* Chosen Alternative: *[alternative 1]*
* *[justification. e.g., only alternative, which meets k.o. criterion decision driver | which resolves force force | ... | comes out best (see below)]*
* *[consequences. e.g., negative impact on quality attribute, follow-up decisions required, ...]* <!-- optional -->

## Pros and Cons of the Alternatives <!-- optional -->

### *[alternative 1]*

* `+` *[argument 1 pro]*
* `+` *[argument 2 pro]*
* `-` *[argument 1 con]*
* *[...]* <!-- numbers of pros and cons can vary -->

### *[alternative 2]*

* `+` *[argument 1 pro]*
* `+` *[argument 2 pro]*
* `-` *[argument 1 con]*
* *[...]* <!-- numbers of pros and cons can vary -->

### *[alternative 3]*

* `+` *[argument 1 pro]*
* `+` *[argument 2 pro]*
* `-` *[argument 1 con]*
* *[...]* <!-- numbers of pros and cons can vary -->
```

The template is available at [template/template.md](template/template.md).


## Example

```markdown
# Use Markdown Architectural Decision Records (MADR)

Should we record the architectural decisions made in this project?
And if we do, how to structure these recordings?

## Considered Alternatives

* [MADR](https://github.com/adr/madr) - Markdown Architectural Decision Records
* [Michael Nygard's template](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions) - The first incarnation of the term "ADR". Maintainable by [adr-tools](https://github.com/npryce/adr-tools).
* [Sustainable Architectural Decisions](https://www.infoq.com/articles/sustainable-architectural-design-decisions) - The Y-Statements
* [DecisionRecord](https://github.com/schubmat/DecisionCapture) - Agile records by [@schubmat](https://github.com/schubmat/)
* Other templates listed at <https://github.com/joelparkerhenderson/architecture_decision_record>
* No records

## Decision Outcome

* Chosen Alternative: MADR
* The MADR template is lean and fits our development style.
```

The example is rendered at [template/0000-use-markdown-architectural-decision-records.md](template/0000-use-markdown-architectural-decision-records.md)

For the MADR project itself, all ADRs are exist at [docs/adr/](docs/adr/).

## Apply It To Your Project

### Initialization

Create folder `docs/adr` in your project.
Copy all files in `template` from the MADR project to the folder `docs/adr` in your project.

For instance, using `npm`, this can be done using the following command:

```sh
$ npm install madr && mkdir -p docs/adr && cp node_modules/madr/template/* docs/adr/
```

### Create a new ADR

Manual approach:

1. Copy `template.md` to `NNNN-title-with-dashes.md`, where `NNNN` indicates the next number in sequence.
2. Edit `NNNN-title-with-dashes.md`.
3. Update `index.md`, e.g., by executing `adr-log -d .`
   You can get adr-log from <https://github.com/adr/adr-log>.

We are working to enhance an adr tool (such as
[adr-j](https://github.com/adoble/adr-j),
[adr-tools](https://github.com/npryce/adr-tools), or
[adr](https://www.npmjs.com/package/adr))
to provide support for MADR.

## Background Information

The Y-Statements (presented as "[Sustainable Architectural Design Decisions](https://www.infoq.com/articles/sustainable-architectural-design-decisions)") are the most prominent alternative of this template.
They are even shorter as their minimal form is just one sentence:

```
In the context of <use case/user story u>,
facing <concern c>
we decided for <option o>
and neglected <other options>,
to achieve <system qualities/desired consequences>,
accepting <downside d/undesired consequences>,
because <additional rationale>.
```

Both MADR and the Y-Statements can embedded in Java code using the [e-adr library](https://github.com/adr/e-adr).

For more information on ADRs check <http://adr.github.io>.


## License

License: [CC0](https://creativecommons.org/share-your-work/public-domain/cc0)
