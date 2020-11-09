# `launchd`

## Agents vs. daemons

- **Agents.** runs tasks on behalf of the currently logged in user.
- **Daemons** runs tasks on behalf of `root` or another user.

## Job definitions

Job definitions are specified in XML files call **property lists.**

|Type|Location|
|:---|:-------|
|User Agents|`$HOME/Library/LaunchAgents`|
|Global Agents|`/Library/LaunchAgents`|
|Global Daemons|`/Library/LaunchDaemons`|
|System Agents|`/System/Library/LaunchAgents`|
|System Daemons|`/System/Library/LaunchDaemons`|


## References
- launchd.info ([original](https://www.launchd.info/), [archive]())