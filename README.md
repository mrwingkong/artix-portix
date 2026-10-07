# artix-portix

Optional **Porteus-style `.xzm` modules** and a small **`pman`** helper for Artix OpenRC. Keep the base system clean; add/remove apps as modules.

**Status:** personal workflow / proof-of-concept (~90% complete).

Related projects:

| Repo | What it is |
|------|------------|
| [artix-base-install](https://github.com/mrwingkong/artix-base-install) | Disk, base system, desktop, audio, portable USB/NVMe notes |
| [artix-post-install](https://github.com/mrwingkong/artix-post-install) | Optional desktop polish + ThinkPad / your hardware |
| **This one** — [artix-portix](https://github.com/mrwingkong/artix-portix) | Optional Porteus-style `.xzm` modules and `pman` |

## Who is this for?

Anyone who finished a working Artix OpenRC desktop (from **[artix-base-install](https://github.com/mrwingkong/artix-base-install)**) and wants modular apps.

## Before you start

- Finish the base install (and optionally **[artix-post-install](https://github.com/mrwingkong/artix-post-install)**).
- You need packages like `squashfs-tools` and `libarchive` — see [`packages.md`](packages.md).

## Get the files

```bash
cd ~
git clone https://github.com/mrwingkong/artix-portix.git
```

**What this does:** puts the module tools in `~/artix-portix`.

## Quick path

1. Finish the base desktop first.
2. Run the all-in-one setup script: [`aio-setup.sh`](aio-setup.sh) (detects your user with `whoami` — no hardcoded names).
3. Read details in [`how-it-works.md`](how-it-works.md).

```bash
bash ~/artix-portix/aio-setup.sh
```

**What this does:** Installs `build-xzm.sh`, `pman`, an OpenRC `module-mounts` service for *your* home directory, and an icon-refresh autostart helper.

Then:

```bash
pman install featherpad
```

**What this does:** Builds/mounts a module and creates a menu entry (example package).

```bash
pman remove featherpad
```

**What this does:** Removes that module and launchers.

## Credits

This repo is inspired by the hard work of these projects. Thank you!

- **[Porteus Linux](https://porteus.org/)**: the portable, modular Linux behind `.xzm` modules. Started by **Fanthom**, with the [Porteus team](https://www.porteus.org/contact-team.html) including **brokenman (Jay Flood)**, **Hamza** and **Tomasz Jokiel**.
- **[Nemesis Linux](https://sourceforge.net/projects/nemesis-linux/)**: Porteus-style modules on an Artix/OpenRC base. Its community uses a `pman` tool for building modules. See the [Nemesis forum](https://forum.porteus.org/viewforum.php?f=137).
- **[Slax](https://www.slax.org/)** by **Tomáš Matějíček**: the modular "pocket" Linux that Porteus grew from.

> ℹ️ The `pman` made by [`aio-setup.sh`](aio-setup.sh) is a small helper written for this repo. It borrows the idea and name but is **not** the Nemesis `pman`.

## Licence

[GPL-3.0](LICENSE)
