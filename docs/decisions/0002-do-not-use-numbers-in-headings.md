---
parent: Decisions
nav_order: 2
---
# Do Not Use Numbers in Headings

## Context and Problem Statement

How to render the first line in an ADR?
ADRs have to take a unique identifier.

## Considered Options

* Use the title only
* Add the ADR number in front of the title (e.g., "# 2. Do not use numbers in headings")

## Decision Outcome

Chosen option: "Use the title only", because

* This is common in other markdown files, too.
  One does not add numbering manually at the markdown files, but tries to get the numbers injected by the rendering framework or CSS.
* Enables renaming of ADRs (before publication) easily
* Allows copy'n'paste of ADRs from other repositories without having to worry about the numbers.
