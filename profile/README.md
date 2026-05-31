# Kira Linux

> *A Linux distribution you actually understand.*

Kira Linux is a rolling-release, developer-oriented Linux distribution built for people who want full control over their system, without sacrificing usability. It is lean by design, transparent by default, and built to be understood and modified by its users.

**Kira is not a distro you install and forget. It is a distro you own.**

---

## What makes Kira different

- **Shinigami kernel** : a stripped and patched Linux fork, built for responsiveness and minimal overhead. No bloat, no legacy driver noise.
- **flux** : a custom package manager written in C, that compiles packages from source with per-package optimization flags and caches the result. Dependency-minimal by design.
- **kotodama recipes** : the package recipe format for flux. Simple, readable, contributor-friendly.
- **musl libc** : smaller binaries, cleaner static linking, lower memory footprint.
- **runit** : no systemd. Ever. Fast boot, transparent service management, dead simple to modify.
- **Wayland-first** : SwayFX as the primary desktop environment, Sleex as an officially supported alternative.
- **No telemetry. No user data collection. No accounts. No subscriptions.**

---

## Repositories

| Repo | Description |
|---|---|
| [`shinigami`](https://github.com/shinigami-os/shinigami) | Linux fork : Kira-specific patches and kernel config |
| [`kira-base`](https://github.com/shinigami-os/kira-base) | Base system : musl, runit, core userland, boot |
| [`flux`](https://github.com/shinigami-os/flux) | Package manager source code (C) |
| [`flux-recipes`](https://github.com/shinigami-os/flux-recipes) | kotodama package recipes |
| [`flux-cache`](https://github.com/shinigami-os/flux-cache) | Binary cache server |
| [`kira-desktop`](https://github.com/shinigami-os/kira-desktop) | SwayFX config, Waybar, theming, desktop defaults |
| [`kira-installer`](https://github.com/shinigami-os/kira-installer) | Installer and ISO build scripts |
| [`kira-docs`](https://github.com/shinigami-os/kira-docs) | Documentation (coming soon) |

---

## Roadmap

### Phase 0 — Foundation `DONE`
- GitHub org and all repos initialized
- Shinigami: Linux forked, patch infrastructure in place, boots in QEMU
- flux: project scaffolding and CLI skeleton in C
- kira-base: musl + BusyBox + runit booting a minimal interactive system in QEMU

### Phase 1 — Bootable Base `DONE`
- Shinigami: BORE scheduler applied, Clang ThinLTO build, boots on real hardware
- kira-base: eudev, dhcpcd, LibreSSL, OpenSSH compiled from source against musl, SSH confirmed working
- kira-base: ZSH as default shell with Powerlevel10k, autosuggestions, syntax highlighting
- flux: `install`, `remove`, `search`, `update` fully working against a local recipe repo
- flux: binary cache working
- First 20 kotodama recipes: essential developer tools
- `kira-base.iso` builds and installs successfully

### Phase 2 — Desktop `IN PROGRESS`
- SwayFX + Waybar + Wofi + Flameshot on Wayland
- Sleex as an officially supported alternative DE
- Firefox recipe, Flatpak support, VS Code and Steam confirmed working
- `kira-desktop.iso`
- Kira Linux website
- Kira Linux discord server

### Phase 3 — Ecosystem
- flux compat layer (Debian container fallback via bubblewrap)
- 100+ kotodama recipes
- PGO support for key packages (Firefox, LLVM)
- Kira docs site live
- Monthly ISO snapshots automated via CI

### Phase 4 — Polish and Self-Hosting
- Migrate to self-hosted Gitea (GitHub remains as mirror)
- Self-hosted binary cache and CI/CD
- RISC-V architecture support begins

---

## Documentation

Full documentation is coming. It will live at the Kira Linux website, built from markdown sources in [`kira-docs`](https://github.com/shinigami-os/kira-docs).

---

## License

- **Shinigami**: GPL-2.0 (inherits Linux kernel license)
- **All other components**: MIT unless otherwise stated in the repository

---

## Author

Built by [OxoGhost](https://github.com/OxoGhost01).

## Contact

*Discord server comming soon!*
*Website comming soon!*
