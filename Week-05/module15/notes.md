User and Group Management

## 15.1 Introduction
Linux uses users, groups, and permissions to control who can access files and system resources.

## 15.2 Administrative Accounts
- `root` is the administrator account with UID `0`.
- `sudo` runs commands with administrative privileges.
- `su - username` switches to another user.
- `exit` returns to the previous shell.

Example:
```bash
sudo apt update
```

## 15.3 User Accounts
The `/etc/passwd` file stores basic user information, including username, UID, GID, home directory, and shell.

Commands:
```bash
cat /etc/passwd
grep sysadmin /etc/passwd
```

## 15.3.1 Passwords
The `/etc/shadow` file stores password hashes and password-expiry information. Access is restricted for security.

```bash
sudo tail -5 /etc/shadow
getent passwd sysadmin
```

Important: Never share password hashes or `/etc/shadow` contents.

## 15.4 System Accounts
System accounts are used by services, not usually by people logging in. They may use `/usr/sbin/nologin`.

Do not delete system accounts unless you understand their purpose.

## 15.5 Group Accounts
Groups help manage access for multiple users. `/etc/group` stores group information and supplementary members.

```bash
cat /etc/group
getent group sudo
```

## 15.6 Viewing User Information
The `id` command displays a user's ID and group membership.

```bash
id
id root
id -g
id -G
```

## 15.7 Viewing Current Users
- `who` — shows currently logged-in users.
- `w` — shows users and more system activity.
- `who -b` — shows the last boot time.
- `who -r` — shows the current runlevel or run state.

## 15.8 Viewing Login History
The `last` command displays recorded login sessions and reboot history.

```bash
last
last sysadmin
```

## Key Takeaways
- Users have UIDs; groups have GIDs.
- `/etc/passwd` stores user details.
- `/etc/shadow` stores protected password information.
- `/etc/group` stores group information.
- `sudo` provides authorized administrative access.
- `id`, `who`, `w`, and `last` help inspect users and login activity.
