# flathub-deskvnc

Community-maintained Flatpak build manifest for DeskVNC, the native remote desktop client for VNC, RDP and SSH built on Rust and Tauri 2.

Upstream project: <https://github.com/psmux/DeskVNC>. This repository holds a copy of the Flatpak manifest so Linux users on Flatpak-capable distributions can install DeskVNC with one command.

## Install

After the manifest lands in a Flatpak remote, install DeskVNC with:

```sh
flatpak install --user --from https://raw.githubusercontent.com/deepaash/flathub-deskvnc/main/io.github.psmux.DeskVNC.flatpakref
# or, once the remote is added:
flatpak install io.github.psmux.DeskVNC
```

## What this manifest ships

`io.github.psmux.DeskVNC.yaml` pins version `0.27.11`, pointing at the real GitHub release tarball for v0.27.11. Every field is either from the upstream source tree, derived from the upstream CI build matrix, or marked as an assumption in a YAML comment.

The manifest uses the org.freedesktop.Platform 24.08 runtime with the rust-stable and node22 SDK extensions, finish-args for Wayland with an X11 fallback, plus IPC, network, xdg-config and home access required for VNC, RDP and SSH sessions and persistent configuration.

## Upstream source

DeskVNC is maintained at <https://github.com/psmux/DeskVNC>. File an issue in the upstream project for bugs in the application itself or for canonical build guidance. File an issue here only when this Flatpak manifest is wrong.
