# Corebird Flatpak

This is a `flatpak-builder` definition file to build both corebird master and current stable branches.

The built app can be found at https://baedert.org/repo which is a flatpak repository.


Install it:

```
wget https://baedert.org/repo/baedert-repo.gpg
flatpak --user remote-add baedert-repo --gpg-import=baedert-repo.gpg https://baedert.org/repo

# for the current stable version
flatpak --user install baedert-repo org.baedert.corebird stable

# for the lastest unstable version
flaptak --user install baedert-repo org.baedert.corebird master

# Run it
flatpak run org.baedert.corebird
```
