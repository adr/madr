# Support links between ADRs inside an ADRs

Technical Story: https://github.com/adr/madr/issues/9

## Considered Options

* Use tables
* Use heading together with a bullet list directly after status
* Use heading together with a bullet list directly after "Decision Outcome"
* Use heading together with a bullet list at the end
* Don't add links

## Decision Outcome

Chosen option: "Use heading together with a bullet list at the end", because comes out best (see below).

## Pros and Cons of the Options

### Use tables

* Good, because easy to write
* Good, because history is shown (enabled by concept)
* Good, because current adr-tools support (https://github.com/npryce/adr-tools/pull/43) uses tables to describe links.
* Bad, because not supported by the CommonMark spec
* Bad, because unclear whether a link was superseeded by another one
* Bad, because valid links not clear at first sight (there might be outdated links shown)

### Use heading together with a bullet list directly after status

Example:
![grafik](https://user-images.githubusercontent.com/1366654/36787434-6a63e318-1c8a-11e8-8824-4dd7b3d0f2c6.png)

* Good, because easy to write
* Good, because supported by the CommonMark spec
* Bad, because not consistent with the status label (refs https://github.com/adr/madr/issues/2)

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

### Don't add links

* Good, because template stays minimal
