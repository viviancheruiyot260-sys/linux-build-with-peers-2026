 Where Data Is Stored-lab

## 1. Exploring `/proc`

| Command | What it does |
|---|---|
| `ls /proc` | Lists process and kernel information. |
| `cat /proc/1/cmdline; echo` | Displays the command used to start process 1. |
| `ps -p 1` | Displays information about process 1. |
| `cat /proc/cmdline` | Shows kernel boot parameters. |

## 2. Managing Processes

| Command | What it does |
|---|---|
| `ping localhost > /dev/null` | Runs ping in the foreground and hides its output. |
| `ping localhost > /dev/null &` | Runs ping in the background. |
| `jobs -l` | Lists background jobs and their PIDs. |
| `fg %1` | Brings job 1 to the foreground. |
| `Ctrl+Z` | Suspends the foreground job. |
| `bg %1` | Resumes suspended job 1 in the background. |
| `kill %1` | Sends a termination signal to job 1. |

## 3. Monitoring and Stopping Processes

| Command | What it does |
|---|---|
| `top` | Monitors running processes and system resources. |
| `sleep 888888 &` | Starts a long-running sleep process in the background. |
| `kill PID` | Sends a termination signal to the process with that PID. |

Replace `PID` with the actual process ID displayed in your terminal. Press `q` to exit `top`.

## 4. Viewing System Logs

| Command | What it does |
|---|---|
| `ls /var/log` | Lists available system log files. |
| `tail -5 /var/log/auth.log` | Displays the last five authentication log lines, if the file exists. |
| `journalctl -n 10` | Displays the latest ten system journal entries. |
| `sudo journalctl -u ssh -n 10` | Displays recent SSH service logs, if available. |



**Note:** Capture your actual terminal output. Stop all test processes when finished. Job numbers and PIDs may differ from the course examples.

