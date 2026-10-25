# Lab 16: Creating Users and Groups
Learn to create, modify, and delete Linux users and groups, manage passwords, and check group membership.

## 1. Create and Manage Groups

```bash
su -
groupadd -r research
groupadd -r sales
getent group research
grep sales /etc/group
```

- `su -` switches to the root account.
- `groupadd -r` creates a system group.
- `getent` and `grep` display group information.

Rename and change the GID of `sales`:

```bash
groupmod -n clerks sales
groupmod -g 10003 clerks
grep clerks /etc/group
groupdel clerks
```

- `groupmod -n` renames a group.
- `groupmod -g` changes its GID.
- `groupdel` deletes a group.

## 2. Configure User Defaults

```bash
useradd -D
useradd -D -f 30
useradd -D
nano /etc/default/useradd
```

Change `CREATE_MAIL_SPOOL=no` to `CREATE_MAIL_SPOOL=yes`, save the file, then verify:

```bash
useradd -D
```

- `useradd -D` displays default settings.
- `-f 30` sets the inactive period to 30 days after password expiry.
- `CREATE_MAIL_SPOOL=yes` enables mail spool creation for new users.

## 3. Create a User

Create `student` with a home directory, a private primary group, and membership in `research`:

```bash
useradd -G research -c 'Linux Student' -m student
grep student /etc/passwd
grep student /etc/group
```

- `-G` adds a supplementary group.
- `-c` adds a comment or full name.
- `-m` creates the home directory.

## 4. Modify and Verify Groups

Add `sysadmin` to the `research` group:

```bash
usermod -aG research sysadmin
getent group research
getent group student
getent passwd student
getent shadow student
```

- `usermod -aG` adds a supplementary group without replacing existing memberships.
- `/etc/passwd` stores basic account information.
- `/etc/shadow` stores password-related information.

## 5. Check Login History

```bash
last
last student
```

- `last` displays login history.
- No entry for `student` may mean the user has not logged in.

## 6. Delete the User

```bash
userdel -r student
grep student /etc/group
```

- `userdel -r` deletes the account and removes its home directory and mail spool.

## Key Takeaways

- `groupadd`, `groupmod`, and `groupdel` manage groups.
- `useradd`, `usermod`, and `userdel` manage users.
- `getent` and `grep` help verify account information.
- Always check group memberships and files before deleting accounts or groups.


