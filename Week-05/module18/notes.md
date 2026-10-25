 Module 18: Special Permissions and Links

## 1. Introduction

Linux has three special permissions that help manage security and shared access:

- **setuid** — runs an executable with the file owner's permissions.
- **setgid** — runs an executable with the file group's permissions or makes files inherit a directory's group.
- **Sticky bit** — protects files in shared directories from being deleted or renamed by other users.

## 2. setuid

The setuid permission allows an executable to run with the permissions of its owner rather than the user running it.

Example: The `passwd` command can update password information in `/etc/shadow`, which ordinary users cannot access directly.

### Commands

```bash
ls -l /usr/bin/passwd
chmod u+s file
chmod 4775 file
chmod u-s file
chmod 0775 file
```

- `s` in the owner's execute position indicates setuid and execute permission are set.
- `S` indicates setuid is set, but owner execute permission is not.
- Numeric value: **4000**.

**Important:** Only set setuid on trusted executables when necessary. Do not experiment with it on system programs.

## 3. setgid

The setgid permission behaves differently depending on whether it is set on a file or directory.

- **On an executable file:** The program runs with the file's group permissions.
- **On a directory:** Newly created files inherit the directory's group ownership. New subdirectories also inherit the setgid permission.

This is useful when several users need to work together in a shared directory.

### Commands

```bash
chmod g+s directory
chmod 2775 directory
chmod g-s directory
chmod 0775 directory
ls -ld directory
```

- `s` in the group's execute position indicates setgid and group execute permission are set.
- `S` indicates setgid is set, but group execute permission is not.
- Numeric value: **2000**.

## 4. Sticky Bit

The sticky bit protects files in shared directories. Users generally cannot delete or rename files owned by other users, even when the directory is writable by everyone. The file owner, directory owner, or root can remove files, subject to other system restrictions.

The `/tmp` directory is a common example.

### Commands

```bash
ls -ld /tmp
chmod o+t directory
chmod 1775 directory
chmod o-t directory
chmod 0775 directory
```

- `t` in the others' execute position indicates the sticky bit and execute permission are set.
- `T` indicates the sticky bit is set, but others' execute permission is not.
- Numeric value: **1000**.

## 5. Numeric Values for Special Permissions

| Permission | Numeric value | Purpose |
|---|---:|---|
| setuid | `4000` | Runs an executable with its owner's permissions |
| setgid | `2000` | Uses the file's group permissions or supports shared directory group ownership |
| Sticky bit | `1000` | Protects files in shared directories |

The special permission digit comes before the three ordinary permission digits.

For example, `2775` means setgid is enabled, with ordinary permissions `rwxrwxr-x`.

## 6. Links in Linux

Links provide another name or a reference to an existing file.

### Hard Links

A hard link is another filename pointing to the same inode and file data as the original.

```bash
ln original.txt hardlink.txt
ls -li original.txt hardlink.txt
```

- Both filenames share the same inode number.
- The link count increases when a hard link is created.
- Removing one hard link does not delete the data while another hard link remains.
- Hard links normally cannot cross filesystems or link to directories.

### Symbolic Links

A symbolic link, also called a soft link, points to another file or directory using a pathname.

```bash
ln -s original.txt symlink.txt
ls -l symlink.txt
```

- The listing begins with `l` and displays the target path.
- Symbolic links can point to files or directories.
- They can cross filesystem boundaries.
- If the target is removed or moved, the symbolic link may become broken.

## 7. Comparing Hard and Symbolic Links

| Feature | Hard link | Symbolic link |
|---|---|---|
| Inode | Same as target | Separate inode |
| Target removed | Data remains if another hard link exists | Link may break |
| Cross-filesystem links | No | Yes |
| Links to directories | Normally not allowed | Allowed |
| Identifying links | Compare inode numbers with `ls -i` | Use `ls -l` to see the target |

To find hard links with a known inode number, the course demonstrates:

```bash
ls -i original.txt
find / -inum INODE_NUMBER 2>/dev/null
```

Replace `INODE_NUMBER` with the actual inode number.

## Key Takeaways

- setuid, setgid, and the sticky bit provide special permission behaviors.
- Their numeric values are `4000`, `2000`, and `1000`, respectively.
- setgid directories help users collaborate by preserving group ownership.
- The sticky bit helps protect files in shared directories.
- Hard links share an inode; symbolic links point to a pathname.
- Use `ls -l`, `ls -ld`, and `ls -i` to inspect permissions and links.
- Be cautious when changing special permissions because they can affect system security.

