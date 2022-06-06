---
parent: Decisions
nav_order: 9
---
# Support Links To Other ADRs Inside an ADR

## Context and Problem Statement

A decision might point to another decision.
For instance, if a decision is a follow-up to another decision.
This should be supported by MADR, too.

Technical Story: <https://github.com/adr/madr/issues/9>

## Considered Options

* Include in section "More Information"
* Use tables
* Use heading together with a bullet list directly after status
* Use heading together with a bullet list directly after "Decision Outcome"
* Use heading together with a bullet list at the end
* Do not add links

## Decision Outcome

Chosen option: "Include in section 'More Information'", because comes out best (see below).

## Pros and Cons of the Options

### Include in section "More Information"

Example:

```markdown
## More Information

[ADR-0008](0008-add-status-field.md) reasons on adding meta data (such as status).
```

* Good, because provides freedom to the user
* Bad, because parsing gets harder

### Use tables

* Good, because easy to write
* Good, because history is shown (enabled by concept)
* Good, because [current `adr-tools`' support](https://github.com/npryce/adr-tools/pull/43) uses tables to describe links.
* Bad, because not supported by the CommonMark spec
* Bad, because unclear whether a link was super seeded by another one
* Bad, because valid links not clear at first sight (there might be outdated links shown)

### Use heading together with a bullet list directly after status

Example:
![grafik](https://user-images.githubusercontent.com/1366654/36787434-6a63e318-1c8a-11e8-8824-4dd7b3d0f2c6.png)

* Good, because easy to write
* Good, because supported by the CommonMark spec
* Bad, because not consistent with the status label (refs <https://github.com/adr/madr/issues/2>)

### Use heading together with a bullet list directly after "Decision Outcome"

* Good, because easy to write
* Good, because supported by the CommonMark spec
* Good, because the options are first introduced and then the links
* Good, because consistent with position of "Decision Outcome"
* Bad, because reader might get distracted: He might expect explanation of the options instead of links to something else
* Bad, because not consistent with scientific papers, where related work and future work are coming after the discussion of the content.

### Use heading together with a bullet list at the end

* Good, because easy to write
* Good, because supported by the CommonMark spec
* Good, because the options and pros/cons are kept together with the option list.
* Good, because consistent with pattern format

### Do not add links

* Good, because template stays minimal
