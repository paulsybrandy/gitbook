# How to kill a task via terminal on Windows

### To obtain a list of all running processes and their PIDs in \[elevated] command prompt:

```
tasklist
```

### To obtain a list of all running processes and their PIDs in \[elevated] Powershell:

```
Get-Process

```

### To kill a task in \[elevated] command prompt:

```
taskkill /IM “ProcessName” /F
```

_(replace “ProcessName” with the name of the executable file of the process)_

### To kill a task in \[elevated] Powershell:

```
Stop-Process -Name “ProcessName” -Force
```

_(replace “ProcessName” with the name of the executable file of the process)_\
