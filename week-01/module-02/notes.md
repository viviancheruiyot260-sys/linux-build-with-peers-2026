
# Module 2: Operating Systems

## 1. What is an Operating System?

An operating system is the main software that manages a computer's hardware and allows other applications to run.

It acts as a bridge between the user, applications, and hardware.

```text
User
↓
Applications
↓
Operating System
↓
Hardware
```

An operating system also manages things such as memory, processes, storage, and devices.

---

## 2. Choosing an Operating System

When choosing an operating system, we should consider:

* **Role** – Is the computer being used as a desktop or a server?
* **Function** – What will the computer be used for?
* **Life cycle** – How long will the OS be supported and updated?
* **Stability** – Is it stable enough for the intended work?
* **Compatibility** – Will the software and hardware work with it?
* **Cost** – What will licensing, maintenance, support, and upgrades cost?
* **Interface** – Will users mainly work through a GUI or command line?

The best operating system depends on the job and the user's needs.

---

## 3. Windows

Windows is developed by Microsoft and is widely used on desktop computers. Microsoft also provides Windows Server for server environments.

Windows mainly provides a graphical interface, but it also supports command-line tools such as PowerShell.

---

## 4. macOS

macOS is developed by Apple for Mac computers.

It has Unix/BSD foundations and provides both a graphical interface and command-line tools.

It is also popular among developers and creative professionals.

---

## 5. Linux

Linux is commonly used to refer to operating systems built around the Linux kernel.

The **Linux kernel** is the core part that manages system resources and communicates with hardware.

A complete Linux system is usually obtained through a **Linux distribution**.

Examples include:

* Ubuntu
* Debian
* Fedora
* Red Hat Enterprise Linux
* openSUSE
* Linux Mint

---

## 6. Linux Distributions

A Linux distribution combines the Linux kernel with other software needed to make a complete operating system.

```text
Linux Kernel
+
System Tools
+
Libraries
+
Package Manager
+
Applications
↓
Linux Distribution
```

Different distributions are designed for different purposes.

For example, some focus more on enterprise stability and long-term support, while others focus on newer software and faster updates.

### My Linux distribution

I checked my own system using:

```bash
cat /etc/os-release
```

My result showed that I am using **Ubuntu 24.04.3 LTS**.

It also showed:

```text
ID_LIKE=debian
```

This helped me confirm that Ubuntu is Debian-derived.

---

## 7. GUI and CLI

A **GUI (Graphical User Interface)** allows users to interact with a computer using windows, icons, menus, and buttons.

A **CLI (Command Line Interface)** allows users to interact with the system by typing commands.

Linux supports both GUI and CLI, but the CLI is especially important when working with Linux servers because servers are often managed remotely.

The command line is also useful for automation, cloud computing, and DevOps.

---

## 8. Terminal and Shell

The terminal provides a place where I can type commands.

The shell interprets the commands and the operating system carries out the requested action.

```text
User
↓
Terminal
↓
Shell
↓
Operating System
↓
Hardware
```

---

## 9. Embedded Systems

An embedded system is a computer system built into another device to perform a specific purpose.

Examples include:

* Smart TVs
* Routers
* Raspberry Pi devices
* Industrial equipment
* IoT devices
* Smart sensors

Linux can be customized for these devices because it is flexible and open source.

---

## Key Takeaways

* An operating system manages hardware and provides services for applications.
* Windows, macOS, and Linux are major desktop operating systems.
* Linux is built around the Linux kernel.
* Ubuntu is a Linux distribution, not the kernel itself.
* Linux distributions can be designed for different needs.
* GUI and CLI are different ways of interacting with an operating system.
* The command line is very important in Linux, cloud computing, and DevOps.
* Linux can also be used in embedded systems and IoT devices.
