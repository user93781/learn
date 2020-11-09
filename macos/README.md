## Persistence

- macOS cron job locations
  - source: [archive](https://archive.is/9A2LO)
  - `/var/at/tabs/` (perms: 700 root wheel)


## Credentials

- Google Chrome Passwords
  - source: [original](https://apple.stackexchange.com/questions/339281/where-does-chrome-store-login-credentials-in-macos), [archive](https://archive.is/wgYXF)
  - `$HOME/Library/Application Supoprt/`
- Keyloggers
  - [Keystroke Receiving - Why are apps asking for this?](https://discussions.apple.com/thread/250720391) ([archive](https://archive.is/5vlAt))

## Evading detection

#### Resetting app permissions
- source: [original](https://apple.stackexchange.com/questions/342710/reset-all-mojave-app-permissions), [archive](https://archive.is/jCUAw)
- `tccutil reset All`
- `tccutil reset All com.apple.Terminal`

#### "Terminal would like to administer your computer."
- source: [original](https://apple.stackexchange.com/questions/360521/how-to-turn-off-terminal-would-like-to-administer-your-computer-message), [archive](https://archive.is/b8UmX)

#### Deleting command history
- source: [original](https://ss64.com/bash/history.html), [archive](https://archive.is/438Iu)
- `history -c`


#### "The 'xyz' command requires the command line developer tools. Would you like to install the tools now?"
- Commands
  - `python3`
  - `pip3`

## Mitigations
- ReiKey (https://objective-see.com/products/reikey.html)
