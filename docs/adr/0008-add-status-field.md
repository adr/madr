# Add status field

Technical Story: <https://github.com/adr/madr/issues/2>

## Context and Problem Statement

ADRs have a status. Should this be tracked? And if it should, how should we track it?

## Considered Options

* Use badge
* Use text line
* Use separate heading
* Use table
* Do not add status

## Decision Outcome

Chosen option: "Use text line", because [justification. e.g., only option, which meets k.o. criterion decision driver | which resolves force | ... | comes out best (see below)].

## Pros and Cons of the Options

### Use badge

#### Examples

* ![grafik](https://user-images.githubusercontent.com/1366654/36786999-ca368324-1c88-11e8-966d-56f25980fd76.png)
* [![status-superseeded](https://img.shields.io/badge/status-superseeded_by_ADR_0001-orange.svg?style=flat-square)](https://github.com/adr/madr/blob/master/docs/adr/0001-use-CC0-as-license.md)

#### Pros/cons

* Good, because plain markdown
* Good, because looks good
* Bad, because hard to read in markdown source
* Bad, because relies on the online service https://shields.io or [local badges have to be generated](https://github.com/badges/shields#using-the-badge-library)
* Bad, because at local usages, many badges have to be generated (superseeded-by-ADR-0006, for each ADR number)
* Bad, because not easy to write

### Use text line

Example: `Status: Accepted`

* Good, because plain markdown
* Good, because easy to read
* Good, because easy to write
* Good, because looks OK in both markdown-source (MD) and in rendered versions (HTML, PDF)
* Good, because no dependencies on external tools
* Good, because single line indicates the current state
* Bad, because "Status" line needs to be maintained
* Bad, because uses space at the beginning. When users read MADR, they should directly dive into the context and problem and not into the status

### Use separate heading

Example:  ![grafik](https://user-images.githubusercontent.com/1366654/36787029-f5ea246c-1c88-11e8-9082-8e9531e4fac7.png)

* Good, because plain markdown
* Good, because easy to write
* Bad, because it uses much space: At least three lines: heading, status, separating empty line

### Use table

Example:  ![grafik](https://user-images.githubusercontent.com/1366654/36787043-0339a53e-1c89-11e8-8ebe-fb2a5752448c.png)

* Good, because history can be included
* Good, because multiple entries can be made
* Good, because already implemented in adr-tools fork
* Bad, because not covered by the [CommonMark specification 0.28 (2017-08-01)](http://spec.commonmark.org/0.28/)
* Bad, because hard to read
* Bad, because outdated entries cannot be easily identified
* Bad, because needs more markdown training

### Do not add status

* Good, because MADR is kept lean
* Bad, because users demand state field
* Bad, because not in line with other ADR templates
