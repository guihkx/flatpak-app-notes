# About

Notes is an open source and cross-platform note-taking app that is both beautiful and powerful.

More information at: https://github.com/nuttyartist/notes

## Building

```bash
git clone https://github.com/guihkx/flatpak-app-notes.git
cd flatpak-app-notes
flatpak-builder --force-clean --sandbox --install-deps-from=flathub --arch=x86_64 --repo=repo/ builddir/ io.github.nuttyartist.notes.yaml
flatpak build-bundle --arch=x86_64 repo/ notes.flatpak io.github.nuttyartist.notes master
```

## Installing

```bash
flatpak install notes.flatpak
```

## TODO

- [ ] Replace `--socket=x11` by `--socket=fallback-x11` and `--socket=wayland` once https://github.com/nuttyartist/notes/issues/429 gets addressed.
- [ ] Upstream the AppStream metadata (`io.github.nuttyartist.notes.metainfo.xml`).
