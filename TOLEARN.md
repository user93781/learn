## Basic Skills

### Bash
- https://linuxcommandlibrary.com/basic/oneliners.html

### Python
- `os`
- `socket`
  - https://docs.python.org/3/library/socket.html
  - `SOCK_STREAM`: TCP
  - `SOCK_DGRAM`: UDP
- `subprocess`

## Malware
- Chill Tab macOS malware
- Custom URL schemes
  - https://objective-see.com/blog/blog_0x38.html

## macOS
- `codesign`
- `spctl`
- `fs_usage`
- Info.plist
- `clamav`
  - `siptool`, part of ClamAV, Can be used to extract embedded macros
- `ProcInfo` by Objective See
- Microsoft Word
  - Sandbox escape: `dlopen()`
- macOS Sandboxes, Entitlements
- XProtect
- Malware Removal Tool (MRT)
  - https://krypted.com/mac-os-x/using-apples-built-malware-removal-tool-mrt/
- Frameworks
  - Core Services
    - Launch Services Keys
  - Mach Services
    - https://developer.apple.com/library/archive/documentation/Darwin/Conceptual/KernelProgramming/Mach/Mach.html
- Entitlements
  - https://developer.apple.com/library/archive/documentation/Miscellaneous/Reference/EntitlementKeyReference/Chapters/AppSandboxTemporaryExceptionEntitlements.html
- Launchd Jobs
  - https://developer.apple.com/library/archive/documentation/MacOSX/Conceptual/BPSystemStartup/Chapters/CreatingLaunchdJobs.html
- Debugging on macOS
  - https://bryce.is/writing/code/macosx/debugging/udp/sockets/dtruss/dtrace/eaddrinuse/2016/07/30/debugging-using-system-calls.html
  - `dtrace`
- Webcam
  - [ ] MacBook Webcam Teardown: https://archive.is/OSnWT

### macOS Persistence techniques
- `cron`
- `dylib` hijack
- `launchd`
- Login hook

## Malware
- Ring -3 rootkit, Intel Active Management Technology (AMT)

## Exploit development
- 

## Hardware
- DataMatrix Codes
  - https://en.wikipedia.org/wiki/Data_Matrix
- Hot air pencil
- PCIe
  - For MacBook cameras?
- Optics
  - Fixed-focus optics
- EEPROM
- I2C
- Laptop hardware
  - IPMI
  - Baseboard Management Interface

## Blue team
- https://github.com/user93781/awesome-cybersecurity-blueteam
- NetFlow
