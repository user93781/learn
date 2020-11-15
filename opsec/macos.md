# OPSEC Techniques

## Reset NVRAM/PRAM
- The NVRAM/PRAM stores the default values for many settings that need to be accessed quickly on a Mac.
  - Examples: sound volume, display resolution, startup-disk selection, time zone, recent kernel panic information.
- The NVRAM can store sensitive information.
- References
  - Apple Support, _Reset NVRAM/RAM on your Mac._ ([archive](https://archive.is/0d2Nx))
  - NVRAM can leak sensitive information. ([archive](https://archive.is/F1r6I))

## Reset SMC
- References
  - Apple Support, _Reset your SMC memory._ ([original](https://support.apple.com/en-us/HT201295), [archive](https://archive.is/bf63b))

## Enable strict hardware decryption
```bash
sudo pmset -a destroyfvkeyonstandby 1
sudo pmset -a hibernatemode 25
sudo pmset -a powernap 0
sudo pmset -a standby 0
sudo pmset -a standbydelay 0
sudo pmset -a autopoweroff 0
```

## Set a firmware password
```bash
sudo firmwarepasswd -setpasswd -setmode command
```

## Ask for a password immediately
```bash
defaults write com.apple.screensaver askForPassword -int 1
defaults write com.apple.screensaver askForPasswordDelay -int 0
```

## Ensure that the version of OpenSSL is the latest
```bash
openssl version
```

## Configure SSH
```
# ~/.ssh/config (perms: 600)
Host *
  PasswordAuthentication no
  ChallengeResponseAuthentication no
  HashKnownHosts yes
  UseKeyChain no
```

## Show all extensions

```bash
defaults write NSGlobalDomain AppleShowAllExtensions -bool true
```

## Disable Crash Reporter
```bash
defaults write com.apple.CrashReporter DialogType none
```

## Clear Crash Reporter Logs
- `$HOME/Library/Logs/CrashReporter`
- `/Library/Logs/CrashReporter`
- References
  - Acronis, _Where are macOS CrashReporter logs saved?_ ([archive](https://archive.is/yvomN))

- https://tristor.ro/blog/2016/03/23/setting-up-a-macbook-for-an-opsec-focused-developer-part-1/ (https://archive.is/PXkpt)
- https://tristor.ro/blog/2016/04/02/setting-up-a-macbook-for-an-opsec-focused-developer-part-2/ (https://archive.is/bp0L3)
