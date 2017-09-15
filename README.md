# Markdown Architectural Decision Records

This repository provides an initial directory structure and files to document Architectural Decisions using Architectural Decision Records and Markdown.

"Markdown Architectural Decision Records" (MADR) `[ˈmæɾɚ]` - architectural decisions that [matter `[ˈmæɾɚ]`](https://en.wiktionary.org/wiki/matter#Pronunciation).

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

The template is available at [docs/adr/template.md](docs/adr/template.md).


## Example

```markdown
# Use Markdown Architectural Decision Records (MADR)

Should we record the architectural decisions made in this project?
And if we do, wow to structure these recordings?

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

The example is rendered at [docs/adr/0000-use-markdown-architectural-decision-records.md](https://github.com/adr/madr/blob/master/docs/adr/0000-use-markdown-architectural-decision-records.md)


## Apply It To Your Project

You can apply it to your project by copying the whole `docs` folder in the root of your project.
When adding a new architectural decision:

1. Copy `template.md` to `ADRnnnn-t.md`, where `nnnn` indicates the next number in sequence and `t` the title with dashes.
2. Edit `ADRnnnn-t.md`.


## Background Information

The template is based on [DecisionCapture](https://github.com/schubmat/DecisionCapture/) by [@schubmat](https://github.com/schubmat/). For more information on ADRs check <http://adr.github.io>.

The [Y-Statements](https://www.infoq.com/articles/sustainable-architectural-design-decisions) are the most prominent alternative of this template.
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


## Using this Template

1. Copy the `docs/adr` folder into your project.
2. For each new ADR: copy `template.md` to `NNNN-title-with-dashes.md`, where `NNNN` is the next number
3. Update `index.md`


## License

License: [CC0](https://creativecommons.org/share-your-work/public-domain/cc0)
