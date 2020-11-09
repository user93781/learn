# Situation Awareness for macOS

#### Check if _System Integrity Protection_ is enabled
- `csrutil status`

#### Find which shell you are using
- `echo $SHELL`

#### Check whether or not macOS command line tools are installed.
- source: [original](https://stackoverflow.com/questions/15371925/how-to-check-if-command-line-tools-is-installed), [archive](https://archive.is/4RMqO)
- `xcode-select -p`

#### Learn about the device
- `system_profiler`

#### Identifying devices on the network
- `arp -i en0 -l -a`

#### Locating interesting files
- `find`

#### Examine terminal history of the user
- `history`