---
parent: Decisions
nav_order: 19
status: "accepted"
---
# Handling of the "Consequences" Section in the Minimal Template

## Context and Problem Statement

The minimal template ([`adr-template-minimal.md`](adr-template-minimal.md)) contains the section "Consequences", but marks it as optional via an HTML comment (`<!-- This is an optional element. Feel free to remove. -->`).
This was reported as confusing in [#218](https://github.com/adr/madr/issues/218):

* If a section in the *minimal* template is optional, the template no longer represents a minimal ADR, since an even smaller document is possible.
* The "optional" hint is only an HTML comment, so it is invisible in the rendered preview and absent entirely from the bare-minimal variant.
* ADRs without consequences carry little value: the "why" and the trade-offs are exactly the information that cannot be reconstructed later.

How should the "Consequences" section be treated in the minimal template?

## Decision Drivers

* "Minimal" should mean "the smallest set of sections we still recommend" — no further reduction implied.
* The recorded decision should retain enough information to be understood years later (the consequences / "why").
* Consistency across the four template variants (full, minimal, bare, bare-minimal).
* Prior art: the [adr-manager](https://github.com/adr/adr-manager) web editor offers a "basic" mode ("Only show required fields") that contains **no** Consequences and points users to "professional" mode, and a "professional" mode ("Show all fields") that does.

## Considered Options

* Keep "Consequences" optional in the minimal template (status quo)
* Make "Consequences" a required section of the minimal template
* Remove "Consequences" from the minimal template entirely (mirror the adr-manager "basic" mode)
* Introduce a new "medium" template tier that contains "Consequences" (optional), keep the minimal template without "Consequences"

## Decision Outcome

Chosen option: "Make 'Consequences' a required section of the minimal template", because it directly resolves the reported confusion, keeps the trade-offs (the hardest-to-reconstruct information) in every recommended ADR, and avoids adding a further template variant that maintainers must keep in sync.

In the full template, "Consequences" stays optional, but it shares that role with "Pros and Cons of the Options"; the templates note that at least one of the two should be present.

### Consequences

* Good, because every minimal ADR records the trade-offs of the decision.
* Good, because it is consistent with [Michael Nygard's original ADR format](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions.html), where "Consequences" is a core section.
* Good, because the "minimal" name is honest: every listed section is required.
* Good, because no new template variant is introduced; the existing four stay in sync.
* Bad, because it diverges from the adr-manager "basic" mode, which currently omits Consequences (adr-manager would need to be aligned).
* Bad, because authors who genuinely have nothing to note under "Consequences" can no longer drop the section from the minimal template.

## Pros and Cons of the Options

### Keep "Consequences" optional in the minimal template

* Bad, because it is the reported source of confusion: a *minimal* template with an optional section is not minimal.
* Bad, because the optional marker is an invisible HTML comment, missing from the bare-minimal variant.

### Make "Consequences" a required section of the minimal template

* Good, because the trade-offs are always captured.
* Good, because consistent with Michael Nygard's original ADR format, where "Consequences" is a core section.
* Good, because no new variant; least maintenance.
* Bad, because it diverges from adr-manager "basic" mode.

### Remove "Consequences" from the minimal template entirely

* Good, because it matches adr-manager's "basic" mode exactly.
* Bad, because it drops the single most valuable piece of information for future readers — the opposite of what [#218](https://github.com/adr/madr/issues/218) asks for.

### Introduce a new "medium" template tier with optional "Consequences"

* Good, because it offers a graded path (minimal → medium → full).
* Bad, because designing it is unclear, and a fifth variant (plus its bare form) increases the number of files to keep consistent.
* Bad, because it does not by itself fix the minimal template; it sidesteps the question.

## More Information

* Issue: [#218](https://github.com/adr/madr/issues/218)
* adr-manager mode handling: `src/components/EditorMadrDecisionOutcome.vue` ("Note that you can add consequences in professional mode.") and `src/components/ToolbarMenuMode.vue` ("basic" = "Only show required fields", "professional" = "Show all fields").
