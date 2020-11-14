# TCC (Transparency Consent and Control)

- Apps are identified by TCC using their **bundle identifier** (e.g.
  `com.company.Product`), but version numbers are not taken into account.
-  Because TCC only identifies via bundle identifier, an application that is
   uninstalled but _not removed from the TCC_ **still retains the TCC's
   permissions.** One can exploit this by creating an application with the same
   bundle identifier as an app in the TCC.

## `tccutil`

#### Resetting app permissions
- source: [original](https://apple.stackexchange.com/questions/342710/reset-all-mojave-app-permissions), [archive](https://archive.is/jCUAw)
- `tccutil reset All`
- `tccutil reset All com.apple.Terminal`

## TCC database location

- Root: `/Library/Application Support/com.apple.TCC/TCC.db`
- Users: `/Users/username/Library/Application Support/com.apple.TCC/TCC.db`

In order to read it, Terminal needs to have **Full Disk Access** permissions.

```bash
sudo sqlite3 /Library/Application\ Support/com.apple.TCC/TCC.db 'select * from access'
```

## References
- **A guide to Catalina's privacy protection, part 2: Controlling privacy settinsg.** ([original](https://eclecticlight.co/2020/01/15/a-guide-to-catalinas-privacy-protection-2-controlling-privacy-settings/), [archive](https://archive.is/32JzX))
- **macOS Catalina and `osquery`.** ([original](https://blog.kolide.com/macos-catalina-osquery-a6753dc3c35c), [archive](https://archive.is/I6cWN))
- **List apps authorized for full disk access.** ([archive](https://archive.is/buUPP))
- **Dropbox hack blocked by Apple in Sierra.** ([archive](https://archive.is/k1lJH))
