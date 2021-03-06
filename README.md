Elm packages docset for Dash 
============================

![.github/workflows/prepare-packages.yaml](https://github.com/kraklin/Dash-User-Contributions/workflows/.github/workflows/prepare-packages.yaml/badge.svg?branch=master&event=workflow_dispatch)

This repository is the base for updating the [Elm packages](https://packages.elm-lang.org) docset for [Dash](https://kapeli.com/dash) and [Zeal](https://zealdocs.org/)

### Repository structure

This repository has been forked from [Kapeli/Dash-User-Contributions](https://github.com/Kapeli/Dash-User-Contributions). To be able to use the Github Actions automation I have branched the `master` to `docs` branch. 

The `docs` branch is being kept in sync with the upstream of [Kapeli/Dash-User-Contributions:master](https://github.com/Kapeli/Dash-User-Contributions) and branches for the upstream PRs with updated packages are being branched from it.

**You should never merge the `master` branch to the upstream master. Always use `docs` branch for that.**

### Generating docset

The docset is being generated by the GitHub Action. It is using the Docker image from [kraklin/elm-docset](https://github.com/kraklin/elm-docset) which takes care of these steps:
  - generate the Elm.docset and tar it
  - creates `docset.json` and `README.md` from the templates and updates the date and package count in them


