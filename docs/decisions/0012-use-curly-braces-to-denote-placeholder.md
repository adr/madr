---
parent: Decisions
nav_order: 12
---
# Use Curly Braces to Denote Placeholders

## Context and Problem Statement

When crafting an ADR placeholders need to be replaced by real values.
How to mark the placeholders?

## Considered Options

* Use curly braces
* Use square brackets
* Use less-than and greater-than
* Use HTML comments

## Decision Outcome

Chosen option: "Use curly braces", because comes out best (see below).
Exception: In the `bare` templates, we use the HTML comment option, because these templates are used by pro users, who are not investigating the HTML for the template, but directly read Markdown.

## Pros and Cons of the Options

### Use curly braces

Example: `{option 1}`.

* Good, because [consistent to mustache templates](https://krasimirtsonev.com/blog/article/markdown-smart-placeholders).
* Good, because no confusion with markdown notation for links.
* Good, because clear distinction between comments on the template usage and placeholders.

### Use square brackets

Example: `[option 1]`.

* Good, because used in MADR 1.x and MADR 2.x.
* Good, because clear distinction between comments on the template usage and placeholders.
* Bad, because confusion with markdown notation for links.
* Bad, because some users did not remove the brackets. Example: `Date: [2021-03-12]` or `Good, because [user no longer activatess shortcut accidently when entering task]`.

### Use less-than and greater-than

Example: `<option 1>`

Idea taken from <https://github.com/schubmat/DecisionCapture/blob/master/templates/captureTemplate_full.md>

* Good, because kept in Markdown as is
* Good, because clear distinction between comments on the template usage and placeholders.
* Bad, because could be mixed up with an HTML element

### Use HTML comments

Example: `<!-- option 1 -->`.

* Good, because feels "natural" in direct Markdown editing
* Bad, because it does not render in HTML
