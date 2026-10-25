Module 17: Lab — File Ownership and Permissions

## Objective

Practice viewing file permissions, modifying permissions with `chmod`, and changing file ownership using `chown` and `chgrp`.

## 1. Create Files and Directories

```bash
cd /tmp
mkdir -p priv-dir pub-dir
touch priv-dir/priv-file pub-dir/pub-file
```

**What I learned:** `mkdir` creates directories, while `touch` creates empty files.

## 2. View Permissions and Ownership

```bash
ls -l priv-dir
ls -l pub-dir
ls -la
```

**What I learned:** `ls -l` displays permissions and ownership. `ls -la` also displays hidden files and directories.

## 3. Add Write Permission for Others

```bash
ls -ld pub-dir
chmod o+w pub-dir
ls -ld pub-dir
```

**What I learned:** `chmod o+w` adds write permission for others.

## 4. Remove Group and Others' Permissions

```bash
ls -l priv-dir/priv-file
chmod g-rw,o-r priv-dir/priv-file
ls -l priv-dir/priv-file
```

**What I learned:** Symbolic `chmod` notation allows specific permissions to be added or removed.

Expected permissions: `-rw-------`

## 5. Create and Execute a Shell Script

```bash
cd /tmp
echo "date" > test.sh
./test.sh
ls -l test.sh
```

The first execution should fail because the file does not yet have execute permission.

Add execute permission and run it:

```bash
chmod u+x test.sh
ls -l test.sh
./test.sh
```

**What I learned:** A file needs execute permission to be run directly as a program.

## 6. View Numeric Permissions

```bash
stat test.sh
```

The `stat` command displays detailed file information, including numeric permissions, user ID, and group ID.

## 7. Change Permissions Using Numeric Notation

```bash
chmod 775 test.sh
ls -l test.sh
stat test.sh
```

**What I learned:** Numeric permissions use `4` for read, `2` for write, and `1` for execute. The value `775` gives the owner and group full permissions and gives others read and execute permissions.

## 8. Change Ownership

The course lab uses a root account to demonstrate ownership changes.

```bash
chown bin pub-dir/pub-file
ls -l pub-dir/pub-file
```

**What I learned:** `chown` changes the user owner of a file and normally requires administrator privileges.

## 9. Change Group Ownership Recursively

```bash
chgrp -R users priv-dir
ls -ld priv-dir
ls -l priv-dir/priv-file
```

**What I learned:** `chgrp` changes group ownership, while `-R` applies the change recursively to a directory and its contents.

**Note:** The `chown` and `chgrp` commands above reflect the Cisco lab environment. On a personal Ubuntu computer, first verify that the specified users and groups exist. Use `sudo` when administrator privileges are required, and never change ownership of system files for practice.

## Key Takeaways

- `ls -l` and `stat` help inspect permissions and ownership.
- `chmod` modifies file and directory permissions.
- Symbolic notation uses letters and operators; numeric notation uses values from `0` to `7`.
- `chown` changes user ownership, while `chgrp` changes group ownership.
- Directory permissions affect access to the files inside them.

