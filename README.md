# Corebird Flatpak

This is a `flatpak-builder` definition file to build both corebird master and current stable branches.

Due to corebird opening a browser whenever a link is clicked, as well as when setting up an account, you need to have `xdg-desktop-portal` as well as one implementation for it (currently there is only `xdg-desktop-portal-gtk` as far as I know) installed.

[Get Flatpak using these instructions](http://flatpak.org/getting.html)

**For the stable version, see Corebird on Flathub: https://flathub.org/apps.html**

## Nightly Version

The nightly version is rebuilt every time a bigger change lands.

```shell
flatpak install --from http://baedert.org/repo/org.baedert.corebird.nightly.flatpakref
```
