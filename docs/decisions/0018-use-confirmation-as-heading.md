---
parent: Decisions
nav_order: 18
---
# Use "Confirmation" as Heading

## Context and Problem Statement

In MADR, we want to include some sort of check that the decision was implemented.
How to name the heading for the explanation?

## Decision Drivers

* Consistent with terms used in IT
* Common word

## Considered Options

* "Confirmation"
* "Validation"
* "Verification"

## Decision Outcome

Chosen option: "Confirmation", because "validation" is out of scope of the template.
There is a process leading to a "valid" ADR.
The other term "verification" is often bound to a formal tool or formal procedure.
We wanted to enable also less formal checks.

### Confirmation

* Before next release; check that there is at least one example that has a "Confirmation" section.
* Before each release: check that templates and examples are still consistent with this decision (or update AD).
* Continuously: Monitor [GitHub issues](https://github.com/adr/madr/issues) for feedback on examples and template/tool change requests periodically.
