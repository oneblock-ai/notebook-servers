# Notebook Images
[![publish](https://github.com/oneblock-ai/notebook-images/actions/workflows/notebook_servers_publish.yaml/badge.svg)](https://github.com/oneblock-ai/notebook-images/actions/workflows/notebook_servers_publish.yaml)
[![Releases](https://img.shields.io/github/release/oneblock-ai/notebook-images.svg)](https://github.com/oneblock-ai/notebook-images/releases)

This repository contains Dockerfiles and scripts to build the images for 1Block.Ai's Notebook Servers.

## Release Process

### Steps for releasing

1. Create a new release branch:
    ```sh
    VERSION="v0.1.0-rc.0"
    RELEASE_BRANCH="release/v0.1"
    git checkout -b $RELEASE_BRANCH origin/main
    ```
2. Commit changes to the release branch:
    ```sh
    git commit -s -a -m "Release $VERSION"
    ```
3. PR merged (after CI validates and builds all images for that commit).
4. CI job (postsubmit) kicks in and builds the images for $VERSION.
5. Tag commit as $VERSION.
