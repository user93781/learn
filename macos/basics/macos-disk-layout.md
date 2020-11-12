# macOS Disk Layout

## Boot layout

### macOS 10.13 (High Sierra), macOS 10.14 (Mojave)

```
disk0
|
|-- disk0s1 (EFI partition)
|-- disk0s2 (APFS container)
    disk1
    |
    |-- disk1s1 (APFS volume)
    |   Startup Volume, often named "Macintosh HD"
    |-- disk1s2 (APFS volume)
    |   Preboot
    |   ~40-50 MB
    |-- disk1s3 (APFS volume)
    |   Recovery
    |   ~500 MB
    |-- disk1s4 (APFS volume)
        VM -> contains disk space used for storing virtual memory
        ~20 KB
```

### macOS 10.15 (Catalina)

```
disk0
|
|-- disk0s1 (EFI partition)
|-- disk0s2 (APFS container)
    disk1
    |
    |-- disk1s1 (APFS volume; read-only)
    |   **System Volume**, often named "Macintosh HD"
    |-- disk1s2 (APFS volume)
    |   **Data Volume**, often named "Macintosh HD - Data"
    |   Normally hidden from view at /System/Volumes
    |-- disk1s3 (APFS volume)
    |   Preboot
    |   ~40-50 MB
    |-- disk1s4 (APFS volume)
    |   Recovery
    |   ~500 MB
    |-- disk1s5 (APFS volume)
        VM -> contains disk space used for storing virtual memory
        ~20 KB
```

### macOS 11.0 (Big Sur)

```
disk0
|
|-- disk0s1 (EFI partition)
|-- disk0s2 (APFS container)
    disk1
    |
    |-- disk1s1 (APFS volume)
    |   |
    |   |--disk1s1s1 (Sealed System Volume, SSV)
    |      "Macintosh HD"
    |
    |-- disk1s2
    |   "Macintosh HD - Data"
    |
    |-- disk1s3
    |   Preboot
    |
    |-- disk1s4
    |   Recovery
    |
    |-- disk1s5
        VM
```

## Notes
- Note that the `/Applications` folder is actually a firmlink to the User's applications _blended with_ `/System/Applications`. They appear to be in one folder, but they are actually not.

## References

- The Eclectic Light Company, _macOS Boot Volume Layout._ ([original](https://eclecticlight.co/2020/09/16/boot-volume-layout/), [archive](https://archive.is/6rtLp))
