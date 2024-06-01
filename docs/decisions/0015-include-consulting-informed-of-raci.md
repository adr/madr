---
parent: Decisions
nav_order: 15
---
# Include "Consulted" and "Informed" of RACI

## Context and Problem Statement

We noticed an intersection between MADR and [RACI](https://en.wikipedia.org/wiki/Responsibility_assignment_matrix), and felt the need to add a "consulted" and "informed" field in addition to "decision maker(s)".
Would it be beneficial to "upstream" these fields to MADR?

MADR Issue: [#62](https://github.com/adr/madr/issues/62).

## Decision Drivers

* MADR should contain fields important to the ADR decision process
* MADR template should be easy to understand
* MADR should be lightweight

## Considered Options

* Include "Consulted" and "Informed" of RACI
* Include all fields of RACI
* Do not include anything of RACI

## Decision Outcome

Chosen option: "Include 'Consulted' and 'Informed' of RACI", because comes out best (see below).

## Pros and Cons of the Options

### Include "Consulted" and "Informed" of RACI

* Good, because these two roles of RACI are well understood.
* Good, because we make these fields optional, thus it keeps MADR still lightweight.
* Bad, because it adds two additional fields

### Include all fields of RACI

This would add "Responsible", "Accountable", "Consulted", and "Informed"

* Good, because complete RACI would be included
* Bad, because get confused about who is "accountable" and who is "responsible".
* Bad, because if decisions are mostly taken by consensus in small committees, then there might not be an "accountable" person.
