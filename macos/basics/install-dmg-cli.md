# Installing a `.dmg` from the command line

## Steps

#### 1. Mount the `.dmg`

```bash
sudo hdiutil attach <image>.dmg
```

#### 2. Install

```bash
sudo installer -package <package>.pkg -target /
```

The `target` parameter refers to the _disk_, not the location (the locations are dictated by the installer).

#### 3. Unmount the `.dmg`

```bash
sudo hdiutil detact /Volumes/<image>
```

## References
- StackExchange, "Is there a command to install a dmg?" ([original](https://apple.stackexchange.com/questions/73926/is-there-a-command-to-install-a-dmg), [archive](https://archive.is/UXFA9))
- StackOverflow, "What does the target parameter mean in OSX installer?" ([original](https://stackoverflow.com/questions/45992256/what-is-the-target-parameter-mean-in-osx-installer), [archive](https://archive.is/OEaAN))