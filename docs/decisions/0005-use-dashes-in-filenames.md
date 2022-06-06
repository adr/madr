---
parent: Decisions
nav_order: 5
---
# Use Dashes in Filenames

## Context and Problem Statement

What is the pattern of the filename where an ADR is stored?

## Considered Options

* `NNNN-title-with-dashes.md` - format used by [adr-tools](https://github.com/npryce/adr-tools)
* `YYYY-MM-DD Title` - see <https://github.com/joelparkerhenderson/architecture_decision_record#adr-file-name-conventions>

## Decision Outcome

Chosen option: "`NNNN-title-with-dashes.md`", because

* `NNNN` provides a unique number, which can be used for referencing in the forms
  * `ADR-0001` in plain text and
  * by `@ADR(1)` Java code (enabled by [e-adr](https://adr.github.io/e-adr/))
* The creation time of an ADR is of historical interest only, if it gets updated somehow.
  The arguments are similar than the ones by [Does Git have keyword expansion?](https://git.wiki.kernel.org/index.php/GitFaq#Does_Git_have_keyword_expansion.3F)
* Having no spaces in filenames eases working in the command line
* This is exactly the format offered by [adr-tools](https://github.com/npryce/adr-tools)
