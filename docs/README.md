# Web Page of MADR

The web site is created using the Jekyll Theme [Just the Docs](https://just-the-docs.github.io/just-the-docs/).

## Local Development

For local development, follow the [Jekyll installation instructions](https://jekyllrb.com/docs/installation/).
Installing the latest version of ruby followed by `gem install bundler` should be enough.

Afterwards, run

```terminal
bundle install
jekyll serve --livereload
```

and go to <http://localhost:4000/> in your browser.

On **Windows**, using a dockerized environment is recommended:

```terminal
docker build . -t madrjekyll
docker run -p 4000:4000 -it --rm --volume="C:\git-repositories\madr\docs":/srv/jekyll madrjekyll jekyll serve -H 0.0.0.0 -t
```

* With <kbd>Ctrl</kbd>+<kbd>C</kbd> you can stop the server (this is enabled by the `-it` switch).
* In case you get errors regarding `Gemfile.lock`, just delete `Gemfile.lock` and rerun.

<!-- markdownlint-disable-file MD033 -->
