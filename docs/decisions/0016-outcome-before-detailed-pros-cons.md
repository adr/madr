---
parent: Decisions
nav_order: 16
---
# Outcome before Detailed Pros and Cons

## Context and Problem Statement

MADR aims to list pros and cons of each option.
Where should that list be placed?

## Decision Drivers

* Most important information should be above the fold.
* MADR should be easy to write.
* MADR should be easy to read.

## Considered Options

* Section "Pros and Cons of the Options" after "Decision Outcome"
* Section "Pros and Cons of the Options" before "Decision Outcome"

## Decision Outcome

Chosen option: "Section 'Pros and Cons of the Options' after 'Decision Outcome'", because this keeps the available options and the decision outcome close together.
One gets the decision outcome above the fold and preserve a nice logical flow.
Hence, one can see the "Pros and Cons" section as a sort of "appendix" to the considered options section.
It is almost like the "Considered Options" section implies the following sentence: "For a more detailed analysis of these options, refer to pros and cons".

## Pros and Cons of the Options

### Section "Pros and Cons of the Options" after "Decision Outcome"

Illustration:

```markdown
## Considered Options

...

## Decision Outcome

...

## Pros and Cons of the Options

...
```

* Good, because this keeps the available options and the decision outcome close together.
* Bad, because readers might be confused, because the logical flow broken: First comes the result, then the detailed arguments.

### Section "Pros and Cons of the Options" before "Decision Outcome"

Illustration:

```markdown
## Considered Options

...

## Pros and Cons of the Options

...

## Decision Outcome

...
```

* Good, because the logical flow is kept
* Bad, because the decision outcome is not close to the options
* Bad, because "small" MADRs with the list of options and the decision outcome (and not containing the section "Pros and Cons of the Options")
* Bad, because "small" MADRs with the list of options and the decision outcome (and not containing the section "Pros and Cons of the Options")
