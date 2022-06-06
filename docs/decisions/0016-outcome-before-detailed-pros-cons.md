---
parent: Decisions
nav_order: 16
---
# Outcome before Detailed Pros and Cons

## Context and Problem Statement

MADR aims to list pros and cons of each option.
Where should that list be placed?

## Decision Drivers

* MADR should be easy to write
* MADR should be easy to read

## Considered Options

* Section "Pros and Cons of the Options" after "Decision Outcome"
* Section "Pros and Cons of the Options" before "Decision Outcome"

## Decision Outcome

Chosen option: "Section 'Pros and Cons of the Options' after 'Decision Outcome'", because this keeps the available options and the decision outcome close together.

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
