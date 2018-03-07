# Use Markdown Architectural Decision Records

Should we record the architectural decisions made in this project?
And if we do, how to structure these recordings?

## Considered Options

* Use [MADR](https://adr.github.io/madr/) 2.0.1 - The Markdown Architectural Decision Records
* [Michael Nygard's template](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions) - The first incarnation of the term "ADR". Maintainable by [adr-tools](https://github.com/npryce/adr-tools).
* [Sustainable Architectural Decisions](https://www.infoq.com/articles/sustainable-architectural-design-decisions) - The Y-Statements
* Other templates listed at <https://github.com/joelparkerhenderson/architecture_decision_record>
* No records

## Decision Outcome

Chosen option: MADR 2.0.1, because:
- Implicit assumptions should be made explicit.
  Design documentation is important to enable people understanding the decisions later on.
  See also [A rational design process: How and why to fake it](https://doi.org/10.1109/TSE.1986.6312940).
- The MADR template is lean and fits our development style.
- Version 2.0.1 is the latest one available when starting to document ADRs.
