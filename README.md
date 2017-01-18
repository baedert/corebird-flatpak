# Corebird Flatpak

This is a `flatpak-builder` definition file to build both corebird master and current stable branches.

Due to corebird opening a browser whenever a link is clicked, as well as when setting up an account, you need to have `xdg-desktop-portal` as well as one implementation for it (currently there is only `xdg-desktop-portal-gtk` as far as I know) installed.

[Get Flatpak using these instructions](http://flatpak.org/getting.html)

First, add the remote for the GNOME Runtime, if you don't have it:
```shell
flatpak remote-add --from gnome https://sdk.gnome.org/gnome.flatpakrepo
```

Then, create the repository:
```shell
flatpak remote-add --from baedert https://raw.githubusercontent.com/baedert/corebird-flatpak/master/baedert.flatpakrepo
```

or manually:
```shell
wget https://baedert.org/repo/baedert-repo.gpg
flatpak remote-add baedert --gpg-import=baedert-repo.gpg https://baedert.org/repo
```

Now you can install corebird from the repo:
```shell
# for the current stable version
flatpak install baedert org.baedert.corebird stable

# for the lastest unstable version
flatpak install baedert-repo org.baedert.corebird master
```

... and run it:
```shell
flatpak run org.baedert.corebird
```
