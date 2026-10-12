# Module 13: Where Data Is Stored

In this lab, I learned how to explore system information, manage running processes, monitor system activity, and view system logs in Linux.

## 1. Exploring `/proc`

| Command | What it does |
|---|---|
| `ls /proc` | Lists files and folders containing system information. |
| `cat /proc/1/cmdline; echo` | Shows the command used to start process 1. |
| `ps -p 1` | Displays information about process 1. |
| `cat /proc/cmdline` | Shows the options used when starting Linux. |

## 2. Managing Processes

| Command | What it does |
|---|---|
| `ping localhost > /dev/null` | Tests the local network connection without displaying the results. |
| `ping localhost > /dev/null &` | Runs the ping command in the background. |
| `jobs -l` | Lists background jobs and their process IDs. |
| `fg %1` | Brings job 1 to the foreground. |
| `Ctrl + Z` | Temporarily pauses a running command. |
| `bg %1` | Resumes a paused job in the background. |
| `kill %1` | Stops job 1. |

## 3. Monitoring and Stopping Processes

| Command | What it does |
|---|---|
| `top` | Displays running processes and their CPU and memory usage. |
| `sleep 888888 &` | Starts a waiting process in the background. |
| `kill PID` | Stops a process using its process ID. |

*Note: Replace `PID` with the actual process ID. Press `q` to exit `top`.*

## 4. Viewing System Logs

| Command | What it does |
|---|---|
| `ls /var/log` | Lists available system log files. |
| `tail -5 /var/log/auth.log` | Shows the last five authentication log entries, if the file exists. |
| `journalctl -n 10` | Displays the ten latest system log entries. |
| `sudo journalctl -u ssh -n 10` | Displays recent SSH service logs, if available. |
