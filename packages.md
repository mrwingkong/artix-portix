# Packages — artix-portix (modules)

Only packages used for building and mounting **`.xzm`** modules.  
Base system: **[artix-base-install](https://github.com/mrwingkong/artix-base-install)**.  
Desktop polish / hardware: **[artix-post-install](https://github.com/mrwingkong/artix-post-install)**.

| Package | What it is | Why needed | Required? |
|---------|------------|------------|-----------|
| `squashfs-tools` | squashfs tools | Build `.xzm` modules | required for modules |
| `libarchive` | Archive library (`bsdtar`) | Pack module contents | required for modules |
| `zip` / `unzip` / `xz` | Archive tools | Pack and unpack | optional |
| `gtk-update-icon-cache` | Icon cache tool | Refresh icons after modules | optional |
