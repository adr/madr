---
parent: Decisions
nav_order: 10
---
# Support Categories

## Context and Problem Statement

ADRs are recorded. The number of ADRs grows and the context/topic/scope of ADRs might be different (e.g., frontend, backend)

## Decision Drivers

* Easy to find groups ADRs in hundreds of ADRs
* Easy to group
* Easy to create
* Good finding without external tooling
* Keep newcomers in mind (should be doable in <10 minutes)
* Keep template lean

## Considered Options

* Use labels
* Add `* Category: CATEGORY` directly under the heading (similar to <https://gist.github.com/FaKleiser/2f9c63b6e1d436abb7358b68bf396f57>)
* Use YAML front matter
* Encode category in filename
* Use subfolders with local IDs
* Use subfolders with global IDs
* Don't do it.

## Decision Outcome

Chosen option: "Use subfolders with local IDs", because comes out best (see below).

## Pros and Cons of the Options

### Use labels

Example:  

Use Angular ![category-frontend](https://img.shields.io/badge/category-frontend-blue.svg?style=flat-square)

`![category-frontend](https://img.shields.io/badge/category-frontend-blue.svg?style=flat-square)`

* Good, because full markdown
* Good, because linking to an overview page is possible (using markdown)
* Bad, because not straight-forward to parse
* Bad, because no simple filtering using `ls` or Windows Explorer is possible

### Add `* Category: CATEGORY` directly under the heading

* Good, because full markdown
* Good, because linking to an overview page is possible (using markdown)
* Good, because straight-forward to parse
* Bad, because no simple filtering using `ls` or Windows Explorer is possible

### Use YAML front matter

Example:

```yaml
---
category: frontend
---
```

* Good, because nearly straight-forward to parse
* Good, because Jekyll supports it
* Bad, because YAML front matter is not part of the [CommonMarc Spec](http://spec.commonmark.org/)
* Bad, because no simple filtering using `ls` or Windows Explorer is possible

### Encode category in filename

Example: `0050--frontend--title-with-dashes.md`

* Good, because programmatic filtering is possible
* Good, because `ls -la | grep --category--` works
* Bad, because plain file list in Windows explorer cannot be filtered
* Bad, because as bad as [TagSpaces](https://www.tagspaces.org/), which stores the tags in the filenames in brackets. E.g., `demo[demotag secondtag].md`.

### Use subfolders with local IDs

Optionally "to-be-categorized" folder.

One level of subfolder, not nested

#### Examples

* `docs/decisions/smar/0000-secure-entities.md`
* `docs/decisions/smar/0001-flexible-properties-selection.md`

#### Pros/cons

* Good, because grouping is done by folders (which are natural for grouping)
* Good, because typos can easily be spotted
* Bad, because there is no unique number identifying an ADR
* Bad, because two indices have to be maintained (`adr-log` needs to be updated)
* Bad, because [e-adr](https://github.com/adr/e-adr) needs to be adapted to `@ADR("category", number)` (not that bad)
* Bad, because when category is unknown it is hard to find the right folder
* Bad, because using categories might be hampering newcomers

### Use subfolders with global IDs

#### Examples

* `docs/decisions/smar/0005-secure-entities.md`
* `docs/decisions/smar/0047-flexible-properties-selection.md`
