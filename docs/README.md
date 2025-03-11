Docs
----

This directory contains [hugo](https://gohugo.io) documentation to be published in Github pages.

Run Locally
-----------

Dependencies

- [Geekdocs v0.41.1](https://github.com/thegeeklab/hugo-geekdoc/releases/tag/v0.41.1)
- [Hugo v0.115.4](https://github.com/gohugoio/hugo/releases/tag/v0.115.4)

```shell
hugo server -D
```

This will serve the docs on [http://localhost:1313](http://localhost:1313).

Deploy to Github Pages
----------------------

Changes to the `master` branch will be deployed automatically with Github actions.

Update Geekdocs
---------------

The docs use the [Geekdocs](https://geekdocs.de/) theme. The theme is checked in to Github in the `./docs/themes/hugo-geekdoc/` folder. To update [Geekdocs](https://geekdocs.de/), remove the current folder and create a new one with the latest [release](https://github.com/thegeeklab/hugo-geekdoc/releases). There are no local modifications in `./docs/themes/hugo-geekdoc/`.

Notes
-----

Here's how the initial `docs/` folder was set up:

```shell
hugo new site docs
cd docs/
mkdir -p themes/hugo-geekdoc/
curl -L https://github.com/thegeeklab/hugo-geekdoc/releases/download/v0.41.1/hugo-geekdoc.tar.gz | tar -xz -C themes/hugo-geekdoc/ --strip-components=1
```

Create the initial `hugo.toml` file as described in [https://geekdocs.de/usage/getting-started/](https://geekdocs.de/usage/getting-started/).
