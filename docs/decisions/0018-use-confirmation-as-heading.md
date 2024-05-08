---
parent: Decisions
nav_order: 18
---
<!-- we need to disable MD025, because we use the different heading "ADR Template" in the homepage (see above) than it is foreseen in the template -->
<!-- markdownlint-disable-next-line MD025 -->
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
The other term "Verification" is often bound to a formal tool or formal procedure.
We wanted to enable also less formal checks.
