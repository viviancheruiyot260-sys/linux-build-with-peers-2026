
Module 16: User and Group Management

## 16.1 Introduction
Linux accounts help control who can use the system and access files.

- **Users:** Individual accounts.
- **Groups:** Help users share files and resources.
- **Root:** The administrator account.
- Plan groups before creating users when possible.

## 16.2 Groups
Groups allow users working together to share files and directories.

### Creating a Group
```bash
sudo groupadd research
getent group research
```

- `groupadd` creates a group.
- `-g` sets a specific group ID (GID).
- `-r` creates a system group.

### Modifying a Group
```bash
sudo groupmod -n clerks sales
sudo groupmod -g 1005 clerks
```

- `-n` changes the group name.
- `-g` changes the group ID.
- Changing a GID can leave files linked only to an old numeric ID.

### Deleting a Group
```bash
sudo groupdel research
```

A group cannot be deleted while it is a user's primary group. Deleting groups can affect file ownership.

### Viewing Groups
```bash
grep research /etc/group
getent group research
```

## 16.3 Users
User information is stored in `/etc/passwd`, while password information is stored in `/etc/shadow`.

### User Defaults
```bash
useradd -D
```

This displays default settings for new accounts, such as the home directory, shell, and account expiry settings.

The `/etc/login.defs` file contains other account defaults, including UID/GID ranges and password-aging settings.

### Creating a User
```bash
sudo useradd -m jane
sudo passwd jane
```

- `useradd` creates a user.
- `-m` creates the home directory.
- `-u` sets the UID.
- `-g` sets the primary group.
- `-G` sets supplementary groups.
- `-s` sets the login shell.
- `-c` adds a comment or full name.

Example with groups:
```bash
sudo useradd -m -G sales,research jane
```

### Passwords
Use strong, unique passwords and never share them.

```bash
passwd
sudo passwd jane
```

- `passwd` changes your password.
- `sudo passwd jane` lets an authorized administrator set Jane's password.

### Password Expiry
The `chage` command manages password-aging settings.

```bash
sudo chage -l jane
sudo chage -M 60 jane
```

- `-l` displays password-aging information.
- `-M` sets the maximum password age in days.

### Modifying a User
The `usermod` command changes an existing account.

```bash
sudo usermod -aG development jane
```

This adds Jane to the `development` group without removing her other supplementary groups.

Other options:
- `-l` changes the login name.
- `-g` changes the primary group.
- `-s` changes the login shell.
- `-L` locks the account.
- `-U` unlocks the account.

**Important:** Using `-G` without `-a` can replace existing supplementary group memberships.

### Deleting a User
```bash
sudo userdel jane
sudo userdel -r jane
```

- `userdel` deletes the account.
- `userdel -r` also removes the home directory and mail spool.

Check for important files before deleting accounts. Files outside the home directory may remain.

## Key Takeaways
- `groupadd`, `groupmod`, and `groupdel` manage groups.
- `useradd`, `usermod`, and `userdel` manage users.
- `passwd` changes passwords.
- `chage` manages password expiry.
- `/etc/passwd`, `/etc/shadow`, and `/etc/group` store account information.
- Always check account memberships and important files before making changes.
