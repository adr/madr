---
parent: Decisions
nav_order: 3
status: on hold
---
# Write Own MADR Tooling

## Context and Problem Statement

Developers seem to like tooling to create ADRs.
That tooling should support MADR.
The tooling should be easy to install.

## Considered Options

* Include in [adr-tools](https://github.com/npryce/adr-tools), 924 stars as of 2018-06-14
* Include in [adr-j](https://github.com/adoble/adr-j), 2 stars as of 2018-06-14
* Include in [adr](https://github.com/phodal/adr), 72 stars as of 2018-06-14
* Write own MADR tooling
* No tool support

## Decision Outcome

Chosen option: "Write own MADR tooling", because

* adding MADR support to `adr-tools` [was rejected](https://github.com/npryce/adr-tools/pull/43)
* other tooling seem to a) modify MADR or b) do not keep up with changes on MADR.

We accept that this comes with maintenance cost.

## More Information

An overview on current tooling of MADR is available at <https://adr.github.io/madr/tooling.html>.
