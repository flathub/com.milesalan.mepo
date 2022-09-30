# Mepo Flatpak

Development via flatpak:

```sh
flatpak remote-add --user --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install flathub org.freedesktop.Platform//22.08 org.freedesktop.Sdk//22.08 runtime/org.freedesktop.Sdk.Extension.ziglang/x86_64/22.08
flatpak-builder build-dir com.milesalan.mepo.yml --force-clean
flatpak-builder --user --install --force-clean build-dir  com.milesalan.mepo.yml
flatpak run com.milesalan.mepo
```
