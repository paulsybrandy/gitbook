---
description: >-
  Two common ports that may experience this error include 3000 and 8081, but can
  be any port.
---

# Find and terminate a Windows Process by Port

### Find the Process ID (PID) <a href="#id-1---find-the-process-id-pid" id="id-1---find-the-process-id-pid"></a>

&#x20;For this, we can use `netstat -a -o -n` to list all active connections.

```
C:\Users\user> netstat -a -o -n

Active Connections

Proto  Local Address          Foreign Address        State           PID
...
TCP    [::]:8080              [::]:0                 LISTENING       3664
...
```

In the list that gets spat out, find the line that has a `Local Address` ending in the port you want to terminate - in this case we see`:8080`. Note the value in the `PID` column - we'll need that in a minute. **NOTE: This value will most likely be different each time you start your program.**

### Confirm that PID is for the program in question <a href="#id-2---confirm-that-pid-is-for-nodeexe" id="id-2---confirm-that-pid-is-for-nodeexe"></a>

> This step is optional, but I like to double check that I'm targeting the correct process before I terminate it.

To get a list of tasks running in `cmd` we can run `tasklist` which details everything actively running on your machine. See [how-to-kill-a-task-via-terminal-on-windows.md](how-to-kill-a-task-via-terminal-on-windows.md "mention")

```
C:\Users\user> tasklist

Image Name                     PID Session Name        Session#    Mem Usage
========================= ======== ================ =========== ============
...
node.exe                      6736 Services                   0      2,080 K
cmd.exe                       3048 Services                   0      2,268 K
node.exe                      3664 Services                   0      6,768 K
...

```

Here, you can see that there are multiple `node.exe` programs running, but only one of them has the PID`3664.`

### Stop the running process <a href="#id-3---stop-the-running-process" id="id-3---stop-the-running-process"></a>

Now that you know that it is`3664` PID, you can commence putting an end to our runaway process. The general format is `taskkill /f /pid ####`, replacing the #### with the PID from above. If you try to run this without the `/f` flag, you'll most likely be prompted to use the `/f Force flag` by Windows.

```
C:\Users\user> taskkill /f /pid 3664
SUCCESS: The process with PID 3664 has been terminated.
```

And now you're set to start your process again!

### Summary <a href="#summary" id="summary"></a>

* Find what Process ID (PID) is occupying the port in question with `netstat -a -o -n`
* (Optional) Confirm this PID is for the expected program with `tasklist`
* Terminate the process with `taskkill /f /pid ####` (replace #### with your PID)
