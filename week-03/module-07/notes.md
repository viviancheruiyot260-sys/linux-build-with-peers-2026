
 Files and Directories


Linux uses a **hierarchical filesystem** that organizes files and directories under the root directory `/`.

Unlike Windows, Linux does not use drive letters such as `C:` or `D:`.

---

## 7.2 Directory Structure

The root directory is:

```bash
/
```

View its contents:

```bash
ls /
```

Common directories:

* `/home` — user home directories
* `/etc` — configuration files
* `/var` — logs and changing data
* `/tmp` — temporary files
* `/usr` — programs and utilities
* `/boot` — boot files

### Home Directory

`~` represents the current user's home directory.

```bash
cd ~
```

---

## 7.3 Navigating Directories

### Check current location

```bash
pwd
```

### Move into a directory

```bash
cd Documents
```

### Move up one level

```bash
cd ..
```

### Go home

```bash
cd
```

### Path types

**Absolute path:** starts with `/`

```text
/home/user/Documents
```

**Relative path:** starts from your current location.

```text
Documents
```

### Useful shortcuts

| Symbol | Meaning           |
| ------ | ----------------- |
| `/`    | Root              |
| `~`    | Home              |
| `.`    | Current directory |
| `..`   | Parent directory  |

---

## 7.4 Listing Files

```bash
ls
```

Show hidden files:

```bash
ls -a
```

Show detailed information:

```bash
ls -l
```

Human-readable sizes:

```bash
ls -lh
```

Combine options:

```bash
ls -la
```

Sort by size:

```bash
ls -lS
```

Sort by modification time:

```bash
ls -lt
```

### File types in `ls -l`

```text
d = directory
- = regular file
l = symbolic link
```

---

## Key Takeaway

Module 7 is about **understanding where you are and navigating the Linux filesystem**.

```text
pwd → Where am I?
ls  → What is here?
cd  → Move around
ls -la → Inspect everything
```
