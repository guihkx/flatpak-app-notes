# Flatpak build of the [Notes](https://www.get-notes.com/) app

## Building

```bash
git clone https://github.com/guihkx/flatpak-app-notes.git
cd flatpak-app-notes
flatpak-builder --force-clean --sandbox --install-deps-from=flathub --arch=x86_64 --repo=repo/ builddir/ com.github.nuttyartist.notes.yaml
flatpak build-bundle --arch=x86_64 repo/ notes.flatpak com.github.nuttyartist.notes master
```

## Installing

```bash
flatpak install notes.flatpak
```

## TODO

- [x] Proper support for the autostart feature. (Done: https://github.com/nuttyartist/notes/pull/345)
- [ ] Once the above is done and a new version is released, get rid of `flatpak-autostart.patch`.
- [x] Check with upstream developers if `com.github.nuttyartist.notes` is their preferred app id. (Done: https://github.com/nuttyartist/notes/pull/345#issuecomment-1253394408)
- [x] ~~Use a better screenshot, preferably one taken on Linux.~~ (Done: The one I'm already using was taken on Linux, sorry)
- [ ] Find a volunteer who's willing to [submit](https://github.com/flathub/flathub/blob/master/CONTRIBUTING.md) Notes to Flathub and maintain it. If you're interested, just do it!
