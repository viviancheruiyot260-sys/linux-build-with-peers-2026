
 Computer Hardware

## 12.1 Introduction
Computer hardware refers to the physical parts of a computer, such as the CPU, RAM, motherboard, and storage devices. Understanding hardware helps with system installation, configuration, and troubleshooting. Computers can be physical or virtual machines.

## 12.2 Motherboards
The motherboard is the main circuit board that connects computer components, including the CPU, RAM, storage, and peripherals. Buses provide communication pathways between components.

## 12.3 Processors
The **CPU (Central Processing Unit)** executes instructions and performs calculations.

- **Multi-core:** One processor with multiple cores.
- **Multiprocessor:** A system with multiple physical processors.
- **x86:** 32-bit architecture.
- **x86_64:** 64-bit architecture, generally supporting more memory.

Commands:
- `arch` — displays the system architecture.
- `lscpu` — displays CPU information.

## 12.4 RAM
**RAM (Random Access Memory)** temporarily stores data used by running programs. It is volatile, meaning its contents are lost when power is switched off.

**Swap** is disk space Linux can use when RAM is insufficient. It is slower than RAM.

Commands:
- `free -h` — displays memory usage in readable units.
- `free -m` — displays memory usage in megabytes.

## 12.5 Buses and Peripherals
Buses allow components to communicate.

- **PCI:** Connects internal expansion devices.
- **USB:** Connects external devices such as keyboards and flash drives.
- **Input devices:** Keyboard and mouse.
- **Output devices:** Monitor and printer.
- **Storage devices:** External hard drives and flash drives.

Commands:
- `lspci` — lists PCI devices.
- `lsusb` — lists USB devices.

Hot-plug devices can be connected or disconnected while the computer is running. Safely eject or unmount storage devices before removal.

## 12.6 Hard Drives
Hard drives and other storage devices store the operating system, applications, and files permanently.

A **partition** is a logical section of a storage device.

- **MBR:** An older partitioning scheme.
- **GPT:** A newer partitioning scheme that supports larger disks and more partitions.

Linux represents storage devices as files under `/dev`, such as `/dev/sda` and `/dev/sda1`.

Commands:
- `lsblk` — lists storage devices and partitions.
- `sudo fdisk -l` — displays disk and partition information.

Inspect disks carefully. Changing partitions can cause data loss.

## 12.7 Solid-State Drives (SSDs)
SSDs use flash memory and have no moving parts. Compared with traditional hard disk drives (HDDs), they are generally faster, quieter, and more energy-efficient, but can cost more per gigabyte.

Command:
- `lsblk -o NAME,SIZE,TYPE,ROTA,MODEL` — displays storage details. `ROTA` is usually `0` for SSDs and `1` for rotational HDDs.

## 12.8 Optical Drives
Optical drives use lasers to read or write CDs, DVDs, and Blu-ray discs.

- **CD-R/DVD-R:** Generally recordable once.
- **DVD-RW:** Rewritable.

Linux commonly accesses removable media through directories under `/media` or `/mnt`. Mounting makes a filesystem accessible; unmounting safely detaches it.

## 12.9 Managing Devices
Linux uses device drivers to communicate with hardware. Drivers may be built into the kernel, loaded as kernel modules, or supplied by vendors.

Commands:
- `lspci` — lists PCI devices.
- `lsusb` — lists USB devices.

These commands identify devices but do not necessarily confirm that every device is working correctly. Check Linux compatibility when choosing hardware.

## 12.10 Video Display Devices
Graphics hardware processes visual output for the monitor. It may be integrated into the computer or provided by a separate graphics card.

Graphics drivers allow Linux to communicate with graphics hardware.

Common display connections:
- **VGA:** Older analog connection.
- **DVI:** Primarily digital, with some types supporting analog.
- **HDMI:** Carries digital video and audio.
- **DisplayPort:** Digital display connection; Mini DisplayPort is a smaller version.

**Resolution** is the number of pixels displayed, for example, 1920 × 1080. The graphics hardware and monitor must support a compatible resolution.

## 12.11 Power Supplies
A power supply converts **AC (alternating current)** from the wall outlet into **DC (direct current)** used by computer components. It provides different voltage levels, such as 3.3V, 5V, and 12V.

A reliable power supply helps maintain system stability. A failing unit can cause shutdowns, instability, or hardware damage.

Desktop computers depend on continuous external power, while laptops can use their batteries during power interruptions. A dedicated surge protector or UPS provides additional protection against power problems.

inux and hardware.
- Safe disk management and reliable power are important for protecting computer systems.
