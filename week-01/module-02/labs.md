# Module 2: Hands-on Lab

## Lab: Exploring My Linux System

For this lab, I used the terminal on my Ubuntu computer to identify my Linux distribution, check the Linux kernel, and view basic system information.

### 1. Identify the Linux Distribution

**Command:**

```bash
cat /etc/os-release
```

**What it does:**

This command displays information about the Linux distribution installed on the computer.

**What I found:**

My system is running **Ubuntu 24.04.3 LTS (Noble Numbat)**.

The output also showed:

```text
ID=ubuntu
ID_LIKE=debian
```

This confirms that I am using Ubuntu and that Ubuntu is Debian-derived.

---

### 2. Check the Linux Kernel

**Command:**

```bash
uname -r
```

**What it does:**

This command displays the version of the Linux kernel currently running on the computer.

**My result:**

```text
6.17.0-14-generic
```

**What I learned:**

This helped me understand the difference between the Linux distribution and the Linux kernel. My distribution is **Ubuntu 24.04.3 LTS**, while the kernel currently running on my system is **Linux 6.17.0-14-generic**.

---

### 3. View System Information

**Command:**

```bash
hostnamectl
```

**What it does:**

This command displays general information about the computer, including the operating system, kernel, architecture, and hardware.

**Some of my results:**

```text
Operating System: Ubuntu 24.04.3 LTS
Kernel: Linux 6.17.0-14-generic
Architecture: x86-64
Hardware Vendor: HP
Hardware Model: HP EliteBook 820 G3
```

**What I learned:**

I learned that `hostnamectl` can give me a quick overview of my Linux system from the terminal.

---

## Screenshot Evidence

I captured the three commands and their outputs in one screenshot.

![Module 2 Linux System Information](screenshots/module-02-linux-system-info.png)

## Lab Takeaway

This hands-on practice helped me connect the theory from Module 2 with the Linux system I actually use.

I was able to identify my Ubuntu distribution, find the Linux kernel version, and view information about my computer using the command line.

The main thing I learned is that **Ubuntu and the Linux kernel are not the same thing**. Ubuntu is my Linux distribution, while the Linux kernel is the core of the system running underneath it.

