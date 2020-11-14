# Situation Awareness for macOS

#### Check what filesystem the disk uses
- `diskutil info /`
  - Look under **File System Personality.**

#### Check if _System Integrity Protection_ is enabled
- `csrutil status`

#### Find which shell you are using
- `echo $SHELL`

#### Check whether or not macOS command line tools are installed.
- source: [original](https://stackoverflow.com/questions/15371925/how-to-check-if-command-line-tools-is-installed), [archive](https://archive.is/4RMqO)
- `xcode-select -p`

---

## Learn about the device

### `system_profiler`

- `SPUSBDataType`
  - Identifies all connected USB drives.
  - Check if the disk is **writable.** (`Writable`)
  - Check the amount of **free space**. (`Available`)
  - Check the **file system** type. (`File System`)

- `SPDisplaysDataType`
  - All video output devices (e.g. monitors).
- `SPCameraDataType`
  - All video input devices (e.g. webcams).

---

#### Identifying devices on the network
- `arp -i en0 -l -a`

#### Locating interesting files
- `find`

#### Examine terminal history of the user
- source: [original](https://ss64.com/bash/history.html), [archive](https://archive.is/438Iu)
  - `history`
  - `history -c` (clear history)

## References
- StackExchange, **How to tell if I'm using HFS+ or APFS?** ([archive](https://archive.is/AIsir))

