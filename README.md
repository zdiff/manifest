# manifest
A container-based build system for compiling portable static binaries

## Available Packages

This repository provides Dockerfiles for building the following statically linked binaries:
- [alacritty](https://alacritty.org)
- [jj](https://www.jj-vcs.dev)
- [helix](https://helix-editor.com)
- [uutils coreutils](https://uutils.org/coreutils)
- [uutils-findutils](https://uutils.org/findutils/)
- [zellij](https://zellij.dev)


## Building Packages

1. Build the base container

   ```shell
   docker build -f base -t manifest-base .
   ```

1. Build a package. The list of available packages can be found in the [Available Packages section](#available-packages)
   ```shell
   docker build --output=. -f ${package} .
   ```

## Project Goals

- Packages are statically linked
- Packages are built from source
- Build Environments require a single dependency (Docker)
