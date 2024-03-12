---
parent: Decisions
nav_order: 14
---
# Allow "neutral" arguments

## Context and Problem Statement

Sometimes, one wants to write down an argument, which is neither pro nor con.

## Considered Options

* Neutral, because …
* OK, because …
* Good/bad, because …
* Interesting, because …
* Indifferent, because …

## Decision Outcome

Chosen option: "Neutral, because …", because

* it fits best.
* it is consistent to patterns: +/0/-

## Pros and Cons of the Options

### Neutral, because …

In the following, a full pro/con list is given:

Example:

* The proposed solution is good, because it resolves the force 1.
* The proposed solution is good, because it addresses decision driver 2.
* The proposed solution is good, because it mitigates the technical risk / dept with respect to decision driver 4.
* The proposed solution is good, because it removes architectural smell …
* The proposed solution is good, because it addresses stakeholder concern …
* The proposed solution is good, because it has a positive effect on the performance (quality property).
* The proposed solution is neutral, because it is indifferent to decision driver 2.
* The proposed solution is bad, because it does not address decision driver 3.
* The proposed solution is bad, because it has a negative effect on the maintainability (quality property).

Shorter example for pros and cons:

* The proposed solution is good with respect to resolving the force 1.
* The considered option is a good solution, because it resolves force1 and the non-resolving of force 1 is OK, …

### OK, because …

Real world example: <https://github.com/island-is/handbook/blob/master/docs/adr/0005-error-tracking-and-monitoring.md>

```markdown
### Bugsnag

- Good, because it offers a Slack integration for faster feedback.
- Good, because it offers a Github integration to link to possible commits and PRs.
- Good, because it offers bot front-side/server-side/serverless error tracking.
- OK, because it was ranked the **\#5** as the best Javascript (client-side) error logging service in a community survey.
- Bad, because it's expensive. (**\$199/mo** for **450k events** and **15 collaborators**)
- Bad, because it's pricing includes a fixed set of collaborators.
```
