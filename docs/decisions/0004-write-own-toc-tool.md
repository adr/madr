# Write own TOC tool

ADRs have to be indexed somehow. E.g., for offering a web site showing all ADRs.

## Considered Options

* Write the own tool `adr-log`
* Use adr-tools' TOC functionality

## Decision Outcome

Chosen option: Write own tool `adr-log`, because

* we want to have the format `ADR-0001 - Title` in the TOC.
* adr-tools offers `title` only.

We accept that changing adr-tools would also be possible.
It is prepared to included header and footer: <https://github.com/npryce/adr-tools/blob/master/tests/generate-contents-with-header-and-footer.sh>.

### Positive Consequences

* `adr-log` is installable using `npm install -g adr-log`, which is easier than installing `adr-tools`.

### Negative consequences

* Another tool has to be maintained
