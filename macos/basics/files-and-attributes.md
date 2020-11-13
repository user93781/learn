# Files: data, attributes, and extended attributes (APFS)

## Introduction

- In modern systems, Files consist of three types of data, often stored separately:
  1. **data** (a.k.a. the data fork)
    - the data that is read and written by applications.
  2. **attributes**
    - the metadata about the file: name, date of creation, permissions, etc.
  3. **extended attributes**
    - supplementary info about the data, richer than the attributes.

## Structure and data forks

### Sparse files
- Some files on macOS are automatically determined to be sparse files.

### Clones
- APFS introduced clones as a way to save disk space.
- Many applications don't utliize clones, however.
- Can create a clone via `cp -c <src> <dest (i.e. the clone)>`

### Compression
- APFS performs file compression transparently.

## Attributes

- `inode`.
  - The most fundamental attribute, particularly for local storage.
  - It is a _unique value_ within the file system volume.
  - `inodes` are used in two ways
    - `volfs` path. `/.vol/<volume number>/<inode>`
    - File Reference URL. `file:///.file/id=<different volume number>.<inode>`
  - Find a file's `inode` with `ls -i` or `stat`.
  - In `stat`, the first number is the **volume** `inode`, and the second
    number is the file `inode`.
- Name.
  - Three characteristics of HFS+ and APFS:
    - Unicode normalization
    - Case insensitive
    - Case preserving
- Dates.
  - Date of last modification of the data fork.
  - Date of last modification of the attributes.
- UNIX/Posix Permissions.
- Uniform type identifier (UTI).
  - UTIs are now determined largely by other attributes.
- Specialized attributes.
  - Attributes for different file systems, e.g. those for cloud services.

## Extended Attributes (`xattrs`)

- `ls -la` that has `@` signifies that extended attributes are present on the file.
- `xattr -l <file>` can be used to show the extended attributes.
- `com.apple.rootless` marks an item protected by SIP.
- `com.apple.ResourceFork.`
- Metadata subtypes (termed "attributes" by Apple)
  - `_kMDItemUserTags`. Finder tag information.
  - `kMDItemIsScreenCapture`.

## References

- **There's more to files than data: structure and data forks.** ([archive](https://archive.is/dGXbK))
- **There's more to files than data: attributes.** ([archive](https://archive.is/OQJ64))
- **There's more to files than data: extended attributes.** ([archive](https://archive.is/QV38s))


