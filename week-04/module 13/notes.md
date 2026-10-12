 Processes, Memory, Logs, and Filesystem

Linux uses the **kernel** to manage hardware, memory, and running programs.

In this module, I learned how to view running processes, check memory usage, read system logs, and understand Linux directories.

## 2. Pseudo-filesystems

Pseudo-filesystems provide information about the system without storing everything as normal files on disk.

- `/proc` — information about processes and the kernel.
- `/dev` — device files.
- `/sys` — information about hardware and devices.

Useful commands:

```bash
ls /proc
cat /proc/meminfo
cat /proc/modules
```

- `ls /proc` lists system information.
- `cat /proc/meminfo` displays memory details.
- `cat /proc/modules` lists loaded kernel modules.

## 3. Processes

A **process** is a program that is currently running.

- **PID:** A process's identification number.
- **PPID:** The ID of its parent process.
- **Parent process:** Creates another process.
- **Child process:** Created by another process.

PID 1 is normally the first process started by the system. On Ubuntu, it is usually `systemd`.

Useful commands:

```bash
ps
ps aux
ps -ef
ps -p 1 -o pid,ppid,comm
pstree
```

- `ps` displays processes linked to the current terminal.
- `ps aux` lists many running processes.
- `ps -ef` displays processes in full format.
- `ps -p 1 -o pid,ppid,comm` checks process 1.
- `pstree` displays processes in a tree.

## 4. Monitoring processes with `top`

The `top` command displays running processes and system resource usage in real time.

```bash
top
```

Useful keys:

- `q` — quit.
- `h` — help.
- `k` — start the process-killing prompt.
- `r` — change a process's priority.

**Load average** shows the system's average workload over the last 1, 5, and 15 minutes.

Check it using:

```bash
uptime
cat /proc/loadavg
```

## 5. Memory management

Linux uses **RAM** to run programs and **swap** as disk-backed memory when needed. Swap is generally slower than RAM.

Check memory usage:

```bash
free -h
free -m
```

- `free -h` displays memory in readable units.
- `free -m` displays memory in mebibytes.

The `available` value estimates how much memory can be used by applications without significant swapping.

## 6. System logs

**Logs** record system events and help us find errors or troubleshoot problems.

Logs are commonly stored in `/var/log`.

View available logs:

```bash
ls /var/log
```

Read a log file:

```bash
less /var/log/syslog
```

Ubuntu may also use the systemd journal.

```bash
journalctl
journalctl -b
journalctl -b -p err
```

- `journalctl` displays journal entries.
- `journalctl -b` shows logs from the current boot.
- `journalctl -b -p err` shows error-level messages from the current boot.

Press `q` to exit `less`.

## 7. Kernel messages

Kernel messages provide information about hardware, drivers, and system events.

```bash
dmesg
dmesg | grep -i usb
journalctl -k
```

- `dmesg` displays kernel messages.
- `grep -i usb` searches for USB-related messages.
- `journalctl -k` displays kernel messages stored in the systemd journal.

## 8. Linux filesystem hierarchy

The **Filesystem Hierarchy Standard (FHS)** describes how files and directories are organized in Linux.

| Directory | Purpose |
|---|---|
| `/` | Main root directory. |
| `/bin` | Essential commands. |
| `/boot` | Files needed to boot Linux. |
| `/dev` | Device files. |
| `/etc` | System configuration files. |
| `/home` | Ordinary users' personal directories. |
| `/root` | Root administrator's home directory. |
| `/proc` | Process and kernel information. |
| `/sys` | Hardware and kernel information. |
| `/tmp` | Temporary files. |
| `/usr` | Applications, libraries, and documentation. |
| `/var` | Changing data, such as logs. |
| `/media` | Common location for removable media. |
| `/mnt` | Common temporary mount point. |
| `/opt` | Optional or third-party software. |

Explore these directories using:

```bash
ls /
ls /home
ls /etc
ls /var
```

On modern Ubuntu, directories such as `/bin` may point to locations inside `/usr`. This is normal.

## 9. Important directories and commands

- `/usr/bin` — many user commands.
- `/usr/share/doc` — software documentation.
- `/var/log` — system and application logs.
- `/var/cache` — cached data.
- `/var/lib` — application and service data.
- `/etc/hosts` — local hostname mappings.
- `/etc/passwd` — user account information.

The `PATH` variable tells the shell where to search for commands.

```bash
echo "$PATH"
command -v ls
```

Check disk space:

```bash
df -h
```

Check the size of the log directory:

```bash
sudo du -sh /var/log
```

## 10. Practical exercises

Run these commands on my Ubuntu system:

```bash
ps aux | head
top
free -h
uptime
journalctl -b -p err
ls /
df -h
```

These exercises help me practice checking processes, monitoring memory, viewing logs, exploring directories, and checking disk space.

## 11. Summary

In this module, I learned that:

- Processes are running programs, and each has a PID.
- `ps` and `top` help monitor processes.
- `free -h` checks memory usage.
- Logs help identify errors and troubleshoot problems.
- `dmesg` displays kernel messages.
- Linux directories have different purposes.
- `df -h` helps check available disk space.

