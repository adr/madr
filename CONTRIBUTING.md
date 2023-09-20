# Contributing to MADR

- Homepage: Contribute to `gh-pages` branch (using a pull request).
  The `docs/` folder of the `gh-pages` branch is the base of the content of <https://adr.github.io/madr/>.
- Template: Contribute to `develop` branch (using a pull request).
  The subdirectory `docs/` will be new homepage of the release.
  The current state is rendered at <https://develop--madr-develop.netlify.app/>.
- Older version of the template: `develop/v{x}`, where `{x}` is the major version you want to contribute.
  In case no such branch exists, contribute to `release/v{x}`.
  We will create the respective development branch.

As soon as a pull request is made, [netlify](https://www.netlify.com/) kicks off a build.
After a successful build, the link to the build is put as a comment to the pull request for inspection.
