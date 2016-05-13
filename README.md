## Inspect OSX Startup Items

There are so many places on OS X that spawns or executes applications at startup and that is pretty confusing and waste developers lots of time to find what they need. Some are exposed, some are hidden and less known.

This repo aims to list all possible locations to find the `plist` or configuration that makes applications running at startup (or user login).

### Listing

**1. Startup Applications**

```
/Library/StartupItems
/System/Library/StartupItems/
```

**2. Startup Daemons**

```
/Library/LaunchDaemons
/System/Library/LaunchDaemons
```

**3. User Login**

```
~/Library/LaunchAgents
/Library/LaunchAgents
/System/Library/LaunchAgents
```

**4. Startup Applications or Scripts Hooked via Login/Logout**

```
$ defaults read com.apple.loginwindow LoginHook

$ defaults read com.apple.loginwindow LogoutHook
```

**5. Crontab**

```
$ crontab -l
```

**6. Extensions boot with Kernel**

*You won't need to check this anyway.*

```
$ kextstat
```

### Notes

If you have anything, feel free to share!
