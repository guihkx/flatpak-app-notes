# Archived

This has been upstreamed at: https://github.com/flathub/io.github.nuttyartist.notes

# About

Notes is an open source and cross-platform note-taking app that is both beautiful and powerful.

More information at: https://github.com/nuttyartist/notes

This repo is currently used as a testing playground, in preparation to submit Notes to [Flathub](https://flathub.org/).

# Installation

You can download the latest stable version from the [Releases page](https://github.com/guihkx/flatpak-app-notes/releases).

But if you're feeling adventurous, you can grab the latest development build from the [CI pipeline](https://github.com/guihkx/flatpak-app-notes/actions/workflows/flatpak.yml).

To install the package for all users, open a terminal window and run:

```bash
flatpak install notes_*-x86_64.flatpak
```

And you're good to go. You should find Notes in your apps list.

# Advanced

## Building

Before proceding, make sure both `flatpak` and `flatpak-builder` packages are installed.

64-bit AMD/Intel:

```bash
# Build
flatpak-builder --arch x86_64 --delete-build-dirs --force-clean --install-deps-from flathub --repo repo/ --sandbox builddir/ io.github.nuttyartist.notes.yaml
# Create a single-bundle file
flatpak build-bundle --arch x86_64 repo/ notes-x86_64.flatpak io.github.nuttyartist.notes master
# Install it
flatpak install notes-x86_64.flatpak
```

64-bit ARM:

```bash
# Build
flatpak-builder --arch aarch64 --delete-build-dirs --force-clean --install-deps-from flathub --repo repo/ --sandbox builddir/ io.github.nuttyartist.notes.yaml
# Create a single-bundle file
flatpak build-bundle --arch aarch64 repo/ notes-aarch64.flatpak io.github.nuttyartist.notes master
# Install it
flatpak install notes-aarch64.flatpak
```
