# Use Markdown Architectural Decision Records

Should we record the architectural decisions made in this project?
And if we do, how to structure these recordings?

## Considered Options

* Use [MADR](https://adr.github.io/madr/) 2.0.1 - The Markdown Architectural Decision Records
* Use other templates listed at <https://github.com/joelparkerhenderson/architecture_decision_record>
* No records

## Decision Outcome

Chosen option: "Use MADR 2.0.1", because:
- Implicit assumptions should be made explicit.
  Design documentation is important to enable people understanding the decisions later on.
  See also [A rational design process: How and why to fake it](https://doi.org/10.1109/TSE.1986.6312940).
- The MADR template is lean and fits our development style.
- Version 2.0.1 is the latest one available when starting to document ADRs.
