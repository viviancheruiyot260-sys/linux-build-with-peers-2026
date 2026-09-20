
# Module 3: Working in Linux

## 3.1 Navigating the Linux Desktop

Linux can be used through:

* **GUI (Graphical User Interface):** Using windows, icons, menus and settings.
* **CLI (Command Line Interface):** Typing commands in the terminal.

The terminal is especially important for system administrators because many Linux servers are managed without a GUI.

## 3.2 Applications

The **kernel** is the core of Linux. It manages resources such as CPU, memory and storage and allows applications to use them.

A **process** is a running task or program managed by the kernel.

Linux applications can be used for different purposes:

* **Server applications** — provide services to other computers.
* **Desktop applications** — programs users interact with directly.
* **Tools** — help users manage or develop software.

Examples include:

* Apache / NGINX → Web servers
* MariaDB / PostgreSQL → Databases
* Samba / NFS → File sharing
* LibreOffice → Productivity
* Firefox → Web browsing

## 3.3 Console Tools

A **shell** allows me to communicate with Linux by typing commands.

**Bash** is one of the most common Linux shells.

Text editors are also important because administrators often need to edit configuration files.

Examples:

* `nano` → simple and beginner-friendly
* `vim` → powerful but has a steeper learning curve

## 3.4 Package Management

A **package manager** helps install, update and remove software.

Since I am using Ubuntu, I mainly work with the Debian package system.

Common commands include:

```bash
sudo apt update
sudo apt install package-name
sudo apt remove package-name

A package may depend on other packages, so the package manager helps handle these dependencies.

## 3.5 Development Languages

Linux supports many programming languages.

* **C** → used to build much of the Linux kernel
* **JavaScript** → commonly used for web development
* **PHP** → used for dynamic websites
* **Python** → useful for scripting, automation and development
* **Ruby / Perl** → also used for scripting and automation

I also learned the difference between:

* **Compiled languages** → code is translated before running.
* **Interpreted languages** → code is generally processed while running.

## 3.6 Security

Linux security involves controlling who can access systems and what they can do.

Important concepts include:

* **Root** → the most privileged user.
* **Passwords** → should be strong and unique.
* **Firewall** → controls network traffic.
* **Updates** → help fix security vulnerabilities.
* **2FA** → adds another layer of login protection.

Privacy also matters. Cookies and tracking technologies can collect information about browsing activity.


## 3.7 Cloud Computing

Cloud computing means using computing resources hosted remotely and accessed through a network.

The four main deployment models are:

* **Public cloud** → shared provider infrastructure.
* **Private cloud** → dedicated to one organization.
* **Community cloud** → shared by organizations with common needs.
* **Hybrid cloud** → combination of different cloud environments.

### Linux in the Cloud

Linux is widely used in cloud environments because it is:

* Flexible
* Cost-effective
* Easy to automate
* Scalable
* Well supported for server workloads


## Virtualization and Containers

**Virtualization** allows one physical computer (**host**) to run multiple virtual machines (**guests**).

A **hypervisor** manages these virtual machines.

**Containers** are a lighter way of running applications with their required dependencies.

Technologies such as **Docker** and **Kubernetes** are commonly used with containers.

