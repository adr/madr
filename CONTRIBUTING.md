# Contributing to MADR

## Homepage

Homepage: Contribute to `gh-pages` branch (using a pull request).
The `docs/` folder of the `gh-pages` branch is the base of the content of <https://adr.github.io/madr/>.

## Template: Next version

Template: Contribute to `develop` branch (using a pull request).
The subdirectory `docs/` will be the new homepage after a release.
The current state is rendered at <https://develop--madr-develop.netlify.app/>.

As soon as a pull request is made, [netlify](https://www.netlify.com/) kicks off a build.
After a successful build, the link to the build is put as a comment to the pull request for inspection.

We use `develop` as branch name, because the name `main` does not definitively indicate whether it is the latest releae or the development version.

## Template: Patches to releases

The most recent releases of each major version are stored in the branch `release/v{x}`.
It is a branch, because the release version changes (and there are git users who do not like changing tags).

Please submit a pull request to that branch.
In case there are multiple fixes, we create a new branch `develop/v{x}` on demand.

Reasing: Wish at [#92](https://github.com/adr/madr/issues/92)
