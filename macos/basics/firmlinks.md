# macOS Firmlinks

## What are firmlinks?

- macOS firmlinks are similar to traditional symlinks, but they
  - are only made between folders,
  - work in both directions,
  - effectively _merge the contents_ of the two linked folders.

## List of existing firmlinks

- This list is derived from `/usr/share/firmlinks`.
- To create your own firmlinks, read `man synthetic.conf`, and edit `/etc/synthetic.conf`.

```
/Applications <-> Applications
/Library <-> Library
/System/Library/Caches <-> System/Library/Caches
/System/Library/Assets <-> System/Library/Assets
/System/Library/PreinstalledAssets <-> System/Library/PreinstalledAssets
/System/Library/AssetsV2 <-> System/Library/AssetsV2
/System/Library/PreinstalledAssetsV2 <-> System/Library/PreinstalledAssetsV2
/System/Library/CoreServices/CoreTypes.bundle/Contents/Library <-> System/Library/CoreServices/CoreTypes.bundle/Contents/Library
/System/Library/Speech <-> System/Library/Speech
/Users <-> Users
/Volumes <-> Volumes
/cores <-> cores
/opt <-> opt
/private <-> private
/usr/local <-> usr/local
/usr/libexec/cups <-> usr/libexec/cups
/usr/share/snmp <-> usr/share/snmp
```

## References
- **Boot volume layout.** ([original](https://eclecticlight.co/2020/09/16/boot-volume-layout/), [archive](https://archive.is/6rtLp))
- **Working with APFS volume groups.** ([original](https://bombich.com/kb/ccc5/working-apfs-volume-groups), [archive](https://archive.is/jKbGy))
