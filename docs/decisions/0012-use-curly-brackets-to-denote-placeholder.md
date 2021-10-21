# Use curly brackets to denote placeholders

## Context and Problem Statement

When crafting an ADR placeholders need to be replaced by real values.
How to mark the place holders?

## Considered Options

* Use curly braces
* Use square brackets
* Use less-than and greater-than

## Decision Outcome

Chosen option: "Use curly braces", because comes out best (see below).

## Pros and Cons of the Options

### Use curly braces

Example: `{option 1}`.

* Good, because [consistent to mustache templates](https://krasimirtsonev.com/blog/article/markdown-smart-placeholders).
* Good, because no confusion with markdown notation for links

### Use square brackets

Example: `[option 1]`.

* Good, because used in MADR 1.x and MADR 2.x
* Bad, because confusion with markdown notation for links

### Use less-than and greater-than

Example: `<option 1>`

Idea taken from <https://github.com/schubmat/DecisionCapture/blob/master/templates/captureTemplate_full.md>

* Good, because kept in markdown as is
* Bad, because could be mixed up with an HTML element
