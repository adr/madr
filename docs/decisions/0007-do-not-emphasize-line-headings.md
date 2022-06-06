---
parent: Decisions
nav_order: 7
---
# Do Not Emphasize Line Headings

## Context and Problem Statement

MADR contains lines such as `Chosen option: "[option 1]"`. Should "Chosen option" be emphasized?

## Decision Drivers

* MADR should be easy to read
* MADR should be easy to write

## Considered Options

* Do not emphasize line headings
* Emphasize line headings

## Decision Outcome

Chosen option: "Do not emphasize line headings", because 1) these headings always are put at the beginning of a line and followed by a colon. Thus, they are already easy to identified as line heading. 2) Readers not familiar with Markdown might be confused by stars in the text.
