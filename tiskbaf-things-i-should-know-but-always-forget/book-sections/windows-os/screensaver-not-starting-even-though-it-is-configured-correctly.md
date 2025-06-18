# Screensaver not starting even though it is configured correctly

### Use command prompt in admin mode to utilize the following commands

To see what processes, services, and drivers may be conflicting with the screensaver from activating:

```
powercfg -requests
```

To override and stop any process, service, or driver from conflicting with the screensaver from activating:

```
powercfg -requestsoverride <name> <type>
```

Complete description and parameter list can be seen by using the following command in command prompt:`powerconfig /?` or `powerconfig /? <command>`
