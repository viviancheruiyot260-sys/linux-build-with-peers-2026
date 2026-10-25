
Module 17: File Ownership and Permissions

1. File Ownership

Every file has:
- **User owner:** The user who owns the file.
- **Group owner:** The group associated with the file.

By default, files belong to the user who creates them and that user's primary group.

### Useful Commands

| Command | Purpose |
|---|---|
| `id` | Shows your UID, GID, and group memberships. |
| `ls -l` | Displays file permissions and ownership. |
| `ls -la` | Displays all files, including hidden files. |
| `stat filename` | Shows detailed file information. |

## 2. Changing Ownership

| Command | Purpose |
|---|---|
| `chgrp group file` | Changes a file's group ownership. |
| `chgrp -R group directory` | Changes group ownership recursively. |
| `sudo chown user file` | Changes the file's user owner. |
| `sudo chown user:group file` | Changes both user and group ownership. |
| `chown :group file` | Changes only the group owner, if permitted. |

Changing user ownership usually requires administrator privileges. A regular user can change a file's group to
